---
title: hybridse::vm::MemWindowIterator

---

# hybridse::vm::MemWindowIterator




`#include <mem_catalog.h>`

Inherits from WindowIterator

## Public Functions

|                | Name           |
| -------------- | -------------- |
| | **[MemWindowIterator](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_mem_window_iterator.md#function-memwindowiterator)**(const [MemSegmentMap](/hybridse/usage/api/markdownNamespaces/namespacehybridse_1_1vm.md#typedef-memsegmentmap) * partitions, const Schema * schema) |
| | **[~MemWindowIterator](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_mem_window_iterator.md#function-~memwindowiterator)**() |
| void | **[Seek](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_mem_window_iterator.md#function-seek)**(const std::string & key) |
| void | **[SeekToFirst](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_mem_window_iterator.md#function-seektofirst)**() |
| void | **[Next](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_mem_window_iterator.md#function-next)**() |
| bool | **[Valid](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_mem_window_iterator.md#function-valid)**() |
| std::unique_ptr< RowIterator > | **[GetValue](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_mem_window_iterator.md#function-getvalue)**() |
| RowIterator * | **[GetRawValue](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_mem_window_iterator.md#function-getrawvalue)**() |
| const Row | **[GetKey](/hybridse/usage/api/markdownClasses/classhybridse_1_1vm_1_1_mem_window_iterator.md#function-getkey)**() |

## Public Functions Documentation

### function MemWindowIterator

```cpp
MemWindowIterator(
    const MemSegmentMap * partitions,
    const Schema * schema
)
```


### function ~MemWindowIterator

```cpp
~MemWindowIterator()
```


### function Seek

```cpp
void Seek(
    const std::string & key
)
```


### function SeekToFirst

```cpp
void SeekToFirst()
```


### function Next

```cpp
void Next()
```


### function Valid

```cpp
bool Valid()
```


### function GetValue

```cpp
std::unique_ptr< RowIterator > GetValue()
```


### function GetRawValue

```cpp
RowIterator * GetRawValue()
```


### function GetKey

```cpp
const Row GetKey()
```


-------------------------------

Updated on 28 March 2021 at 19:34:49 PDT