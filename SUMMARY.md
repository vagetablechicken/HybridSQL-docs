# Summary

* [首页](README.md)
* HybridSE
    * [介绍](hybridse/introduction/README.md)
    * 使用文档
        * [快速开始](hybridse/usage/quick_start.md)
        * [ToyDB使用手册](hybridse/usage/toydb_usage/toydb_quickstart.md)
        * [实现一个简单SQL引擎](hybridse/usage/simple_engine_demo.md)
        * SQL语法手册
            * [语言结构](hybridse/language_guide/lexical.md)
            * [表达式，函数和运算](hybridse/language_guide/expressions_functions_and_operators.md)
            * [数据类型](hybridse/language_guide//data_types.md)
            * [数据查询语句(DQL)](hybridse/language_guide/query.md)
            * [数据操作语句(DML)](hybridse/language_guide/dml.md)
            * [数据定义语句(DDL)](hybridse/language_guide/ddl.md)
        * C++ API文档
            * [Classes](hybridse/usage/api/c++/Classes/README.md)

              * **namespace [hybridse](/hybridse/usage/api/c++/Namespaces/namespacehybridse.md)** 
                * **namespace [base](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1base.md)** 
                  * **class [AbstractIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1base_1_1_abstract_iterator.md)** <br>An iterator over a key-value pairs dataset. 
                  * **class [ConstIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1base_1_1_const_iterator.md)** <br>An const iterator over a key-value pairs dataset. 
                  * **struct [DefaultComparator](/hybridse/usage/api/c++/Classes/structhybridse_1_1base_1_1_default_comparator.md)** 
                  * **class [Iterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1base_1_1_iterator.md)** <br>An iterator over a key-value pairs dataset. 
                * **namespace [codec](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1codec.md)** 
                  * **struct [ColInfo](/hybridse/usage/api/c++/Classes/structhybridse_1_1codec_1_1_col_info.md)** 
                  * **class [ListV](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_list_v.md)** <br>Basic key-value list of HybridSe. 
                  * **class [Row](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row.md)** 
                  * **class [RowBuilder](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row_builder.md)** 
                  * **class [RowFormat](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row_format.md)** 
                  * **class [RowSelector](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row_selector.md)** 
                  * **class [RowView](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row_view.md)** 
                  * **class [SchemaCodec](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_schema_codec.md)** 
                  * **struct [StringColInfo](/hybridse/usage/api/c++/Classes/structhybridse_1_1codec_1_1_string_col_info.md)** 
                  * **class [WindowIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_window_iterator.md)** <br>A iterator over a Row-Iterator<[codec::Row](/hybridse/usage/api/c++/Classes/classhybridse_1_1codec_1_1_row.md)> pairs dataset. 
                * **namespace [vm](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md)** 
                  * **struct [AscComparor](/hybridse/usage/api/c++/Classes/structhybridse_1_1vm_1_1_asc_comparor.md)** 
                  * **struct [AscKeyComparor](/hybridse/usage/api/c++/Classes/structhybridse_1_1vm_1_1_asc_key_comparor.md)** 
                  * **class [AysncRowHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_aysnc_row_handler.md)** <br>A wrapper of table handler which is used as a asynchronous row handler. 
                  * **struct [BatchRequestInfo](/hybridse/usage/api/c++/Classes/structhybridse_1_1vm_1_1_batch_request_info.md)** 
                  * **class [BatchRequestRunSession](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_batch_request_run_session.md)** 
                  * **class [BatchRunSession](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_batch_run_session.md)** 
                  * **class [Catalog](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_catalog.md)** <br>A [Catalog]() handler which defines a set of operation for, e.g, database, table and index management. 
                  * **class [CompileInfo](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_compile_info.md)** 
                  * **class [CompileInfoCache](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_compile_info_cache.md)** 
                  * **class [ConcatTableHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_concat_table_handler.md)** 
                  * **class [CurrentHistoryWindow](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_current_history_window.md)** 
                  * **class [DataHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md)** <br>The basic dataset operation abstraction. 
                  * **class [DataHandlerList](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler_list.md)** <br>A sequence of [DataHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler.md). 
                  * **class [DataHandlerRepeater](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler_repeater.md)** <br>A implementation of [DataHandlerList](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler_list.md). 
                  * **class [DataHandlerVector](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler_vector.md)** <br>A implementation of [DataHandlerList](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_data_handler_list.md). 
                  * **struct [DescComparor](/hybridse/usage/api/c++/Classes/structhybridse_1_1vm_1_1_desc_comparor.md)** 
                  * **class [Engine](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_engine.md)** 
                  * **class [EngineOptions](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_engine_options.md)** 
                  * **class [ErrorRowHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_error_row_handler.md)** <br>A row's error handler, representing a error row. 
                  * **class [ErrorTableHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_error_table_handler.md)** <br>A table dataset's error handler, representing a error table. 
                  * **struct [ExplainOutput](/hybridse/usage/api/c++/Classes/structhybridse_1_1vm_1_1_explain_output.md)** 
                  * **class [HistoryWindow](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_history_window.md)** 
                  * **struct [IndexSt](/hybridse/usage/api/c++/Classes/structhybridse_1_1vm_1_1_index_st.md)** 
                  * **class [JitOptions](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_jit_options.md)** 
                  * **class [LocalTablet](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_local_tablet.md)** 
                  * **class [MemCatalog](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_catalog.md)** 
                  * **class [MemPartitionHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_partition_handler.md)** 
                  * **class [MemRowHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_row_handler.md)** 
                  * **class [MemSegmentHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_segment_handler.md)** 
                  * **class [MemTableHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_table_handler.md)** 
                  * **class [MemTableIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_table_iterator.md)** 
                  * **class [MemTimeTableHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_handler.md)** 
                  * **class [MemTimeTableIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_time_table_iterator.md)** 
                  * **class [MemWindowIterator](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_mem_window_iterator.md)** 
                  * **class [PartitionHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_partition_handler.md)** <br>The abstraction of partition dataset operation. 
                  * **class [RequestRunSession](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_request_run_session.md)** 
                  * **class [RequestUnionTableHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_request_union_table_handler.md)** 
                  * **class [Router](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_router.md)** 
                  * **class [RowHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_row_handler.md)** <br>A row operation abstraction. 
                  * **class [RunSession](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_run_session.md)** 
                  * **class [SchemaSource](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_schema_source.md)** 
                  * **class [SchemasContext](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_schemas_context.md)** 
                  * **class [TableHandler](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_table_handler.md)** <br>A table dataset operation abstraction. 
                  * **class [Tablet](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_tablet.md)** <br>A component responsible to Query subtask. 
                  * **class [Window](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_window.md)** 
                  * **class [WindowRange](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_window_range.md)** 
              * **struct [represents](/hybridse/usage/api/c++/Classes/structrepresents.md)**

            * [Namespaces](hybridse/usage/api/c++/Namespaces/README.md)
              * **namespace [hybridse](/hybridse/usage/api/c++/Namespaces/namespacehybridse.md)** 
              * **namespace [base](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1base.md)** 
              * **namespace [codec](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1codec.md)** 
              * **namespace [vm](/hybridse/usage/api/c++/Namespaces/namespacehybridse_1_1vm.md)** 
* FEDB
    * [介绍](fedb/README.md)
    * 使用文档
        * [部署](fedb/usage/fedb_deploy.md)
* NativeSpark
    * [介绍](nativespark/introduction/README.md)
    * 使用文档
        * [使用教程](nativespark/usage/usage.md)
        * [Java接口](nativespark/usage/java_api.md)
        * [从源码构建](nativespark/usage/build_from_scratch.md)
    * [性能测试](nativespark/benchmark/README.md)
    * [常见问题](nativespark/faq.md)
* [项目贡献](contribution/README.md)

