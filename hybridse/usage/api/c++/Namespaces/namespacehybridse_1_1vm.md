---
title: hybridse::vm

---
# hybridse::vm

## Classes

|                | Name           |
| -------------- | -------------- |
| struct | **[hybridse::vm::AscComparor](/hybridse/usage/api/c++/Classes/structhybridse_1_1vm_1_1_asc_comparor.md)**  |
| struct | **[hybridse::vm::AscKeyComparor](/hybridse/usage/api/c++/Classes/structhybridse_1_1vm_1_1_asc_key_comparor.md)**  |
| class | **[hybridse::vm::AysncRowHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_aysnc_row_handler.md)** <br>A wrapper of table handler which is used as a asynchronous row handler.  |
| struct | **[hybridse::vm::BatchRequestInfo](/hybridse/usage/api/c++/Classes/structhybridse_1_1vm_1_1_batch_request_info.md)**  |
| class | **[hybridse::vm::BatchRequestRunSession](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_batch_request_run_session.md)** <br>[BatchRequestRunSession]() is a kind of [RunSession]() designed for batch request mode query.  |
| class | **[hybridse::vm::BatchRunSession](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_batch_run_session.md)** <br>[BatchRunSession]() is a kind of [RunSession]() designed for batch mode query.  |
| class | **[hybridse::vm::Catalog](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_catalog.md)** <br>A [Catalog]() handler which defines a set of operation for, e.g, database, table and index management.  |
| class | **[hybridse::vm::CompileInfo](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_compile_info.md)**  |
| class | **[hybridse::vm::CompileInfoCache](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_compile_info_cache.md)**  |
| class | **[hybridse::vm::ConcatTableHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_concat_table_handler.md)**  |
| class | **[hybridse::vm::CurrentHistoryWindow](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_current_history_window.md)**  |
| class | **[hybridse::vm::DataHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md)** <br>The basic dataset operation abstraction.  |
| class | **[hybridse::vm::DataHandlerList](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler_list.md)** <br>A sequence of [DataHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md).  |
| class | **[hybridse::vm::DataHandlerRepeater](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler_repeater.md)** <br>A implementation of [DataHandlerList](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler_list.md).  |
| class | **[hybridse::vm::DataHandlerVector](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler_vector.md)** <br>A implementation of [DataHandlerList](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler_list.md).  |
| struct | **[hybridse::vm::DescComparor](/hybridse/usage/api/c++/Classes/structhybridse_1_1vm_1_1_desc_comparor.md)**  |
| class | **[hybridse::vm::Engine](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_engine.md)** <br>An engine is responsible to compile SQL on the specific [Catalog](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_catalog.md).  |
| class | **[hybridse::vm::EngineOptions](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_engine_options.md)** <br>An options class for controlling engine behaviour.  |
| class | **[hybridse::vm::ErrorRowHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_error_row_handler.md)** <br>A row's error handler, representing a error row.  |
| class | **[hybridse::vm::ErrorTableHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_error_table_handler.md)** <br>A table dataset's error handler, representing a error table.  |
| struct | **[hybridse::vm::ExplainOutput](/hybridse/usage/api/c++/Classes/structhybridse_1_1vm_1_1_explain_output.md)** <br>An options class for controlling runtime interpreter behavior.  |
| class | **[hybridse::vm::HistoryWindow](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_history_window.md)**  |
| struct | **[hybridse::vm::IndexSt](/hybridse/usage/api/c++/Classes/structhybridse_1_1vm_1_1_index_st.md)**  |
| class | **[hybridse::vm::JitOptions](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_jit_options.md)**  |
| class | **[hybridse::vm::LocalTablet](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_local_tablet.md)** <br>Local tablet is responsible to run a task locally.  |
| class | **[hybridse::vm::MemCatalog](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_catalog.md)**  |
| class | **[hybridse::vm::MemPartitionHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_partition_handler.md)**  |
| class | **[hybridse::vm::MemRowHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_row_handler.md)**  |
| class | **[hybridse::vm::MemSegmentHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_segment_handler.md)**  |
| class | **[hybridse::vm::MemTableHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_table_handler.md)**  |
| class | **[hybridse::vm::MemTableIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_table_iterator.md)**  |
| class | **[hybridse::vm::MemTimeTableHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md)**  |
| class | **[hybridse::vm::MemTimeTableIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_iterator.md)**  |
| class | **[hybridse::vm::MemWindowIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_window_iterator.md)**  |
| class | **[hybridse::vm::PartitionHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_partition_handler.md)** <br>The abstraction of partition dataset operation.  |
| class | **[hybridse::vm::RequestRunSession](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_request_run_session.md)** <br>[RequestRunSession]() is a kind of [RunSession]() designed for request mode query.  |
| class | **[hybridse::vm::RequestUnionTableHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_request_union_table_handler.md)**  |
| class | **[hybridse::vm::Router](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_router.md)**  |
| class | **[hybridse::vm::RowHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_row_handler.md)** <br>A row operation abstraction.  |
| class | **[hybridse::vm::RunSession](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_run_session.md)** <br>A [RunSession]() maintain SQL running context, including compile information, procedure name.  |
| class | **[hybridse::vm::SchemasContext](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_schemas_context.md)**  |
| class | **[hybridse::vm::SchemaSource](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_schema_source.md)**  |
| class | **[hybridse::vm::TableHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md)** <br>A table dataset operation abstraction.  |
| class | **[hybridse::vm::Tablet](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_tablet.md)** <br>A component responsible to Query subtask.  |
| class | **[hybridse::vm::Window](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_window.md)**  |
| class | **[hybridse::vm::WindowRange](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_window_range.md)**  |

