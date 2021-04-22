---
title: /Users/chenjing/work/4paradigm/HybridSE/java/hybridse-sdk/src/main/java/com/_4paradigm/hybridse/sdk/JitManager.java

---
# /Users/chenjing/work/4paradigm/HybridSE/java/hybridse-sdk/src/main/java/com/_4paradigm/hybridse/sdk/JitManager.java

## Namespaces

| Name           |
| -------------- |
| **[com._4paradigm.hybridse.sdk](/hybridse/usage/api/java/Namespaces/namespacecom_1_1__4paradigm_1_1hybridse_1_1sdk.md)**  |

## Classes

|                | Name           |
| -------------- | -------------- |
| class | **[com._4paradigm.hybridse.sdk.JitManager](/hybridse/usage/api/java/Classes/classcom_1_1__4paradigm_1_1hybridse_1_1sdk_1_1_jit_manager.md)** <br>JIT manager provides a set of API to access jit, configure JitOptions and init llvm module.  |




## Source code

```cpp
/*
 * Copyright 2021 4Paradigm
 *
 * Licensed under the Apache License, Version 2.0 (the "License");
 * you may not use this file except in compliance with the License.
 * You may obtain a copy of the License at
 *
 * http://www.apache.org/licenses/LICENSE-2.0
 *
 * Unless required by applicable law or agreed to in writing, software
 * distributed under the License is distributed on an "AS IS" BASIS,
 * WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
 * See the License for the specific language governing permissions and
 * limitations under the License.
 */

package com._4paradigm.hybridse.sdk;

import com._4paradigm.hybridse.HybridSeLibrary;
import com._4paradigm.hybridse.vm.Engine;
import com._4paradigm.hybridse.vm.HybridSeJitWrapper;
import com._4paradigm.hybridse.vm.JitOptions;
import java.io.IOException;
import java.io.InputStream;
import java.nio.ByteBuffer;
import java.util.HashMap;
import java.util.HashSet;
import java.util.Map;
import java.util.Properties;
import java.util.Set;
import org.slf4j.Logger;
import org.slf4j.LoggerFactory;

public class JitManager {

    private static Logger logger = LoggerFactory.getLogger(JitManager.class);

    static {
        HybridSeLibrary.initCore();
        Engine.InitializeGlobalLLVM();
    }

    // One jit currently only take one llvm module, since symbol may duplicate
    private static Map<String, HybridSeJitWrapper> jits = new HashMap<>();
    private static Set<String> initializedModuleTags = new HashSet<>();

    public static synchronized HybridSeJitWrapper getJit(String tag) {
        if (!jits.containsKey(tag)) {
            HybridSeJitWrapper jit = HybridSeJitWrapper.Create(getJitOptions());
            if (jit == null) {
                throw new RuntimeException("Fail to create native jit");
            }
            jit.Init();
            HybridSeJitWrapper.InitJitSymbols(jit);
            jits.put(tag, jit);
        }
        return jits.get(tag);
    }

    private static JitOptions getJitOptions() {
        JitOptions options = new JitOptions();
        try (InputStream input = JitManager.class.getClassLoader().getResourceAsStream("jit.properties")) {
            Properties prop = new Properties(System.getProperties());
            if (input == null) {
                return options;
            }
            prop.load(input);
            String enableMcJit = prop.getProperty("fesql.jit.enable_mcjit");
            if (enableMcJit != null && enableMcJit.toLowerCase().equals("true")) {
                logger.info("Try enable llvm legacy mcjit support");
                options.set_enable_mcjit(true);
            }
            String enableVtune = prop.getProperty("fesql.jit.enable_vtune");
            if (enableVtune != null && enableVtune.toLowerCase().equals("true")) {
                logger.info("Try enable intel jit events support");
                options.set_enable_vtune(true);
            }
            String enablePerf = prop.getProperty("fesql.jit.enable_perf");
            if (enablePerf != null && enablePerf.toLowerCase().equals("true")) {
                logger.info("Try enable perf jit events support");
                options.set_enable_perf(true);
            }
            String enableGdb = prop.getProperty("fesql.jit.enable_gdb");
            if (enableGdb != null && enableGdb.toLowerCase().equals("true")) {
                logger.info("Try enable gdb jit events support");
                options.set_enable_gdb(true);
            }
        } catch (IOException ex) {
            logger.debug("Can not find jit.properties", ex);
        }
        return options;
    }

    private static synchronized boolean hasModule(String tag) {
        return initializedModuleTags.contains(tag);
    }

    private static synchronized void initModule(String tag, ByteBuffer moduleBuffer) {
        HybridSeJitWrapper jit = getJit(tag);
        if (!moduleBuffer.isDirect()) {
            throw new RuntimeException("JIT must use direct buffer");
        }
        if (!jit.AddModuleFromBuffer(moduleBuffer)) {
            throw new RuntimeException("Fail to initialize native module");
        }
        initializedModuleTags.add(tag);
    }

    public static synchronized void initJitModule(String tag, ByteBuffer moduleBuffer) {

        // ensure worker native
        HybridSeLibrary.initCore();

        // ensure worker side module
        if (!JitManager.hasModule(tag)) {
            JitManager.initModule(tag, moduleBuffer);
            logger.info("Init jit module with tag:\n" + tag);
        }
    }

    public static synchronized void removeModule(String tag) {
        initializedModuleTags.remove(tag);
        HybridSeJitWrapper jit = jits.remove(tag);
        if (jit != null) {
            HybridSeJitWrapper.DeleteJit(jit);
            jit.delete();
        }
    }

    public static synchronized void clear() {
        initializedModuleTags.clear();
        for (Map.Entry<String, HybridSeJitWrapper> entry : jits.entrySet()) {
            HybridSeJitWrapper.DeleteJit(entry.getValue());
            entry.getValue().delete();
        }
        jits.clear();
    }
}
```



