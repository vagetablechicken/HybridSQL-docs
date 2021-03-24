# WindowIterator

`#include<codec/list_iterator_codec.h>`

## Summary

`WindowIterator` is the base class provided to simplify definitions of the required types for [RowIterator](./iterator.md#RowIterator) iterators. 

| Constructors and Destructors      |
| :-------------------------------- |
| [WindowIterator](#WindowIterator) |

| Public functions            | Return type                    |
| :-------------------------- | ------------------------------ |
| [Valid](#Valid)             | `const bool`                   |
| [Next](#Next)               | `void`                         |
| [GetKey](#GetKey)           | `const Row&`                   |
| [GetValue](#GetValue)       | `std::unique_ptr<RowIterator>` |
| [Seek](#Seek)               | `void`                         |
| [SeekToFirst](#SeekToFirst) | `void`                         |
| [IsSeekable](#IsSeekable)   | `const bool`                   |

Public functions

#### Valid

```c++
bool Valid() const = 0;
```

Return `true`  if the iteration has elements.

#### Next

```c++
void Next()
```

Move to the next segmen in the iteration if `Valid()` return `true`.

#### GetValue

```c++
std::unique_ptr<RowIterator> GetValue()
```

Return the `RowIterator` of current segment of dataset if `Valid()` return `true`.

**Notes**

> Assuming the dataset is logically organized by segments, we can use `Valid`, `Next` and `GetValue` methods to iterate these "segments" one by one. Then when it comes to segment, it's easily to access the rows with  `RowIterator` 's interfaces.
>
> ```c++
> // assume we have got and initialized an window iterator already
> // here is an example of counting segments and rows in the dataset
> size_t segment_num = 0, row_num = 0;
> while (window_iterator->Valid()) {
>   segment_num += 1;
>   auto &row_iterator = window_iterator->GetValue();
>   auto &key = window_iterator->GetKey();
>   while (row_iterator->Valid()) {
>     row_num += 1;
>     row_iterator->Next();
>   }
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

The following example shows how to implement simple memory window iterator by inheriting from `WindowIterator`

```c++
typedef std::map<std::string, MemTimeTable, std::greater<std::string>>
    MemSegmentMap;

class MemWindowIterator : public WindowIterator {
 public:
    MemWindowIterator(const MemSegmentMap* partitions, const Schema* schema);
    ~MemWindowIterator();

    void Seek(const std::string& key);
    void SeekToFirst();
    void Next();
    bool Valid();
    std::unique_ptr<RowIterator> GetValue();
    RowIterator* GetRawValue();
    const Row GetKey();

 private:
    const MemSegmentMap* partitions_;
    const Schema* schema_;
    MemSegmentMap::const_iterator iter_;
    const MemSegmentMap::const_iterator start_iter_;
    const MemSegmentMap::const_iterator end_iter_;
};
MemWindowIterator::MemWindowIterator(const MemSegmentMap* partitions,
                                     const Schema* schema)
    : WindowIterator(),
      partitions_(partitions),
      schema_(schema),
      iter_(partitions->cbegin()),
      start_iter_(partitions->cbegin()),
      end_iter_(partitions->cend()) {}
MemWindowIterator::~MemWindowIterator() {}

void MemWindowIterator::Seek(const std::string& key) {
    iter_ = partitions_->find(key);
}
void MemWindowIterator::SeekToFirst() { iter_ = start_iter_; }
void MemWindowIterator::Next() { iter_++; }
bool MemWindowIterator::Valid() { return end_iter_ != iter_; }
std::unique_ptr<RowIterator> MemWindowIterator::GetValue() {
    return std::unique_ptr<RowIterator>(
        new MemTimeTableIterator(&(iter_->second), schema_));
}
const Row MemWindowIterator::GetKey() { return Row(iter_->first); }

```

