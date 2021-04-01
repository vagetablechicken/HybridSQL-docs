---
title: hybridse::vm::MemWindowIterator

---
# hybridse::vm::MemWindowIterator



`#include <mem_catalog.h>`

## Summary


|  Public functions|            |
| -------------- | -------------- |
|**[MemWindowIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_window_iterator.md#function-memwindowiterator)**(const [MemSegmentMap](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#typedef-memsegmentmap) * partitions, const Schema * schema)|  |
|**[~MemWindowIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_window_iterator.md#function-~memwindowiterator)**()|  |
|**[Seek](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_window_iterator.md#function-seek)**(const std::string & key)| void  |
|**[SeekToFirst](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_window_iterator.md#function-seektofirst)**()| void <br>Move to the beginning of the dataset.  |
|**[Next](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_window_iterator.md#function-next)**()| void  |
|**[Valid](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_window_iterator.md#function-valid)**()| bool  |
|**[GetValue](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_window_iterator.md#function-getvalue)**()| std::unique_ptr< RowIterator >  |
|**[GetRawValue](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_window_iterator.md#function-getrawvalue)**()| RowIterator *  |
|**[GetKey](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_window_iterator.md#function-getkey)**()| const [Row](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row.md)  |

## Inherited members
Inherited from [hybridse::codec::WindowIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_window_iterator.md)
| **Inherited public functions** | Name           |
| -------------- | -------------- |
|**[WindowIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_window_iterator.md#function-windowiterator)**()|  |
|**[~WindowIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_window_iterator.md#function-~windowiterator)**()| virtual  |


## Public Functions

#### function MemWindowIterator

```cpp
MemWindowIterator(
    const MemSegmentMap * partitions,
    const Schema * schema
)
```


#### function ~MemWindowIterator

```cpp
~MemWindowIterator()
```


#### function Seek

```cpp
virtual void Seek(
    const std::string & key
)
```


**Reimplements**: [hybridse::codec::WindowIterator::Seek](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_window_iterator.md#function-seek)


Set the dataset's current position at the segment with key equals to `key`


#### function SeekToFirst

```cpp
virtual void SeekToFirst()
```

Move to the beginning of the dataset. 

**Reimplements**: [hybridse::codec::WindowIterator::SeekToFirst](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_window_iterator.md#function-seektofirst)


#### function Next

```cpp
virtual void Next()
```


**Reimplements**: [hybridse::codec::WindowIterator::Next](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_window_iterator.md#function-next)


Move to the next segment in the iteration if [Valid()](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_window_iterator.md#function-valid) return `true`. 


#### function Valid

```cpp
virtual bool Valid()
```


**Reimplements**: [hybridse::codec::WindowIterator::Valid](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_window_iterator.md#function-valid)


Return `true` if the iteration has elements. 


#### function GetValue

```cpp
virtual std::unique_ptr< RowIterator > GetValue()
```


**Reimplements**: [hybridse::codec::WindowIterator::GetValue](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_window_iterator.md#function-getvalue)


Return the RowIterator of current segment of dataset if [Valid()](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_window_iterator.md#function-valid) return `true`. 


#### function GetRawValue

```cpp
virtual RowIterator * GetRawValue()
```


**Reimplements**: [hybridse::codec::WindowIterator::GetRawValue](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_window_iterator.md#function-getrawvalue)


Return the RowIterator of current segment of dataset if [Valid()](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_window_iterator.md#function-valid) return `true`. 


#### function GetKey

```cpp
virtual const Row GetKey()
```


**Reimplements**: [hybridse::codec::WindowIterator::GetKey](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_window_iterator.md#function-getkey)


Return the key of current segment of dataset if [Valid()](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_window_iterator.md#function-valid) is `true`


-------------------------------

Updated on  1 April 2021 at 16:11:23 PDT