## Types

|                | Name           |
| -------------- | -------------- |
| enum| **[HandlerType](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#enum-handlertype)** { kRowHandler, kTableHandler, kPartitionHandler} |
| enum| **[OrderType](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#enum-ordertype)** { kDescOrder, kAscOrder, kNoneOrder} |
| enum| **[EngineMode](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#enum-enginemode)** { kBatchMode, kRequestMode, kBatchRequestMode} |
| enum| **[ComileType](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#enum-comiletype)** { kCompileSql} |
| typedef ::google::protobuf::RepeatedPtrField<::hybridse::type::IndexDef > | **[IndexList](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#typedef-indexlist)**  |
| typedef std::map< std::string, [ColInfo](/hybridse/usage/api/c++/Classes/structhybridse_1_1codec_1_1_col_info.md) > | **[Types](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#typedef-types)**  |
| typedef std::map< std::string, [IndexSt](/hybridse/usage/api/c++/Classes/structhybridse_1_1vm_1_1_index_st.md) > | **[IndexHint](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#typedef-indexhint)**  |
| typedef std::map< [EngineMode](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#enum-enginemode), std::map< std::string, boost::compute::detail::lru_cache< std::string, std::shared_ptr< [CompileInfo](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_compile_info.md) > > > > | **[EngineLRUCache](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#typedef-enginelrucache)**  |
| typedef std::deque< std::pair< uint64_t, [Row](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row.md) > > | **[MemTimeTable](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#typedef-memtimetable)**  |
| typedef std::vector< [Row](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row.md) > | **[MemTable](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#typedef-memtable)**  |
| typedef std::map< std::string, [MemTimeTable](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#typedef-memtimetable), std::greater< std::string > > | **[MemSegmentMap](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#typedef-memsegmentmap)**  |
| typedef std::map< std::string, std::map< std::string, std::shared_ptr< [MemTimeTableHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md) > > > | **[MemTables](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#typedef-memtables)**  |
| typedef std::map< std::string, std::shared_ptr< type::Database > > | **[Databases](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#typedef-databases)**  |

## Functions

|                | Name           |
| -------------- | -------------- |
| std::string | **[EngineModeName](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#function-enginemodename)**([EngineMode](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#enum-enginemode) mode) |
| void | **[GetRowIter](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#function-getrowiter)**(int8_t * input, int8_t * iter) |
| bool | **[RowIterHasNext](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#function-rowiterhasnext)**(int8_t * iter) |
| void | **[RowIterNext](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#function-rowiternext)**(int8_t * iter) |
| int8_t * | **[RowIterGetCurSlice](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#function-rowitergetcurslice)**(int8_t * iter, size_t idx) |
| size_t | **[RowIterGetCurSliceSize](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#function-rowitergetcurslicesize)**(int8_t * iter, size_t idx) |
| void | **[RowIterDelete](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#function-rowiterdelete)**(int8_t * iter) |
| int8_t * | **[RowGetSlice](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#function-rowgetslice)**(int8_t * row_ptr, size_t idx) |
| size_t | **[RowGetSliceSize](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#function-rowgetslicesize)**(int8_t * row_ptr, size_t idx) |

## Attributes

|                | Name           |
| -------------- | -------------- |
| constexpr uint32_t | **[INVALID_POS](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md#variable-invalid_pos)**  |

## Types Documentation

### enum HandlerType

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| kRowHandler | |   |
| kTableHandler | |   |
| kPartitionHandler | |   |




### enum OrderType

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| kDescOrder | |   |
| kAscOrder | |   |
| kNoneOrder | |   |




### enum EngineMode

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| kBatchMode | |   |
| kRequestMode | |   |
| kBatchRequestMode | |   |




### enum ComileType

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| kCompileSql | |   |




### typedef IndexList

```cpp
typedef ::google::protobuf::RepeatedPtrField<::hybridse::type::IndexDef> hybridse::vm::IndexList;
```


### typedef Types

```cpp
typedef std::map<std::string, ColInfo> hybridse::vm::Types;
```


### typedef IndexHint

```cpp
typedef std::map<std::string, IndexSt> hybridse::vm::IndexHint;
```


### typedef EngineLRUCache

```cpp
typedef std::map< EngineMode, std::map<std::string, boost::compute::detail::lru_cache< std::string, std::shared_ptr<CompileInfo> > > > hybridse::vm::EngineLRUCache;
```


### typedef MemTimeTable

```cpp
typedef std::deque<std::pair<uint64_t, Row> > hybridse::vm::MemTimeTable;
```


### typedef MemTable

```cpp
typedef std::vector<Row> hybridse::vm::MemTable;
```


### typedef MemSegmentMap

```cpp
typedef std::map<std::string, MemTimeTable, std::greater<std::string> > hybridse::vm::MemSegmentMap;
```


### typedef MemTables

```cpp
typedef std::map<std::string, std::map<std::string, std::shared_ptr<MemTimeTableHandler> > > hybridse::vm::MemTables;
```


### typedef Databases

```cpp
typedef std::map<std::string, std::shared_ptr<type::Database> > hybridse::vm::Databases;
```



## Functions Documentation

### function EngineModeName

```cpp
std::string EngineModeName(
    EngineMode mode
)
```


### function GetRowIter

```cpp
void GetRowIter(
    int8_t * input,
    int8_t * iter
)
```


### function RowIterHasNext

```cpp
bool RowIterHasNext(
    int8_t * iter
)
```


### function RowIterNext

```cpp
void RowIterNext(
    int8_t * iter
)
```


### function RowIterGetCurSlice

```cpp
int8_t * RowIterGetCurSlice(
    int8_t * iter,
    size_t idx
)
```


### function RowIterGetCurSliceSize

```cpp
size_t RowIterGetCurSliceSize(
    int8_t * iter,
    size_t idx
)
```


### function RowIterDelete

```cpp
void RowIterDelete(
    int8_t * iter
)
```


### function RowGetSlice

```cpp
int8_t * RowGetSlice(
    int8_t * row_ptr,
    size_t idx
)
```


### function RowGetSliceSize

```cpp
size_t RowGetSliceSize(
    int8_t * row_ptr,
    size_t idx
)
```



## Attributes Documentation

### variable INVALID_POS

```cpp
constexpr uint32_t INVALID_POS = UINT32_MAX;
```





