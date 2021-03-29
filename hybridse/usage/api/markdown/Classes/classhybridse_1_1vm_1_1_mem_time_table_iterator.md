---
title: hybridse::vm::MemTimeTableIterator

---

# hybridse::vm::MemTimeTableIterator




`#include <mem_catalog.h>`

Inherits from RowIterator

## Public Functions

|                | Name           |
| -------------- | -------------- |
| | **[MemTimeTableIterator](/Classes/classhybridse_1_1vm_1_1_mem_time_table_iterator.md#function-memtimetableiterator)**(const [MemTimeTable](/Namespaces/namespacehybridse_1_1vm.md#typedef-memtimetable) * table, const vm::Schema * schema) |
| | **[MemTimeTableIterator](/Classes/classhybridse_1_1vm_1_1_mem_time_table_iterator.md#function-memtimetableiterator)**(const [MemTimeTable](/Namespaces/namespacehybridse_1_1vm.md#typedef-memtimetable) * table, const vm::Schema * schema, int32_t start, int32_t end) |
| | **[~MemTimeTableIterator](/Classes/classhybridse_1_1vm_1_1_mem_time_table_iterator.md#function-~memtimetableiterator)**() |
| void | **[Seek](/Classes/classhybridse_1_1vm_1_1_mem_time_table_iterator.md#function-seek)**(const uint64_t & ts) |
| void | **[SeekToFirst](/Classes/classhybridse_1_1vm_1_1_mem_time_table_iterator.md#function-seektofirst)**() |
| const uint64_t & | **[GetKey](/Classes/classhybridse_1_1vm_1_1_mem_time_table_iterator.md#function-getkey)**() const |
| void | **[Next](/Classes/classhybridse_1_1vm_1_1_mem_time_table_iterator.md#function-next)**() |
| bool | **[Valid](/Classes/classhybridse_1_1vm_1_1_mem_time_table_iterator.md#function-valid)**() const |
| const Row & | **[GetValue](/Classes/classhybridse_1_1vm_1_1_mem_time_table_iterator.md#function-getvalue)**() override |
| bool | **[IsSeekable](/Classes/classhybridse_1_1vm_1_1_mem_time_table_iterator.md#function-isseekable)**() const override |

## Public Functions Documentation

### function MemTimeTableIterator

```cpp
MemTimeTableIterator(
    const MemTimeTable * table,
    const vm::Schema * schema
)
```


### function MemTimeTableIterator

```cpp
MemTimeTableIterator(
    const MemTimeTable * table,
    const vm::Schema * schema,
    int32_t start,
    int32_t end
)
```


### function ~MemTimeTableIterator

```cpp
~MemTimeTableIterator()
```


### function Seek

```cpp
void Seek(
    const uint64_t & ts
)
```


### function SeekToFirst

```cpp
void SeekToFirst()
```


### function GetKey

```cpp
const uint64_t & GetKey() const
```


### function Next

```cpp
void Next()
```


### function Valid

```cpp
bool Valid() const
```


### function GetValue

```cpp
const Row & GetValue() override
```


### function IsSeekable

```cpp
bool IsSeekable() const override
```


-------------------------------

Updated on 28 March 2021 at 19:23:48 PDT