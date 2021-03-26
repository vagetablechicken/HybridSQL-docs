# RowIterator

`#include<codec/list_iterator_codec.h>`

## Summary

`RowIterator` is the base class provided to simplify definitions of the required types for `Row` iterators. 

Internally, each` RowIterator` is characterized by properties as followed:

| Constructors and Destructors    |
| :------------------------------ |
| [ConstIterator](#ConstIterator) |

| Public functions            | Return type     |
| :-------------------------- | --------------- |
| [Valid](#Valid)             | `const bool`    |
| [Next](#Next)               | `void`          |
| [GetKey](#GetKey)           | `const uint64&` |
| [GetValue](#GetValue)       | `const Row&`    |
| [Seek](#Seek)               | `void`          |
| [SeekToFirst](#SeekToFirst) | `void`          |
| [IsSeekable](#IsSeekable)   | `const bool`    |

## Public functions

#### Valid

```c++
bool Valid() const = 0;
```

Implemented by subclasses to return  if the iteration has elements or not.

#### Next

```c++
void Next()
```

Implemented by subclasses to move to the next element in the iteration if `Valid()` return `true`.

#### GetValue

```c++
const Row& GetValue()
```

Implemented by subclasses to return the current element if `Valid()` return `true`.

**Notes**

> We use the `Valid` and  `Next()` functions to manually iterate through all the items of an iterator. When we reach the end and the `Valid` will return `false`
>
> ```c++
> // assume we have got and initialized an row iterator already
> while (iterator->Valid()) {
>   auto &value = iterator->GetValue();
>   auto &key = iterator->GetKey();
>   iterator->Next();
> }
> ```

#### IsSeekable

```c++
bool IsSeekable() const 
```

Implemented by subclasses to return whether the dataset is seekable or not. A dataset is seekable if it allows access to data with `Seek()` method

#### Seek

```c++
void Seek(const uint64& offset)
```

Implemented by subclasses  to set the dataset's current position at the offset.

#### SeekToFirst

```c++
void SeekToFirst()
```

Implemented by subclasses to seek to the beginning of the dataset.

## Example

### MemTimeTableIterator

The following example shows how to implement simple memory table iterator by inheriting `RowIterator`

- Implement constructor by initialize schema and  `MemTimeTable` . 

```c++
MemTimeTableIterator::MemTimeTableIterator(const MemTimeTable* table,
                                           const vm::Schema* schema)
    : table_(table),
      schema_(schema),
      start_iter_(table->cbegin()),
      end_iter_(table->cend()),
      iter_(table->cbegin()) {}
```

- Implement basic operation of  `Iterator`

```c++
void MemTimeTableIterator::Seek(const uint64_t& ts) {
    iter_ = start_iter_;
    while (iter_ != end_iter_) {
        if (iter_->first <= ts) {
            return;
        }
        iter_++;
    }
}
void MemTimeTableIterator::SeekToFirst() { iter_ = start_iter_; }
const uint64_t& MemTimeTableIterator::GetKey() const { return iter_->first; }
const Row& hybridse::vm::MemTimeTableIterator::GetValue() {
    return iter_->second;
}
void MemTimeTableIterator::Next() { iter_++; }
bool MemTimeTableIterator::Valid() const { return end_iter_ > iter_; }
bool MemTimeTableIterator::IsSeekable() const { return true; }
const Row MemWindowIterator::GetKey() { return Row(iter_->first); }
```

