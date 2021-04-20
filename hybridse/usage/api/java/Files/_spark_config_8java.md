---
title: /Users/chenjing/work/4paradigm/HybridSE/java/hybridse-sdk/src/main/java/com/_4paradigm/hybridse/element/SparkConfig.java

---
# /Users/chenjing/work/4paradigm/HybridSE/java/hybridse-sdk/src/main/java/com/_4paradigm/hybridse/element/SparkConfig.java

## Namespaces

| Name           |
| -------------- |
| **[com._4paradigm.hybridse.element](/hybridse/usage/api/java/Namespaces/namespacecom_1_1__4paradigm_1_1hybridse_1_1element.md)**  |

## Classes

|                | Name           |
| -------------- | -------------- |
| class | **[com._4paradigm.hybridse.element.SparkConfig](/hybridse/usage/api/java/Classes/classcom_1_1__4paradigm_1_1hybridse_1_1element_1_1_spark_config.md)**  |




## Source code

```cpp
/*
 * Copyright 2021 4Paradigm
 *
 * Licensed under the Apache License, Version 2.0 (the "License");
 * you may not use this file except in compliance with the License.
 * You may obtain a copy of the License at
 *
 *   http://www.apache.org/licenses/LICENSE-2.0
 *
 * Unless required by applicable law or agreed to in writing, software
 * distributed under the License is distributed on an "AS IS" BASIS,
 * WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
 * See the License for the specific language governing permissions and
 * limitations under the License.
 */

package com._4paradigm.hybridse.element;

import lombok.Data;

import java.util.*;

@Data
public class SparkConfig {
    private String sql = "";
    private Map<String, String> tables = new LinkedHashMap<>();
    private List<String> sparkConfig = new ArrayList<>();
    private String outputPath = "";
    private String instanceFormat = "parquet";
}
```



