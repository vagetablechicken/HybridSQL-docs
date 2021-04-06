---
title: /Users/chenjing/work/4paradigm/HybridSE/include/codec/row_iterator.h

---
# /Users/chenjing/work/4paradigm/HybridSE/include/codec/row_iterator.h

## Namespaces

| Name           |
| -------------- |
| **[hybridse](/hybridse/usage/api/c++/Namespaces/namespacehybridse.md)**  |
| **[hybridse::codec](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1codec.md)**  |

## Classes

|                | Name           |
| -------------- | -------------- |
| class | **[hybridse::codec::WindowIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_window_iterator.md)** <br>A iterator over a Row-Iterator<[codec::Row](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row.md)> pairs dataset.  |




## Source code

```cpp
/*
 * row_iterator.h
 * Copyright (C) 4paradigm 2021 chenjing <chenjing@4paradigm.com>
 * Licensed under the Apache License, Version 2.0 (the "License");
 * you may not use this file except in compliance with the License.
 * You may obtain a copy of the License at
 *
 *    http://www.apache.org/licenses/LICENSE-2.0
 *
 * Unless required by applicable law or agreed to in writing, software
 * distributed under the License is distributed on an "AS IS" BASIS,
 * WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
 * See the License for the specific language governing permissions and
 * limitations under the License.
 */
#ifndef INCLUDE_CODEC_ROW_ITERATOR_H_
#define INCLUDE_CODEC_ROW_ITERATOR_H_
#include <memory>
#include <string>
#include "codec/row.h"
namespace hybridse {
namespace codec {
using hybridse::base::ConstIterator;

typedef ConstIterator<uint64_t, Row> RowIterator;

class WindowIterator {
 public:
    WindowIterator() {}
    virtual ~WindowIterator() {}

    virtual void Seek(const std::string &key) = 0;
    virtual void SeekToFirst() = 0;
    virtual void Next() = 0;
    virtual bool Valid() = 0;
    virtual std::unique_ptr<RowIterator> GetValue() = 0;
    virtual RowIterator *GetRawValue() = 0;
    virtual const Row GetKey() = 0;
};
}  // namespace codec
}  // namespace hybridse

#endif  // INCLUDE_CODEC_ROW_ITERATOR_H_
```


-------------------------------

Updated on  6 April 2021 at 09:17:26 PDT
