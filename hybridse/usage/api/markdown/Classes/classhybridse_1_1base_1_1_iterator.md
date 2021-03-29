---
title: hybridse::base::Iterator
summary: An iterator over a key-value pairs dataset. 

---

# hybridse::base::Iterator



An iterator over a key-value pairs dataset.  [More...](#detailed-description)


`#include <iterator.h>`

Inherits from [hybridse::base::AbstractIterator< K, V, V & >](/hybridse/usage/api/markdown/Classes/classhybridse_1_1base_1_1_abstract_iterator.md)

## Additional inherited members

**Public Functions inherited from [hybridse::base::AbstractIterator< K, V, V & >](/hybridse/usage/api/markdown/Classes/classhybridse_1_1base_1_1_abstract_iterator.md)**

|                | Name           |
| -------------- | -------------- |
| | **[AbstractIterator](/hybridse/usage/api/markdown/Classes/classhybridse_1_1base_1_1_abstract_iterator.md#function-abstractiterator)**() |
| | **[AbstractIterator](/hybridse/usage/api/markdown/Classes/classhybridse_1_1base_1_1_abstract_iterator.md#function-abstractiterator)**(const [AbstractIterator](/hybridse/usage/api/markdown/Classes/classhybridse_1_1base_1_1_abstract_iterator.md) & ) |
| [AbstractIterator](/hybridse/usage/api/markdown/Classes/classhybridse_1_1base_1_1_abstract_iterator.md) & | **[operator=](/hybridse/usage/api/markdown/Classes/classhybridse_1_1base_1_1_abstract_iterator.md#function-operator=)**(const [AbstractIterator](/hybridse/usage/api/markdown/Classes/classhybridse_1_1base_1_1_abstract_iterator.md) & ) |
| virtual | **[~AbstractIterator](/hybridse/usage/api/markdown/Classes/classhybridse_1_1base_1_1_abstract_iterator.md#function-~abstractiterator)**() |
| virtual bool | **[Valid](/hybridse/usage/api/markdown/Classes/classhybridse_1_1base_1_1_abstract_iterator.md#function-valid)**() const =0 |
| virtual void | **[Next](/hybridse/usage/api/markdown/Classes/classhybridse_1_1base_1_1_abstract_iterator.md#function-next)**() =0 |
| virtual const K & | **[GetKey](/hybridse/usage/api/markdown/Classes/classhybridse_1_1base_1_1_abstract_iterator.md#function-getkey)**() const =0<br>Implemented by subclasses to return the key of current element pair.  |
| virtual Ref | **[GetValue](/hybridse/usage/api/markdown/Classes/classhybridse_1_1base_1_1_abstract_iterator.md#function-getvalue)**() =0 |
| virtual bool | **[IsSeekable](/hybridse/usage/api/markdown/Classes/classhybridse_1_1base_1_1_abstract_iterator.md#function-isseekable)**() const =0 |
| virtual void | **[Seek](/hybridse/usage/api/markdown/Classes/classhybridse_1_1base_1_1_abstract_iterator.md#function-seek)**(const K & k) =0 |
| virtual void | **[SeekToFirst](/hybridse/usage/api/markdown/Classes/classhybridse_1_1base_1_1_abstract_iterator.md#function-seektofirst)**() =0<br>Implemented by subclasses to seek to the beginning of the dataset.  |


## Detailed Description

```cpp
template <class K ,
class V >
class hybridse::base::Iterator;
```

An iterator over a key-value pairs dataset. 

**Template Parameters**: 

  * **K** key type of elements 
  * **V** value type of elements 

-------------------------------

Updated on 29 March 2021 at 10:12:21 PDT