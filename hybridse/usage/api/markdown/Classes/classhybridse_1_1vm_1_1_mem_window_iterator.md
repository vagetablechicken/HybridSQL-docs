---
title: hybridse::vm::MemWindowIterator

---

# hybridse::vm::MemWindowIterator




`#include <mem_catalog.h>`

Inherits from [hybridse::codec::WindowIterator](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_window_iterator.md)

## Public Functions

|                | Name           |
| -------------- | -------------- |
| | **[MemWindowIterator](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_window_iterator.md#function-memwindowiterator)**(const [MemSegmentMap](/hybridse/usage/api/markdown/Namespaces/namespacehybridse_1_1vm.md#typedef-memsegmentmap) * partitions, const Schema * schema) |
| | **[~MemWindowIterator](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_window_iterator.md#function-~memwindowiterator)**() |
| virtual void | **[Seek](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_window_iterator.md#function-seek)**(const std::string & key) |
| virtual void | **[SeekToFirst](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_window_iterator.md#function-seektofirst)**() |
| virtual void | **[Next](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_window_iterator.md#function-next)**()<br>Move to the next segmen in the iteration if `[Valid()]()` return `true`.  |
| virtual bool | **[Valid](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_window_iterator.md#function-valid)**() |
| virtual std::unique_ptr< RowIterator > | **[GetValue](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_window_iterator.md#function-getvalue)**() |
| virtual RowIterator * | **[GetRawValue](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_window_iterator.md#function-getrawvalue)**() |
| virtual const [Row](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_row.md) | **[GetKey](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_window_iterator.md#function-getkey)**() |

## Additional inherited members

**Public Functions inherited from [hybridse::codec::WindowIterator](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_window_iterator.md)**

|                | Name           |
| -------------- | -------------- |
| | **[WindowIterator](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_window_iterator.md#function-windowiterator)**() |
| virtual | **[~WindowIterator](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_window_iterator.md#function-~windowiterator)**() |


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
virtual void Seek(
    const std::string & key
)
```


**Reimplements**: [hybridse::codec::WindowIterator::Seek](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_window_iterator.md#function-seek)


### function SeekToFirst

```cpp
virtual void SeekToFirst()
```


**Reimplements**: [hybridse::codec::WindowIterator::SeekToFirst](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_window_iterator.md#function-seektofirst)


### function Next

```cpp
virtual void Next()
```

Move to the next segmen in the iteration if `[Valid()]()` return `true`. 

**Reimplements**: [hybridse::codec::WindowIterator::Next](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_window_iterator.md#function-next)


### function Valid

```cpp
virtual bool Valid()
```


**Return**: 

**Reimplements**: [hybridse::codec::WindowIterator::Valid](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_window_iterator.md#function-valid)


Return `true` if the iteration has elements. 


### function GetValue

```cpp
virtual std::unique_ptr< RowIterator > GetValue()
```


**Reimplements**: [hybridse::codec::WindowIterator::GetValue](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_window_iterator.md#function-getvalue)


Return the `RowIterator` of current segment of dataset if `[Valid()](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_window_iterator.md#function-valid)` return `true`. 


### function GetRawValue

```cpp
virtual RowIterator * GetRawValue()
```


**Reimplements**: [hybridse::codec::WindowIterator::GetRawValue](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_window_iterator.md#function-getrawvalue)


### function GetKey

```cpp
virtual const Row GetKey()
```


**Reimplements**: [hybridse::codec::WindowIterator::GetKey](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_window_iterator.md#function-getkey)


-------------------------------

Updated on 29 March 2021 at 10:12:21 PDT