---
title: hybridse::base::AbstractIterator
summary: An iterator over a key-value pairs dataset. 

---
# hybridse::base::AbstractIterator



`#include <iterator.h>`

An iterator over a key-value pairs dataset. 
## Summary

```cpp
template <class K ,
class V ,
class Ref >
class hybridse::base::AbstractIterator;
```
An iterator over a key-value pairs dataset. 

**Template Parameters**: 

  * **K** key type of elements 
  * **V** value type of elements 
  * **Ref** decorate the value returned by GetValue method, e.g, it can be const V& or V&



Example:

We use the Valid and [Next()](/hybridse/usage/api/c++/Classes/classhybridse_1_1base_1_1_abstract_iterator.md#function-next) functions to manually iterate through all the items of an iterator. When we reach the end and [Valid()](/hybridse/usage/api/c++/Classes/classhybridse_1_1base_1_1_abstract_iterator.md#function-valid) will return `false`.



```cpp
// assume we have got and initialized an row iterator already
while (iterator->Valid()) {
    auto &value = iterator->GetValue();
    auto &key = iterator->GetKey();
    iterator->Next();
}
```



|  Public functions|            |
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

## Public Functions

#### function AbstractIterator

```cpp
inline AbstractIterator()
```


#### function AbstractIterator

```cpp
AbstractIterator(
    const AbstractIterator & 
)
```


#### function operator=

```cpp
AbstractIterator & operator=(
    const AbstractIterator & 
)
```


#### function ~AbstractIterator

```cpp
inline virtual ~AbstractIterator()
```


#### function Valid

```cpp
virtual bool Valid() const =0
```


Return whether the iteration has elements or not. 


#### function Next

```cpp
virtual void Next() =0
```


Implemented by subclasses to move to the next element in the iteration when [Valid()](/hybridse/usage/api/c++/Classes/classhybridse_1_1base_1_1_abstract_iterator.md#function-valid) return `true`. 


#### function GetKey

```cpp
virtual const K & GetKey() const =0
```

Return the key of current element pair. 

#### function GetValue

```cpp
virtual Ref GetValue() =0
```


Return the value of current element pari when [Valid()](/hybridse/usage/api/c++/Classes/classhybridse_1_1base_1_1_abstract_iterator.md#function-valid) return `true`. 


#### function IsSeekable

```cpp
virtual bool IsSeekable() const =0
```


Return whether the dataset is seekable or not. A dataset is seekable if it allows access to data with [Seek()](/hybridse/usage/api/c++/Classes/classhybridse_1_1base_1_1_abstract_iterator.md#function-seek) method 


#### function Seek

```cpp
virtual void Seek(
    const K & k
) =0
```


Set the dataset's current position move to the first element whose key equals to `k` offset. 


#### function SeekToFirst

```cpp
virtual void SeekToFirst() =0
```

Move to the beginning of the dataset. 

-------------------------------

Updated on  6 April 2021 at 09:17:26 PDT