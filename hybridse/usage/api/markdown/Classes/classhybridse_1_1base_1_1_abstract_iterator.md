---
title: hybridse::base::AbstractIterator
summary: An iterator over a key-value pairs dataset. 

---

# hybridse::base::AbstractIterator



An iterator over a key-value pairs dataset.  [More...](#detailed-description)


`#include <iterator.h>`

## Public Functions

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

We use the `Valid` and `[Next()](/hybridse/usage/api/markdown/Classes/classhybridse_1_1base_1_1_abstract_iterator.md#function-next)` functions to manually iterate through all the items of an iterator. When we reach the end and the `Valid` will return `false`



```cpp
// assume we have got and initialized an row iterator already
while (iterator->Valid()) {
    auto &value = iterator->GetValue();
    auto &key = iterator->GetKey();
    iterator->Next();
}
```

## Public Functions Documentation

### function AbstractIterator

```cpp
inline AbstractIterator()
```


### function AbstractIterator

```cpp
AbstractIterator(
    const AbstractIterator & 
)
```


### function operator=

```cpp
AbstractIterator & operator=(
    const AbstractIterator & 
)
```


### function ~AbstractIterator

```cpp
inline virtual ~AbstractIterator()
```


### function Valid

```cpp
virtual bool Valid() const =0
```


Implemented by subclasses to return whether the iteration has elements or not. 


### function Next

```cpp
virtual void Next() =0
```


Implemented by subclasses to move to the next element in the iteration when `[Valid()](/hybridse/usage/api/markdown/Classes/classhybridse_1_1base_1_1_abstract_iterator.md#function-valid)` return `true`. 


### function GetKey

```cpp
virtual const K & GetKey() const =0
```

Implemented by subclasses to return the key of current element pair. 

### function GetValue

```cpp
virtual Ref GetValue() =0
```


**Return**: 

Implemented by subclasses to return the value of current element pari when `[Valid()](/hybridse/usage/api/markdown/Classes/classhybridse_1_1base_1_1_abstract_iterator.md#function-valid)` return `true`. 


### function IsSeekable

```cpp
virtual bool IsSeekable() const =0
```


**Return**: 

Implemented by subclasses to return whether the dataset is seekable or not. A dataset is seekable if it allows access to data with `[Seek()](/hybridse/usage/api/markdown/Classes/classhybridse_1_1base_1_1_abstract_iterator.md#function-seek)` method 


### function Seek

```cpp
virtual void Seek(
    const K & k
) =0
```


Implemented by subclasses to set the dataset's current position move to the first element whose key equals to `k` offset. 


### function SeekToFirst

```cpp
virtual void SeekToFirst() =0
```

Implemented by subclasses to seek to the beginning of the dataset. 

-------------------------------

Updated on 29 March 2021 at 10:12:21 PDT