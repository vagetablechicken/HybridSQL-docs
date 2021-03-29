---
title: hybridse::codec::WindowIterator
summary: A iterator over a Row-Iterator<Row> pairs dataset. 

---

# hybridse::codec::WindowIterator



A iterator over a Row-Iterator<Row> pairs dataset.  [More...](#detailed-description)


`#include <row_iterator.h>`

Inherited by [hybridse::vm::MemWindowIterator](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_window_iterator.md)

## Public Functions

|                | Name           |
| -------------- | -------------- |
| | **[WindowIterator](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_window_iterator.md#function-windowiterator)**() |
| virtual | **[~WindowIterator](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_window_iterator.md#function-~windowiterator)**() |
| virtual void | **[Seek](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_window_iterator.md#function-seek)**(const std::string & key) =0 |
| virtual void | **[SeekToFirst](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_window_iterator.md#function-seektofirst)**() =0 |
| virtual void | **[Next](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_window_iterator.md#function-next)**() =0<br>Move to the next segmen in the iteration if `[Valid()]()` return `true`.  |
| virtual bool | **[Valid](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_window_iterator.md#function-valid)**() =0 |
| virtual std::unique_ptr< [RowIterator](/hybridse/usage/api/markdown/Namespaces/namespacehybridse_1_1codec.md#typedef-rowiterator) > | **[GetValue](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_window_iterator.md#function-getvalue)**() =0 |
| virtual [RowIterator](/hybridse/usage/api/markdown/Namespaces/namespacehybridse_1_1codec.md#typedef-rowiterator) * | **[GetRawValue](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_window_iterator.md#function-getrawvalue)**() =0 |
| virtual const [Row](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_row.md) | **[GetKey](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_window_iterator.md#function-getkey)**() =0 |

## Detailed Description

```cpp
class hybridse::codec::WindowIterator;
```

A iterator over a Row-Iterator<Row> pairs dataset. 

Example

Assuming the dataset is logically organized by segments, we can use `Valid`, `Next` and `GetValue` methods to iterate these "segments" one by one. Then when it comes to segment, it's easily to access the rows with `RowIterator` 's interfaces. 

```cpp
 // assume we have got and initialized an window iterator already
 // here is an example of counting segments and rows in the dataset
 size_t segment_num = 0, row_num = 0;
 while (window_iterator->Valid()) {
     segment_num += 1;
     auto &row_iterator = window_iterator->GetValue();
     auto &key = window_iterator->GetKey();
     while (row_iterator->Valid()) {
         row_num += 1;
         row_iterator->Next();
     }
}
```

## Public Functions Documentation

### function WindowIterator

```cpp
inline WindowIterator()
```


### function ~WindowIterator

```cpp
inline virtual ~WindowIterator()
```


### function Seek

```cpp
virtual void Seek(
    const std::string & key
) =0
```


**Reimplemented by**: [hybridse::vm::MemWindowIterator::Seek](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_window_iterator.md#function-seek)


### function SeekToFirst

```cpp
virtual void SeekToFirst() =0
```


**Reimplemented by**: [hybridse::vm::MemWindowIterator::SeekToFirst](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_window_iterator.md#function-seektofirst)


### function Next

```cpp
virtual void Next() =0
```

Move to the next segmen in the iteration if `[Valid()]()` return `true`. 

**Reimplemented by**: [hybridse::vm::MemWindowIterator::Next](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_window_iterator.md#function-next)


### function Valid

```cpp
virtual bool Valid() =0
```


**Return**: 

**Reimplemented by**: [hybridse::vm::MemWindowIterator::Valid](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_window_iterator.md#function-valid)


Return `true` if the iteration has elements. 


### function GetValue

```cpp
virtual std::unique_ptr< RowIterator > GetValue() =0
```


**Reimplemented by**: [hybridse::vm::MemWindowIterator::GetValue](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_window_iterator.md#function-getvalue)


Return the `RowIterator` of current segment of dataset if `[Valid()](/hybridse/usage/api/markdown/Classes/classhybridse_1_1codec_1_1_window_iterator.md#function-valid)` return `true`. 


### function GetRawValue

```cpp
virtual RowIterator * GetRawValue() =0
```


**Reimplemented by**: [hybridse::vm::MemWindowIterator::GetRawValue](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_window_iterator.md#function-getrawvalue)


### function GetKey

```cpp
virtual const Row GetKey() =0
```


**Reimplemented by**: [hybridse::vm::MemWindowIterator::GetKey](/hybridse/usage/api/markdown/Classes/classhybridse_1_1vm_1_1_mem_window_iterator.md#function-getkey)


-------------------------------

Updated on 29 March 2021 at 10:12:21 PDT