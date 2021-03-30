---
title: hybridse::vm::MemTableIterator

---
# hybridse::vm::MemTableIterator



`#include <mem_catalog.h>`

## Summary


|  Public functions|            |
| -------------- | -------------- |
|**[MemTableIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_table_iterator.md#function-memtableiterator)**(const [MemTable](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#typedef-memtable) * table, const vm::Schema * schema)|  |
|**[MemTableIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_table_iterator.md#function-memtableiterator)**(const [MemTable](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#typedef-memtable) * table, const vm::Schema * schema, int32_t start, int32_t end)|  |
|**[~MemTableIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_table_iterator.md#function-~memtableiterator)**()|  |
|**[Seek](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_table_iterator.md#function-seek)**(const uint64_t & ts)| void  |
|**[SeekToFirst](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_table_iterator.md#function-seektofirst)**()| void  |
|**[GetKey](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_table_iterator.md#function-getkey)**() const| const uint64_t &  |
|**[GetValue](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_table_iterator.md#function-getvalue)**()| const [Row](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row.md) &  |
|**[Next](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_table_iterator.md#function-next)**()| void  |
|**[Valid](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_table_iterator.md#function-valid)**() const| bool  |
|**[IsSeekable](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_table_iterator.md#function-isseekable)**() const override| bool  |

## Public Functions

#### function MemTableIterator

```cpp
MemTableIterator(
    const MemTable * table,
    const vm::Schema * schema
)
```


#### function MemTableIterator

```cpp
MemTableIterator(
    const MemTable * table,
    const vm::Schema * schema,
    int32_t start,
    int32_t end
)
```


#### function ~MemTableIterator

```cpp
~MemTableIterator()
```


#### function Seek

```cpp
void Seek(
    const uint64_t & ts
)
```


#### function SeekToFirst

```cpp
void SeekToFirst()
```


#### function GetKey

```cpp
const uint64_t & GetKey() const
```


#### function GetValue

```cpp
const Row & GetValue()
```


#### function Next

```cpp
void Next()
```


#### function Valid

```cpp
bool Valid() const
```


#### function IsSeekable

```cpp
bool IsSeekable() const override
```


-------------------------------

Updated on 29 March 2021 at 18:05:16 PDT