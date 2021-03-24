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

Return `true`  if the iteration has elements.

#### Next

```c++
void Next()
```

Move to the next element in the iteration if `Valid()` return `true`.

#### GetValue

```c++
const Row& GetValue()
```

Return the current element if `Valid()` return `true`.

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

Return true if the dataset is seekable. A dataset is seekable if it allows access to data with `Seek()` method

#### Seek

```c++
void Seek(const uint64& offset)
```

Method **Seek()** sets the dataset's current position at the offse.

#### SeekToFirst

```c++
void SeekToFirst()
```

Method **SeekToFirst()** seek to the beginning of the dataset.

### Example

The following example shows how to implement simple memory table iterator by inheriting from `RowIterator`

```c++
typedef std::deque<std::pair<uint64_t, Row>> MemTimeTable;

class MemTimeTableIterator : public RowIterator {
 public:
    MemTimeTableIterator(const MemTimeTable* table, const vm::Schema* schema);
    ~MemTimeTableIterator();
    void Seek(const uint64_t& ts);
    void SeekToFirst();
    const uint64_t& GetKey() const;
    void Next();
    bool Valid() const;
    const Row& GetValue() override;
    bool IsSeekable() const override;

 private:
    const MemTimeTable* table_;
    const Schema* schema_;
    const MemTimeTable::const_iterator start_iter_;
    const MemTimeTable::const_iterator end_iter_;
    MemTimeTable::const_iterator iter_;
};

MemTimeTableIterator::MemTimeTableIterator(const MemTimeTable* table,
                                           const vm::Schema* schema)
    : table_(table),
      schema_(schema),
      start_iter_(table->cbegin()),
      end_iter_(table->cend()),
      iter_(table->cbegin()) {}
MemTimeTableIterator::~MemTimeTableIterator() {}

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
```



