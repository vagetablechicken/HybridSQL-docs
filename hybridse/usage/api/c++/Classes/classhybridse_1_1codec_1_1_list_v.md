---
title: hybridse::codec::ListV
summary: Basic key-value list of HybridSe. 

---
# hybridse::codec::ListV



`#include <row_list.h>`

Basic key-value list of HybridSe. 
## Summary

```cpp
template <class V >
class hybridse::codec::ListV;
```
Basic key-value list of HybridSe. 

**Template Parameters**: 

  * **V** the type of elements in this list



The user can access a element by its position in the list. Also, can just use the iterator returned by [GetIterator()](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_list_v.md#function-getiterator) to traverse the list. 



|  Public functions|            |
| -------------- | -------------- |
|**[ListV](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_list_v.md#function-listv)**()|  |
|**[~ListV](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_list_v.md#function-~listv)**()|  |
|**[GetIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_list_v.md#function-getiterator)**() =0| std::unique_ptr< [ConstIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1base_1_1_const_iterator.md)< uint64_t, V > > <br>Return the const iterator.  |
|**[GetRawIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_list_v.md#function-getrawiterator)**() =0| [ConstIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1base_1_1_const_iterator.md)< uint64_t, V > * <br>Return the const iterator raw pointer.  |
|**[GetCount](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_list_v.md#function-getcount)**()| const uint64_t <br>Returns the number of elements in this list.  |
|**[At](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_list_v.md#function-at)**(uint64_t pos)| V <br>Return a the value of element by its position in the list.  |

## Public Functions

#### ListV

```cpp
inline ListV()
```


#### ~ListV

```cpp
inline virtual ~ListV()
```


#### GetIterator

```cpp
virtual std::unique_ptr< ConstIterator< uint64_t, V > > GetIterator() =0
```

Return the const iterator. 

**Reimplemented by**: [hybridse::vm::ErrorTableHandler::GetIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_error_table_handler.md#function-getiterator), [hybridse::vm::PartitionHandler::GetIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_partition_handler.md#function-getiterator), [hybridse::vm::MemTimeTableHandler::GetIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-getiterator), [hybridse::vm::MemSegmentHandler::GetIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_segment_handler.md#function-getiterator), [hybridse::vm::ConcatTableHandler::GetIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_concat_table_handler.md#function-getiterator), [hybridse::vm::RowHandler::GetIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_row_handler.md#function-getiterator), [hybridse::vm::MemTableHandler::GetIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_table_handler.md#function-getiterator), [hybridse::vm::Window::GetIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_window.md#function-getiterator), [hybridse::vm::RequestUnionTableHandler::GetIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_request_union_table_handler.md#function-getiterator)


#### GetRawIterator

```cpp
virtual ConstIterator< uint64_t, V > * GetRawIterator() =0
```

Return the const iterator raw pointer. 

**Reimplemented by**: [hybridse::vm::ErrorTableHandler::GetRawIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_error_table_handler.md#function-getrawiterator), [hybridse::vm::PartitionHandler::GetRawIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_partition_handler.md#function-getrawiterator), [hybridse::vm::MemTimeTableHandler::GetRawIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-getrawiterator), [hybridse::vm::Window::GetRawIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_window.md#function-getrawiterator), [hybridse::vm::ConcatTableHandler::GetRawIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_concat_table_handler.md#function-getrawiterator), [hybridse::vm::RowHandler::GetRawIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_row_handler.md#function-getrawiterator), [hybridse::vm::MemTableHandler::GetRawIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_table_handler.md#function-getrawiterator), [hybridse::vm::MemSegmentHandler::GetRawIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_segment_handler.md#function-getrawiterator), [hybridse::vm::RequestUnionTableHandler::GetRawIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_request_union_table_handler.md#function-getrawiterator)


#### GetCount

```cpp
inline virtual const uint64_t GetCount()
```

Returns the number of elements in this list. 

**Reimplemented by**: [hybridse::vm::MemTableHandler::GetCount](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_table_handler.md#function-getcount), [hybridse::vm::MemTimeTableHandler::GetCount](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-getcount), [hybridse::vm::Window::GetCount](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_window.md#function-getcount), [hybridse::vm::MemSegmentHandler::GetCount](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_segment_handler.md#function-getcount), [hybridse::vm::MemPartitionHandler::GetCount](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_partition_handler.md#function-getcount), [hybridse::vm::ConcatTableHandler::GetCount](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_concat_table_handler.md#function-getcount), [hybridse::vm::RowHandler::GetCount](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_row_handler.md#function-getcount), [hybridse::vm::ErrorTableHandler::GetCount](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_error_table_handler.md#function-getcount)


It count element by traverse the list 


#### At

```cpp
inline virtual V At(
    uint64_t pos
)
```

Return a the value of element by its position in the list. 

**Parameters**: 

  * **pos** is element position in the list 


**Reimplemented by**: [hybridse::vm::ErrorTableHandler::At](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_error_table_handler.md#function-at), [hybridse::vm::PartitionHandler::At](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_partition_handler.md#function-at), [hybridse::vm::MemTableHandler::At](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_table_handler.md#function-at), [hybridse::vm::MemTimeTableHandler::At](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md#function-at), [hybridse::vm::Window::At](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_window.md#function-at), [hybridse::vm::RowHandler::At](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_row_handler.md#function-at), [hybridse::vm::MemSegmentHandler::At](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_segment_handler.md#function-at), [hybridse::vm::ConcatTableHandler::At](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_concat_table_handler.md#function-at)


-------------------------------

Updated on 29 March 2021 at 17:34:52 PDT