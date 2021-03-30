---
title: hybridse::vm::MemTimeTableIterator

---
# hybridse::vm::MemTimeTableIterator



`#include <mem_catalog.h>`

## Summary


|  Public functions|            |
| -------------- | -------------- |
|**[MemTimeTableIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_iterator.md#function-memtimetableiterator)**(const [MemTimeTable](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#typedef-memtimetable) * table, const vm::Schema * schema)|  |
|**[MemTimeTableIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_iterator.md#function-memtimetableiterator)**(const [MemTimeTable](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#typedef-memtimetable) * table, const vm::Schema * schema, int32_t start, int32_t end)|  |
|**[~MemTimeTableIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_iterator.md#function-~memtimetableiterator)**()|  |
|**[Seek](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_iterator.md#function-seek)**(const uint64_t & ts)| void  |
|**[SeekToFirst](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_iterator.md#function-seektofirst)**()| void  |
|**[GetKey](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_iterator.md#function-getkey)**() const| const uint64_t &  |
|**[Next](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_iterator.md#function-next)**()| void  |
|**[Valid](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_iterator.md#function-valid)**() const| bool  |
|**[GetValue](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_iterator.md#function-getvalue)**() override| const [Row](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row.md) &  |
|**[IsSeekable](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_iterator.md#function-isseekable)**() const override| bool  |

## Public Functions

#### MemTimeTableIterator { function MemTimeTableIterator }

```cpp
MemTimeTableIterator(
    const MemTimeTable * table,
    const vm::Schema * schema
)
```


#### MemTimeTableIterator { function MemTimeTableIterator }

```cpp
MemTimeTableIterator(
    const MemTimeTable * table,
    const vm::Schema * schema,
    int32_t start,
    int32_t end
)
```


#### ~MemTimeTableIterator { function ~MemTimeTableIterator }

```cpp
~MemTimeTableIterator()
```


#### Seek { function Seek }

```cpp
void Seek(
    const uint64_t & ts
)
```


#### SeekToFirst { function SeekToFirst }

```cpp
void SeekToFirst()
```


#### GetKey { function GetKey }

```cpp
const uint64_t & GetKey() const
```


#### Next { function Next }

```cpp
void Next()
```


#### Valid { function Valid }

```cpp
bool Valid() const
```


#### GetValue { function GetValue }

```cpp
const Row & GetValue() override
```


#### IsSeekable { function IsSeekable }

```cpp
bool IsSeekable() const override
```


-------------------------------

Updated on 29 March 2021 at 17:58:50 PDT