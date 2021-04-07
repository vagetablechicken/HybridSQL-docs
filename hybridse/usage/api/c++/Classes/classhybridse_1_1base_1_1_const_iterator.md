---
title: hybridse::base::ConstIterator
summary: An const iterator over a key-value pairs dataset. 

---
# hybridse::base::ConstIterator



`#include <iterator.h>`

An const iterator over a key-value pairs dataset. 
## Summary

```cpp
template <class K ,
class V >
class hybridse::base::ConstIterator;
```
An const iterator over a key-value pairs dataset. 

**Template Parameters**: 

  * **K** key type of elements 
  * **V** value type of elements 

## Inherited members

Inherited from [hybridse::base::AbstractIterator< K, V, const V & >](/hybridse/usage/api/c++/Classes/classhybridse_1_1base_1_1_abstract_iterator.md)

|  Inherited Public functions|            |
| -------------- | -------------- |
|**[AbstractIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1base_1_1_abstract_iterator.md#function-abstractiterator)**()|  |
|**[AbstractIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1base_1_1_abstract_iterator.md#function-abstractiterator)**(const [AbstractIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1base_1_1_abstract_iterator.md) & )|  |
|**[operator=](/hybridse/usage/api/c++/Classes/classhybridse_1_1base_1_1_abstract_iterator.md#function-operator=)**(const [AbstractIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1base_1_1_abstract_iterator.md) & )| [AbstractIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1base_1_1_abstract_iterator.md) &  |
|**[~AbstractIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1base_1_1_abstract_iterator.md#function-~abstractiterator)**()|  |
|**[Valid](/hybridse/usage/api/c++/Classes/classhybridse_1_1base_1_1_abstract_iterator.md#function-valid)**() const =0| bool  |
|**[Next](/hybridse/usage/api/c++/Classes/classhybridse_1_1base_1_1_abstract_iterator.md#function-next)**() =0| void  |
|**[GetKey](/hybridse/usage/api/c++/Classes/classhybridse_1_1base_1_1_abstract_iterator.md#function-getkey)**() const =0| const K & <br>Return the key of current element pair.  |
|**[GetValue](/hybridse/usage/api/c++/Classes/classhybridse_1_1base_1_1_abstract_iterator.md#function-getvalue)**() =0| Ref  |
|**[IsSeekable](/hybridse/usage/api/c++/Classes/classhybridse_1_1base_1_1_abstract_iterator.md#function-isseekable)**() const =0| bool  |
|**[Seek](/hybridse/usage/api/c++/Classes/classhybridse_1_1base_1_1_abstract_iterator.md#function-seek)**(const K & k) =0| void  |
|**[SeekToFirst](/hybridse/usage/api/c++/Classes/classhybridse_1_1base_1_1_abstract_iterator.md#function-seektofirst)**() =0| void <br>Move to the beginning of the dataset.  |


