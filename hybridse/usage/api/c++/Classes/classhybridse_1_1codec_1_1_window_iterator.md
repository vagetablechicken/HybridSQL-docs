---
title: hybridse::codec::WindowIterator
summary: A iterator over a Row-Iterator<codec::Row> pairs dataset. 

---
# hybridse::codec::WindowIterator



`#include <row_iterator.h>`

A iterator over a Row-Iterator<[codec::Row](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row.md)> pairs dataset. 
## Summary

```cpp
class hybridse::codec::WindowIterator;
```
A iterator over a Row-Iterator<[codec::Row](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row.md)> pairs dataset. 

**Example**

Assuming the dataset is logically organized by segments, we can use Valid, Next and GetValue methods to iterate these "segments" one by one. Then when it comes to segment, it's easily to access the rows with RowIterator 's interfaces. 

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



|  Public functions|            |
| -------------- | -------------- |
|**[WindowIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_window_iterator.md#function-windowiterator)**()|  |
|**[~WindowIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_window_iterator.md#function-~windowiterator)**()|  |
|**[Seek](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_window_iterator.md#function-seek)**(const std::string & key) =0| void  |
|**[SeekToFirst](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_window_iterator.md#function-seektofirst)**() =0| void <br>Move to the beginning of the dataset.  |
|**[Next](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_window_iterator.md#function-next)**() =0| void  |
|**[Valid](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_window_iterator.md#function-valid)**() =0| bool  |
|**[GetValue](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_window_iterator.md#function-getvalue)**() =0| std::unique_ptr< [RowIterator](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1codec.md#typedef-rowiterator) >  |
|**[GetRawValue](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_window_iterator.md#function-getrawvalue)**() =0| [RowIterator](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1codec.md#typedef-rowiterator) *  |
|**[GetKey](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_window_iterator.md#function-getkey)**() =0| const [Row](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row.md)  |

## Public Functions

#### WindowIterator { function WindowIterator }

```cpp
inline WindowIterator()
```


#### ~WindowIterator { function ~WindowIterator }

```cpp
inline virtual ~WindowIterator()
```


#### Seek { function Seek }

```cpp
virtual void Seek(
    const std::string & key
) =0
```


**Reimplemented by**: [hybridse::vm::MemWindowIterator::Seek](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_window_iterator.md#function-seek)


Set the dataset's current position at the segment with key equals to `key`


#### SeekToFirst { function SeekToFirst }

```cpp
virtual void SeekToFirst() =0
```

Move to the beginning of the dataset. 

**Reimplemented by**: [hybridse::vm::MemWindowIterator::SeekToFirst](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_window_iterator.md#function-seektofirst)


#### Next { function Next }

```cpp
virtual void Next() =0
```


**Reimplemented by**: [hybridse::vm::MemWindowIterator::Next](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_window_iterator.md#function-next)


Move to the next segment in the iteration if [Valid()](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_window_iterator.md#function-valid) return `true`. 


#### Valid { function Valid }

```cpp
virtual bool Valid() =0
```


**Reimplemented by**: [hybridse::vm::MemWindowIterator::Valid](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_window_iterator.md#function-valid)


Return `true` if the iteration has elements. 


#### GetValue { function GetValue }

```cpp
virtual std::unique_ptr< RowIterator > GetValue() =0
```


**Reimplemented by**: [hybridse::vm::MemWindowIterator::GetValue](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_window_iterator.md#function-getvalue)


Return the RowIterator of current segment of dataset if [Valid()](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_window_iterator.md#function-valid) return `true`. 


#### GetRawValue { function GetRawValue }

```cpp
virtual RowIterator * GetRawValue() =0
```


**Reimplemented by**: [hybridse::vm::MemWindowIterator::GetRawValue](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_window_iterator.md#function-getrawvalue)


Return the RowIterator of current segment of dataset if [Valid()](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_window_iterator.md#function-valid) return `true`. 


#### GetKey { function GetKey }

```cpp
virtual const Row GetKey() =0
```


**Reimplemented by**: [hybridse::vm::MemWindowIterator::GetKey](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_window_iterator.md#function-getkey)


Return the key of current segment of dataset if [Valid()](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_window_iterator.md#function-valid) is `true`


-------------------------------

Updated on 29 March 2021 at 17:58:50 PDT