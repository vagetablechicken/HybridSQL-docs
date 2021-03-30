---
title: hybridse::base::Iterator
summary: An iterator over a key-value pairs dataset. 

---
# hybridse::base::Iterator



`#include <iterator.h>`

An iterator over a key-value pairs dataset. 
## Summary

```cpp
template <class K ,
class V >
class hybridse::base::Iterator;
```
An iterator over a key-value pairs dataset. 

**Template Parameters**: 

  * **K** key type of elements 
  * **V** value type of elements 

## Inherited members
Inherited from [hybridse::base::AbstractIterator< K, V, V & >](/hybridse/usage/api/c++/Classes/classhybridse_1_1base_1_1_abstract_iterator.md)
| **Inherited public functions** | Name           |
| -------------- | -------------- |
|**[AbstractIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1base_1_1_abstract_iterator.md#function-abstractiterator)**()|  |
|**[AbstractIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1base_1_1_abstract_iterator.md#function-abstractiterator)**(const [AbstractIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1base_1_1_abstract_iterator.md) & )|  |
|**[operator=](/hybridse/usage/api/c++/Classes/classhybridse_1_1base_1_1_abstract_iterator.md#function-operator=)**(const [AbstractIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1base_1_1_abstract_iterator.md) & )| [AbstractIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1base_1_1_abstract_iterator.md) &  |
|**[~AbstractIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1base_1_1_abstract_iterator.md#function-~abstractiterator)**()| virtual  |
|**[Valid](/hybridse/usage/api/c++/Classes/classhybridse_1_1base_1_1_abstract_iterator.md#function-valid)**() const =0| virtual bool  |
|**[Next](/hybridse/usage/api/c++/Classes/classhybridse_1_1base_1_1_abstract_iterator.md#function-next)**() =0| virtual void  |
|**[GetKey](/hybridse/usage/api/c++/Classes/classhybridse_1_1base_1_1_abstract_iterator.md#function-getkey)**() const =0| virtual const K & <br>Return the key of current element pair.  |
|**[GetValue](/hybridse/usage/api/c++/Classes/classhybridse_1_1base_1_1_abstract_iterator.md#function-getvalue)**() =0| virtual Ref  |
|**[IsSeekable](/hybridse/usage/api/c++/Classes/classhybridse_1_1base_1_1_abstract_iterator.md#function-isseekable)**() const =0| virtual bool  |
|**[Seek](/hybridse/usage/api/c++/Classes/classhybridse_1_1base_1_1_abstract_iterator.md#function-seek)**(const K & k) =0| virtual void  |
|**[SeekToFirst](/hybridse/usage/api/c++/Classes/classhybridse_1_1base_1_1_abstract_iterator.md#function-seektofirst)**() =0| virtual void <br>Move to the beginning of the dataset.  |


-------------------------------

Updated on 29 March 2021 at 18:02:27 PDT