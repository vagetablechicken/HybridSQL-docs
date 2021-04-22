---
title: udfs/udfs.h

---

## Functions

|                | Name           |
| -------------- | -------------- |
| | **[abs](/hybridse/language_guide/udf/Files/udfs_8h.md#function-abs)**()<br>Return the absolute value of expr.  |
| | **[acos](/hybridse/language_guide/udf/Files/udfs_8h.md#function-acos)**()<br>Return the arc cosine of expr.  |
| | **[add](/hybridse/language_guide/udf/Files/udfs_8h.md#function-add)**() |
| | **[asin](/hybridse/language_guide/udf/Files/udfs_8h.md#function-asin)**()<br>Return the arc sine of expr.  |
| | **[at](/hybridse/language_guide/udf/Files/udfs_8h.md#function-at)**() |
| | **[atan](/hybridse/language_guide/udf/Files/udfs_8h.md#function-atan)**()<br>Return the arc tangent of expr If called with one parameter, this function returns the arc tangent of expr. If called with two parameters X and Y, this function returns the arc tangent of Y / X.  |
| | **[atan2](/hybridse/language_guide/udf/Files/udfs_8h.md#function-atan2)**()<br>Return the arc tangent of Y / X..  |
| | **[avg](/hybridse/language_guide/udf/Files/udfs_8h.md#function-avg)**()<br>Compute average of values.  |
| | **[avg_cate](/hybridse/language_guide/udf/Files/udfs_8h.md#function-avg_cate)**()<br>Compute average of values grouped by category key and output string. Each group is represented as 'K:V' and separated by comma in outputs and are sorted by key in ascend order.  |
| | **[avg_cate_where](/hybridse/language_guide/udf/Files/udfs_8h.md#function-avg_cate_where)**()<br>Compute average of values matching specified condition grouped by category key and output string. Each group is represented as 'K:V' and separated by comma in outputs and are sorted by key in ascend order.  |
| | **[avg_where](/hybridse/language_guide/udf/Files/udfs_8h.md#function-avg_where)**()<br>Compute average of values match specified condition.  |
| | **[bool](/hybridse/language_guide/udf/Files/udfs_8h.md#function-bool)**() |
| | **[ceil](/hybridse/language_guide/udf/Files/udfs_8h.md#function-ceil)**()<br>Return the smallest integer value not less than the expr.  |
| | **[ceiling](/hybridse/language_guide/udf/Files/udfs_8h.md#function-ceiling)**()<br>Return the smallest integer value not less than the expr.  |
| | **[concat](/hybridse/language_guide/udf/Files/udfs_8h.md#function-concat)**() |
| | **[concat_ws](/hybridse/language_guide/udf/Files/udfs_8h.md#function-concat_ws)**() |
| | **[cos](/hybridse/language_guide/udf/Files/udfs_8h.md#function-cos)**()<br>Return the cosine of expr.  |
| | **[cot](/hybridse/language_guide/udf/Files/udfs_8h.md#function-cot)**()<br>Return the cotangent of expr.  |
| | **[count](/hybridse/language_guide/udf/Files/udfs_8h.md#function-count)**()<br>Compute count of values.  |
| | **[count_cate](/hybridse/language_guide/udf/Files/udfs_8h.md#function-count_cate)**()<br>Compute count of values grouped by category key and output string. Each group is represented as 'K:V' and separated by comma in outputs and are sorted by key in ascend order.  |
| | **[count_cate_where](/hybridse/language_guide/udf/Files/udfs_8h.md#function-count_cate_where)**()<br>Compute count of values matching specified condition grouped by category key and output string. Each group is represented as 'K:V' and separated by comma in outputs and are sorted by key in ascend order.  |
| | **[count_where](/hybridse/language_guide/udf/Files/udfs_8h.md#function-count_where)**()<br>Compute number of values match specified condition.  |
| | **[date](/hybridse/language_guide/udf/Files/udfs_8h.md#function-date)**() |
| | **[date_format](/hybridse/language_guide/udf/Files/udfs_8h.md#function-date_format)**() |
| | **[day](/hybridse/language_guide/udf/Files/udfs_8h.md#function-day)**() |
| | **[dayofmonth](/hybridse/language_guide/udf/Files/udfs_8h.md#function-dayofmonth)**() |
| | **[dayofweek](/hybridse/language_guide/udf/Files/udfs_8h.md#function-dayofweek)**() |
| | **[distinct_count](/hybridse/language_guide/udf/Files/udfs_8h.md#function-distinct_count)**()<br>Compute distinct number of values.  |
| | **[double](/hybridse/language_guide/udf/Files/udfs_8h.md#function-double)**() |
| | **[exp](/hybridse/language_guide/udf/Files/udfs_8h.md#function-exp)**()<br>Return the value of e (the base of natural logarithms) raised to the power of expr.  |
| | **[first_value](/hybridse/language_guide/udf/Files/udfs_8h.md#function-first_value)**()<br>Returns the value of expr from the first row of the window frame.  |
| | **[float](/hybridse/language_guide/udf/Files/udfs_8h.md#function-float)**() |
| | **[floor](/hybridse/language_guide/udf/Files/udfs_8h.md#function-floor)**()<br>Return the largest integer value not less than the expr.  |
| | **[fz_join](/hybridse/language_guide/udf/Files/udfs_8h.md#function-fz_join)**() |
| | **[fz_split](/hybridse/language_guide/udf/Files/udfs_8h.md#function-fz_split)**()<br>Used by feature zero, split string to list by delimeter. Null values are skipped.  |
| | **[fz_split_by_key](/hybridse/language_guide/udf/Files/udfs_8h.md#function-fz_split_by_key)**()<br>Used by feature zero, split string by delimeter and then split each segment as kv pair, then add each key to output list. Null and illegal segments are skipped.  |
| | **[fz_split_by_value](/hybridse/language_guide/udf/Files/udfs_8h.md#function-fz_split_by_value)**()<br>Used by feature zero, split string by delimeter and then split each segment as kv pair, then add each value to output list. Null and illegal segments are skipped.  |
| | **[fz_top1_ratio](/hybridse/language_guide/udf/Files/udfs_8h.md#function-fz_top1_ratio)**()<br>Compute the top1 key's ratio.  |
| | **[fz_topn_frequency](/hybridse/language_guide/udf/Files/udfs_8h.md#function-fz_topn_frequency)**()<br>Return the topN keys sorted by their frequency.  |
| | **[fz_window_split](/hybridse/language_guide/udf/Files/udfs_8h.md#function-fz_window_split)**()<br>Used by feature zero, for each string value from specified column of window, split by delimeter and add segment to output list. Null values are skipped.  |
| | **[fz_window_split_by_key](/hybridse/language_guide/udf/Files/udfs_8h.md#function-fz_window_split_by_key)**()<br>Used by feature zero, for each string value from specified column of window, split by delimeter and then split each segment as kv pair, then add each key to output list. Null and illegal segments are skipped.  |
| | **[fz_window_split_by_value](/hybridse/language_guide/udf/Files/udfs_8h.md#function-fz_window_split_by_value)**()<br>Used by feature zero, for each string value from specified column of window, split by delimeter and then split each segment as kv pair, then add each value to output list. Null and illegal segments are skipped.  |
| | **[hour](/hybridse/language_guide/udf/Files/udfs_8h.md#function-hour)**() |
| | **[identity](/hybridse/language_guide/udf/Files/udfs_8h.md#function-identity)**() |
| | **[if_null](/hybridse/language_guide/udf/Files/udfs_8h.md#function-if_null)**()<br>If input is not null, return input value; else return default value.  |
| | **[ifnull](/hybridse/language_guide/udf/Files/udfs_8h.md#function-ifnull)**()<br>If input is not null, return input value; else return default value.  |
| | **[inc](/hybridse/language_guide/udf/Files/udfs_8h.md#function-inc)**() |
| | **[int16](/hybridse/language_guide/udf/Files/udfs_8h.md#function-int16)**() |
| | **[int32](/hybridse/language_guide/udf/Files/udfs_8h.md#function-int32)**() |
| | **[int64](/hybridse/language_guide/udf/Files/udfs_8h.md#function-int64)**() |
| | **[is_null](/hybridse/language_guide/udf/Files/udfs_8h.md#function-is_null)**()<br>Check if input value is null, return bool.  |
| | **[isnull](/hybridse/language_guide/udf/Files/udfs_8h.md#function-isnull)**()<br>Check if input value is null, return bool.  |
| | **[ln](/hybridse/language_guide/udf/Files/udfs_8h.md#function-ln)**()<br>Return the natural logarithm of expr.  |
| | **[log](/hybridse/language_guide/udf/Files/udfs_8h.md#function-log)**()<br>log(base, expr) If called with one parameter, this function returns the natural logarithm of expr. If called with two parameters, this function returns the logarithm of expr to the base.  |
| | **[log10](/hybridse/language_guide/udf/Files/udfs_8h.md#function-log10)**()<br>Return the base-10 logarithm of expr.  |
| | **[log2](/hybridse/language_guide/udf/Files/udfs_8h.md#function-log2)**()<br>Return the base-2 logarithm of expr.  |
| | **[make_tuple](/hybridse/language_guide/udf/Files/udfs_8h.md#function-make_tuple)**() |
| | **[max](/hybridse/language_guide/udf/Files/udfs_8h.md#function-max)**()<br>Compute max of values.  |
| | **[max_cate](/hybridse/language_guide/udf/Files/udfs_8h.md#function-max_cate)**()<br>Compute maximum of values grouped by category key and output string. Each group is represented as 'K:V' and separated by comma in outputs and are sorted by key in ascend order.  |
| | **[max_cate_where](/hybridse/language_guide/udf/Files/udfs_8h.md#function-max_cate_where)**()<br>Compute maximum of values matching specified condition grouped by category key and output string. Each group is represented as 'K:V' and separated by comma in outputs and are sorted by key in ascend order.  |
| | **[max_where](/hybridse/language_guide/udf/Files/udfs_8h.md#function-max_where)**()<br>Compute maximum of values match specified condition.  |
| | **[maximum](/hybridse/language_guide/udf/Files/udfs_8h.md#function-maximum)**() |
| | **[min](/hybridse/language_guide/udf/Files/udfs_8h.md#function-min)**()<br>Compute min of values.  |
| | **[min_cate](/hybridse/language_guide/udf/Files/udfs_8h.md#function-min_cate)**() |
| | **[min_cate_where](/hybridse/language_guide/udf/Files/udfs_8h.md#function-min_cate_where)**() |
| | **[min_where](/hybridse/language_guide/udf/Files/udfs_8h.md#function-min_where)**()<br>Compute minimum of values match specified condition.  |
| | **[minimum](/hybridse/language_guide/udf/Files/udfs_8h.md#function-minimum)**() |
| | **[minute](/hybridse/language_guide/udf/Files/udfs_8h.md#function-minute)**() |
| | **[month](/hybridse/language_guide/udf/Files/udfs_8h.md#function-month)**() |
| | **[pow](/hybridse/language_guide/udf/Files/udfs_8h.md#function-pow)**()<br>Return the value of expr1 to the power of expr2.  |
| | **[power](/hybridse/language_guide/udf/Files/udfs_8h.md#function-power)**()<br>Return the value of expr1 to the power of expr2.  |
| | **[round](/hybridse/language_guide/udf/Files/udfs_8h.md#function-round)**()<br>Return the nearest integer value to expr (in floating-point format), rounding halfway cases away from zero, regardless of the current rounding mode.  |
| | **[second](/hybridse/language_guide/udf/Files/udfs_8h.md#function-second)**() |
| | **[sin](/hybridse/language_guide/udf/Files/udfs_8h.md#function-sin)**()<br>Return the sine of expr.  |
| | **[sqrt](/hybridse/language_guide/udf/Files/udfs_8h.md#function-sqrt)**()<br>Return square root of expr.  |
| | **[strcmp](/hybridse/language_guide/udf/Files/udfs_8h.md#function-strcmp)**()<br>Returns 0 if the strings are the same, -1 if the first argument is smaller than the second according to the current sort order, and 1 otherwise.  |
| | **[string](/hybridse/language_guide/udf/Files/udfs_8h.md#function-string)**() |
| | **[substr](/hybridse/language_guide/udf/Files/udfs_8h.md#function-substr)**()<br>Return a substring from string `str` starting at position `pos`.  |
| | **[substring](/hybridse/language_guide/udf/Files/udfs_8h.md#function-substring)**()<br>Return a substring from string `str` starting at position `pos`.  |
| | **[sum](/hybridse/language_guide/udf/Files/udfs_8h.md#function-sum)**()<br>Compute sum of values.  |
| | **[sum_cate](/hybridse/language_guide/udf/Files/udfs_8h.md#function-sum_cate)**()<br>Compute sum of values grouped by category key and output string. Each group is represented as 'K:V' and separated by comma in outputs and are sorted by key in ascend order.  |
| | **[sum_cate_where](/hybridse/language_guide/udf/Files/udfs_8h.md#function-sum_cate_where)**()<br>Compute sum of values matching specified condition grouped by category key and output string. Each group is represented as 'K:V' and separated by comma in outputs and are sorted by key in ascend order.  |
| | **[sum_where](/hybridse/language_guide/udf/Files/udfs_8h.md#function-sum_where)**()<br>Compute sum of values match specified condition.  |
| | **[tan](/hybridse/language_guide/udf/Files/udfs_8h.md#function-tan)**()<br>Return the tangent of expr.  |
| | **[timestamp](/hybridse/language_guide/udf/Files/udfs_8h.md#function-timestamp)**() |
| | **[top](/hybridse/language_guide/udf/Files/udfs_8h.md#function-top)**()<br>Compute top k of values and output string separated by comma. The outputs are sorted in desc order.  |
| | **[top_n_key_avg_cate_where](/hybridse/language_guide/udf/Files/udfs_8h.md#function-top_n_key_avg_cate_where)**()<br>Compute average of values matching specified condition grouped by category key. Output string for top N keys in descend order. Each group is represented as 'K:V' and separated by comma.  |
| | **[top_n_key_count_cate_where](/hybridse/language_guide/udf/Files/udfs_8h.md#function-top_n_key_count_cate_where)**()<br>Compute count of values matching specified condition grouped by category key. Output string for top N keys in descend order. Each group is represented as 'K:V' and separated by comma.  |
| | **[top_n_key_max_cate_where](/hybridse/language_guide/udf/Files/udfs_8h.md#function-top_n_key_max_cate_where)**()<br>Compute maximum of values matching specified condition grouped by category key. Output string for top N keys in descend order. Each group is represented as 'K:V' and separated by comma.  |
| | **[top_n_key_min_cate_where](/hybridse/language_guide/udf/Files/udfs_8h.md#function-top_n_key_min_cate_where)**() |
| | **[top_n_key_sum_cate_where](/hybridse/language_guide/udf/Files/udfs_8h.md#function-top_n_key_sum_cate_where)**()<br>Compute sum of values matching specified condition grouped by category key. Output string for top N keys in descend order. Each group is represented as 'K:V' and separated by comma.  |
| | **[truncate](/hybridse/language_guide/udf/Files/udfs_8h.md#function-truncate)**()<br>Return the nearest integer that is not greater in magnitude than the expr.  |
| | **[week](/hybridse/language_guide/udf/Files/udfs_8h.md#function-week)**() |
| | **[weekofyear](/hybridse/language_guide/udf/Files/udfs_8h.md#function-weekofyear)**() |
| | **[year](/hybridse/language_guide/udf/Files/udfs_8h.md#function-year)**() |


## Functions Documentation

### function abs

```sql
abs()
```

**Description**:

Return the absolute value of expr. 

**Parameters**: 

  * **expr** 


**Since**:
0.1.0


Example:



```sql
SELECT ABS(-32);
-- output 32
```


**Supported Types**:

* [bool]
* [number] 

### function acos

```sql
acos()
```

**Description**:

Return the arc cosine of expr. 

**Parameters**: 

  * **expr** 


**Since**:
0.1.0


Example:



```sql
SELECT ACOS(1);
-- output 0
```


**Supported Types**:

* [number] 

### function add

```sql
add()
```

**Description**:


**Supported Types**:

* [bool, bool]
* [bool, number]
* [bool, timestamp]
* [int16, timestamp]
* [int32, timestamp]
* [int64, timestamp]
* [number, bool]
* [number, number]
* [timestamp, bool]
* [timestamp, int16]
* [timestamp, int32]
* [timestamp, int64]
* [timestamp, timestamp] 

### function asin

```sql
asin()
```

**Description**:

Return the arc sine of expr. 

**Parameters**: 

  * **expr** 


**Since**:
0.1.0


Example:



```sql
SELECT ASIN(0.0);
-- output 0.000000
```


**Supported Types**:

* [number] 

### function at

```sql
at()
```

**Description**:


**Supported Types**:

* [list_bool, int64]
* [list_date, int64]
* [list_number, int64]
* [list_string, int64]
* [list_timestamp, int64] 

### function atan

```sql
atan()
```

**Description**:

Return the arc tangent of expr If called with one parameter, this function returns the arc tangent of expr. If called with two parameters X and Y, this function returns the arc tangent of Y / X. 

**Parameters**: 

  * **X** 
  * **Y** 


**Since**:
0.1.0


Example:



```sql
SELECT ATAN(-0.0);  
-- output -0.000000

SELECT ATAN(0, -0);
-- output 3.141593
```


**Supported Types**:

* [bool, bool]
* [bool, number]
* [number]
* [number, bool]
* [number, number] 

### function atan2

```sql
atan2()
```

**Description**:

Return the arc tangent of Y / X.. 

**Parameters**: 

  * **X** 
  * **Y** 


**Since**:
0.1.0


Example:



```sql
SELECT ATAN2(0, -0);
-- output 3.141593
```


**Supported Types**:

* [bool, bool]
* [bool, number]
* [number, bool]
* [number, number] 

### function avg

```sql
avg()
```

**Description**:

Compute average of values. 

**Supported Types**:

* [list_number] 

### function avg_cate

```sql
avg_cate()
```

**Description**:

Compute average of values grouped by category key and output string. Each group is represented as 'K:V' and separated by comma in outputs and are sorted by key in ascend order. 

**Parameters**: 

  * **value** Specify value column to aggregate on. 
  * **catagory** Specify catagory column to group by.



Example:


| value   | catagory    |
|  -------- | -------- |
| 0   | x    |
| 1   | y    |
| 2   | x    |
| 3   | y    |
| 4   | x    |




```sql
SELECT avg_cate(value, catagory) OVER w;
-- output "x:2,y:2"
```

**Supported Types**:

* [list_number, list_date]
* [list_number, list_int16]
* [list_number, list_int32]
* [list_number, list_int64]
* [list_number, list_string]
* [list_number, list_timestamp] 

### function avg_cate_where

```sql
avg_cate_where()
```

**Description**:

Compute average of values matching specified condition grouped by category key and output string. Each group is represented as 'K:V' and separated by comma in outputs and are sorted by key in ascend order. 

**Parameters**: 

  * **catagory** Specify catagory column to group by. 
  * **value** Specify value column to aggregate on. 
  * **condition** Specify condition column.



Example:


| value   | condition   | catagory    |
|  -------- | -------- | -------- |
| 0   | true   | x    |
| 1   | false   | y    |
| 2   | false   | x    |
| 3   | true   | y    |
| 4   | true   | x    |




```sql
SELECT avg_cate_where(catagory, value, condition) OVER w;
-- output "x:2,y:3"
```

**Supported Types**:

* [list_number, list_bool, list_date]
* [list_number, list_bool, list_int16]
* [list_number, list_bool, list_int32]
* [list_number, list_bool, list_int64]
* [list_number, list_bool, list_string]
* [list_number, list_bool, list_timestamp] 

### function avg_where

```sql
avg_where()
```

**Description**:

Compute average of values match specified condition. 

**Supported Types**:

* [list_number, list_bool] 

### function bool

```sql
bool()
```

**Description**:


**Supported Types**:

* [string] 

### function ceil

```sql
ceil()
```

**Description**:

Return the smallest integer value not less than the expr. 

**Parameters**: 

  * **expr** 


**Since**:
0.1.0


Example:



```sql
SELECT CEIL(1.23);
-- output 2
```


**Supported Types**:

* [bool]
* [number] 

### function ceiling

```sql
ceiling()
```

**Description**:

Return the smallest integer value not less than the expr. 

**Parameters**: 

  * **expr** 


**Since**:
0.1.0


Example:



```sql
SELECT CEIL(1.23);
-- output 2
```


**Supported Types**:

* [bool]
* [number] 

### function concat

```sql
concat()
```

**Description**:


**Supported Types**:

* [...] 

### function concat_ws

```sql
concat_ws()
```

**Description**:


**Supported Types**:

* [bool, ...]
* [date, ...]
* [number, ...]
* [string, ...]
* [timestamp, ...] 

### function cos

```sql
cos()
```

**Description**:

Return the cosine of expr. 

**Parameters**: 

  * **expr** It is a single argument in radians.


**Since**:
0.1.0


Example:



```sql
SELECT COS(0);
-- output 1.000000
```



* The value returned by [cos()](/hybridse/language_guide/udf/Files/udfs_8h.md#function-cos) is always in the range: -1 to 1.

**Supported Types**:

* [number] 

### function cot

```sql
cot()
```

**Description**:

Return the cotangent of expr. 

**Parameters**: 

  * **expr** 


**Since**:
0.1.0


Example:



```sql
SELECT COT(1);  
-- output 0.6420926159343306
```


**Supported Types**:

* [number] 

### function count

```sql
count()
```

**Description**:

Compute count of values. 

**Supported Types**:

* [list_bool]
* [list_date]
* [list_number]
* [list_row]
* [list_string]
* [list_timestamp] 

### function count_cate

```sql
count_cate()
```

**Description**:

Compute count of values grouped by category key and output string. Each group is represented as 'K:V' and separated by comma in outputs and are sorted by key in ascend order. 

**Parameters**: 

  * **value** Specify value column to aggregate on. 
  * **catagory** Specify catagory column to group by.



Example:


| value   | catagory    |
|  -------- | -------- |
| 0   | x    |
| 1   | y    |
| 2   | x    |
| 3   | y    |
| 4   | x    |


Example:



```sql
SELECT count_cate(value, catagory) OVER w;
-- output "x:3,y:2"
```

**Supported Types**:

* [list_number, list_date]
* [list_number, list_int16]
* [list_number, list_int32]
* [list_number, list_int64]
* [list_number, list_string]
* [list_number, list_timestamp] 

### function count_cate_where

```sql
count_cate_where()
```

**Description**:

Compute count of values matching specified condition grouped by category key and output string. Each group is represented as 'K:V' and separated by comma in outputs and are sorted by key in ascend order. 

**Parameters**: 

  * **catagory** Specify catagory column to group by. 
  * **value** Specify value column to aggregate on. 
  * **condition** Specify condition column.



Example:


| value   | condition   | catagory    |
|  -------- | -------- | -------- |
| 0   | true   | x    |
| 1   | false   | y    |
| 2   | false   | x    |
| 3   | true   | y    |
| 4   | true   | x    |


Example:



```sql
SELECT count_cate_where(catagory, value, condition) OVER w;
-- output "x:2,y:1"
```

**Supported Types**:

* [list_number, list_bool, list_date]
* [list_number, list_bool, list_int16]
* [list_number, list_bool, list_int32]
* [list_number, list_bool, list_int64]
* [list_number, list_bool, list_string]
* [list_number, list_bool, list_timestamp] 

### function count_where

```sql
count_where()
```

**Description**:

Compute number of values match specified condition. 

**Supported Types**:

* [list_date, list_bool]
* [list_number, list_bool]
* [list_string, list_bool]
* [list_timestamp, list_bool] 

### function date

```sql
date()
```

**Description**:


**Supported Types**:

* [string]
* [timestamp] 

### function date_format

```sql
date_format()
```

**Description**:


**Supported Types**:

* [date, string]
* [timestamp, string] 

### function day

```sql
day()
```

**Description**:


**Supported Types**:

* [date]
* [int64]
* [timestamp] 

### function dayofmonth

```sql
dayofmonth()
```

**Description**:


**Supported Types**:

* [date]
* [int64]
* [timestamp] 

### function dayofweek

```sql
dayofweek()
```

**Description**:


**Supported Types**:

* [date]
* [int64]
* [timestamp] 

### function distinct_count

```sql
distinct_count()
```

**Description**:

Compute distinct number of values. 

**Supported Types**:

* [list_bool]
* [list_date]
* [list_number]
* [list_string]
* [list_timestamp] 

### function double

```sql
double()
```

**Description**:


**Supported Types**:

* [string] 

### function exp

```sql
exp()
```

**Description**:

Return the value of e (the base of natural logarithms) raised to the power of expr. 

**Parameters**: 

  * **expr** 


**Since**:
0.1.0




```sql
SELECT EXP(0);  
-- output 1
```


**Supported Types**:

* [number] 

### function first_value

```sql
first_value()
```

**Description**:

Returns the value of expr from the first row of the window frame. 

**Supported Types**: 

### function float

```sql
float()
```

**Description**:


**Supported Types**:

* [string] 

### function floor

```sql
floor()
```

**Description**:

Return the largest integer value not less than the expr. 

**Parameters**: 

  * **expr** 


**Since**:
0.1.0


Example:



```sql
SELECT FLOOR(1.23);
-- output 1
```


**Supported Types**:

* [bool]
* [number] 

### function fz_join

```sql
fz_join()
```

**Description**:


**Supported Types**:

* [list_string, string] 

### function fz_split

```sql
fz_split()
```

**Description**:

Used by feature zero, split string to list by delimeter. Null values are skipped. 

**Supported Types**:

* [string, string] 

### function fz_split_by_key

```sql
fz_split_by_key()
```

**Description**:

Used by feature zero, split string by delimeter and then split each segment as kv pair, then add each key to output list. Null and illegal segments are skipped. 

**Supported Types**:

* [string, string, string] 

### function fz_split_by_value

```sql
fz_split_by_value()
```

**Description**:

Used by feature zero, split string by delimeter and then split each segment as kv pair, then add each value to output list. Null and illegal segments are skipped. 

**Supported Types**:

* [string, string, string] 

### function fz_top1_ratio

```sql
fz_top1_ratio()
```

**Description**:

Compute the top1 key's ratio. 

**Supported Types**:

* [list_date]
* [list_number]
* [list_string]
* [list_timestamp] 

### function fz_topn_frequency

```sql
fz_topn_frequency()
```

**Description**:

Return the topN keys sorted by their frequency. 

**Supported Types**:

* [list_date, list_int32]
* [list_number, list_int32]
* [list_string, list_int32]
* [list_timestamp, list_int32] 

### function fz_window_split

```sql
fz_window_split()
```

**Description**:

Used by feature zero, for each string value from specified column of window, split by delimeter and add segment to output list. Null values are skipped. 

**Supported Types**:

* [list_string, list_string] 

### function fz_window_split_by_key

```sql
fz_window_split_by_key()
```

**Description**:

Used by feature zero, for each string value from specified column of window, split by delimeter and then split each segment as kv pair, then add each key to output list. Null and illegal segments are skipped. 

**Supported Types**:

* [list_string, list_string, list_string] 

### function fz_window_split_by_value

```sql
fz_window_split_by_value()
```

**Description**:

Used by feature zero, for each string value from specified column of window, split by delimeter and then split each segment as kv pair, then add each value to output list. Null and illegal segments are skipped. 

**Supported Types**:

* [list_string, list_string, list_string] 

### function hour

```sql
hour()
```

**Description**:


**Supported Types**:

* [int64]
* [timestamp] 

### function identity

```sql
identity()
```

**Description**:


**Supported Types**:

* [bool]
* [date]
* [number]
* [string]
* [timestamp] 

### function if_null

```sql
if_null()
```

**Description**:

If input is not null, return input value; else return default value. 

**Parameters**: 

  * **input** Input value 
  * **default** Default value if input is null


**Since**:
0.1.0


Example:



```sql
SELECT if_null("hello", "default"), if_null(NULL, "default");
-- output ["hello", "default"]
```


**Supported Types**:

* [bool, bool]
* [date, date]
* [double, double]
* [float, float]
* [int16, int16]
* [int32, int32]
* [int64, int64]
* [string, string]
* [timestamp, timestamp] 

### function ifnull

```sql
ifnull()
```

**Description**:

If input is not null, return input value; else return default value. 

**Parameters**: 

  * **input** Input value 
  * **default** Default value if input is null


**Since**:
0.1.0


Example:



```sql
SELECT if_null("hello", "default"), if_null(NULL, "default");
-- output ["hello", "default"]
```


**Supported Types**:

* [bool, bool]
* [date, date]
* [double, double]
* [float, float]
* [int16, int16]
* [int32, int32]
* [int64, int64]
* [string, string]
* [timestamp, timestamp] 

### function inc

```sql
inc()
```

**Description**:


**Supported Types**:

* [number] 

### function int16

```sql
int16()
```

**Description**:


**Supported Types**:

* [string] 

### function int32

```sql
int32()
```

**Description**:


**Supported Types**:

* [string] 

### function int64

```sql
int64()
```

**Description**:


**Supported Types**:

* [string] 

### function is_null

```sql
is_null()
```

**Description**:

Check if input value is null, return bool. 

**Parameters**: 

  * **input** Input value


**Since**:
0.1.0



**Supported Types**:

* [bool]
* [date]
* [number]
* [string]
* [timestamp] 

### function isnull

```sql
isnull()
```

**Description**:

Check if input value is null, return bool. 

**Parameters**: 

  * **input** Input value


**Since**:
0.1.0



**Supported Types**:

* [bool]
* [date]
* [number]
* [string]
* [timestamp] 

### function ln

```sql
ln()
```

**Description**:

Return the natural logarithm of expr. 

**Parameters**: 

  * **expr** 


**Since**:
0.1.0


Example:



```sql
SELECT LN(1);  
-- output 0.000000
```


**Supported Types**:

* [bool]
* [number] 

### function log

```sql
log()
```

**Description**:

log(base, expr) If called with one parameter, this function returns the natural logarithm of expr. If called with two parameters, this function returns the logarithm of expr to the base. 

**Parameters**: 

  * **base** 
  * **expr** 


**Since**:
0.1.0


Example:



```sql
SELECT LOG(1);  
-- output 0.000000

SELECT LOG(10,100);
-- output 2
```


**Supported Types**:

* [bool]
* [bool, bool]
* [bool, date]
* [bool, number]
* [bool, string]
* [bool, timestamp]
* [number]
* [number, bool]
* [number, date]
* [number, number]
* [number, string]
* [number, timestamp] 

### function log10

```sql
log10()
```

**Description**:

Return the base-10 logarithm of expr. 

**Parameters**: 

  * **expr** 


**Since**:
0.1.0


Example:



```sql
SELECT LOG10(100);  
-- output 2
```


**Supported Types**:

* [bool]
* [number] 

### function log2

```sql
log2()
```

**Description**:

Return the base-2 logarithm of expr. 

**Parameters**: 

  * **expr** 


**Since**:
0.1.0


Example:



```sql
SELECT LOG2(65536);  
-- output 16
```


**Supported Types**:

* [bool]
* [number] 

### function make_tuple

```sql
make_tuple()
```

**Description**:


**Supported Types**:

* [...] 

### function max

```sql
max()
```

**Description**:

Compute max of values. 

**Supported Types**:

* [list_date]
* [list_number]
* [list_string]
* [list_timestamp] 

### function max_cate

```sql
max_cate()
```

**Description**:

Compute maximum of values grouped by category key and output string. Each group is represented as 'K:V' and separated by comma in outputs and are sorted by key in ascend order. 

**Parameters**: 

  * **value** Specify value column to aggregate on. 
  * **catagory** Specify catagory column to group by.



Example:


| value   | catagory    |
|  -------- | -------- |
| 0   | x    |
| 1   | y    |
| 2   | x    |
| 3   | y    |
| 4   | x    |




```sql
SELECT max_cate(value, catagory) OVER w;
-- output "x:4,y:3"
```

**Supported Types**:

* [list_number, list_date]
* [list_number, list_int16]
* [list_number, list_int32]
* [list_number, list_int64]
* [list_number, list_string]
* [list_number, list_timestamp] 

### function max_cate_where

```sql
max_cate_where()
```

**Description**:

Compute maximum of values matching specified condition grouped by category key and output string. Each group is represented as 'K:V' and separated by comma in outputs and are sorted by key in ascend order. 

**Parameters**: 

  * **catagory** Specify catagory column to group by. 
  * **value** Specify value column to aggregate on. 
  * **condition** Specify condition column.



Example:


| value   | condition   | catagory    |
|  -------- | -------- | -------- |
| 0   | true   | x    |
| 1   | false   | y    |
| 2   | false   | x    |
| 3   | true   | y    |
| 4   | true   | x    |




```sql
SELECT max_cate_where(catagory, value, condition) OVER w;
-- output "x:4,y:3"
```

**Supported Types**:

* [list_number, list_bool, list_date]
* [list_number, list_bool, list_int16]
* [list_number, list_bool, list_int32]
* [list_number, list_bool, list_int64]
* [list_number, list_bool, list_string]
* [list_number, list_bool, list_timestamp] 

### function max_where

```sql
max_where()
```

**Description**:

Compute maximum of values match specified condition. 

**Supported Types**:

* [list_number, list_bool] 

### function maximum

```sql
maximum()
```

**Description**:


**Supported Types**:

* [bool, bool]
* [date, date]
* [double, double]
* [float, float]
* [int16, int16]
* [int32, int32]
* [int64, int64]
* [string, string]
* [timestamp, timestamp] 

### function min

```sql
min()
```

**Description**:

Compute min of values. 

**Supported Types**:

* [list_date]
* [list_number]
* [list_string]
* [list_timestamp] 

### function min_cate

```sql
min_cate()
```

**Description**:


**Parameters**: 

  * **value** Specify value column to aggregate on. 
  * **catagory** Specify catagory column to group by.


Compute minimum of values grouped by category key and output string. Each group is represented as 'K:V' and separated by comma in outputs and are sorted by key in ascend order.


Example:


| value   | catagory    |
|  -------- | -------- |
| 0   | x    |
| 1   | y    |
| 2   | x    |
| 3   | y    |
| 4   | x    |




```sql
SELECT min_cate(value, catagory) OVER w;
-- output "x:0,y:1"
```

**Supported Types**:

* [list_number, list_date]
* [list_number, list_int16]
* [list_number, list_int32]
* [list_number, list_int64]
* [list_number, list_string]
* [list_number, list_timestamp] 

### function min_cate_where

```sql
min_cate_where()
```

**Description**:


**Parameters**: 

  * **catagory** Specify catagory column to group by. 
  * **value** Specify value column to aggregate on. 
  * **condition** Specify condition column.


Compute minimum of values matching specified condition grouped by category key and output string. Each group is represented as 'K:V' and separated by comma in outputs and are sorted by key in ascend order.


Example:


| value   | condition   | catagory    |
|  -------- | -------- | -------- |
| 0   | true   | x    |
| 1   | false   | y    |
| 2   | false   | x    |
| 1   | true   | y    |
| 4   | true   | x    |
| 3   | true   | y    |




```sql
SELECT min_cate_where(catagory, value, condition) OVER w;
-- output "x:0,y:1"
```

**Supported Types**:

* [list_number, list_bool, list_date]
* [list_number, list_bool, list_int16]
* [list_number, list_bool, list_int32]
* [list_number, list_bool, list_int64]
* [list_number, list_bool, list_string]
* [list_number, list_bool, list_timestamp] 

### function min_where

```sql
min_where()
```

**Description**:

Compute minimum of values match specified condition. 

**Supported Types**:

* [list_number, list_bool] 

### function minimum

```sql
minimum()
```

**Description**:


**Supported Types**:

* [bool, bool]
* [date, date]
* [double, double]
* [float, float]
* [int16, int16]
* [int32, int32]
* [int64, int64]
* [string, string]
* [timestamp, timestamp] 

### function minute

```sql
minute()
```

**Description**:


**Supported Types**:

* [int64]
* [timestamp] 

### function month

```sql
month()
```

**Description**:


**Supported Types**:

* [date]
* [int64]
* [timestamp] 

### function pow

```sql
pow()
```

**Description**:

Return the value of expr1 to the power of expr2. 

**Parameters**: 

  * **expr1** 
  * **expr2** 


**Since**:
0.1.0


Example:



```sql
SELECT POW(2, 10);
-- output 1024.000000
```


**Supported Types**:

* [bool, bool]
* [bool, number]
* [number, bool]
* [number, number] 

### function power

```sql
power()
```

**Description**:

Return the value of expr1 to the power of expr2. 

**Parameters**: 

  * **expr1** 
  * **expr2** 


**Since**:
0.1.0


Example:



```sql
SELECT POW(2, 10);
-- output 1024.000000
```


**Supported Types**:

* [bool, bool]
* [bool, number]
* [number, bool]
* [number, number] 

### function round

```sql
round()
```

**Description**:

Return the nearest integer value to expr (in floating-point format), rounding halfway cases away from zero, regardless of the current rounding mode. 

**Parameters**: 

  * **expr** 


**Since**:
0.1.0


Example:



```sql
SELECT ROUND(1.23);
-- output 1
```


**Supported Types**:

* [bool]
* [number] 

### function second

```sql
second()
```

**Description**:


**Supported Types**:

* [int64]
* [timestamp] 

### function sin

```sql
sin()
```

**Description**:

Return the sine of expr. 

**Parameters**: 

  * **expr** It is a single argument in radians.


**Since**:
0.1.0


Example:



```sql
SELECT SIN(0);
-- output 0.000000
```



* The value returned by [sin()](/hybridse/language_guide/udf/Files/udfs_8h.md#function-sin) is always in the range: -1 to 1.

**Supported Types**:

* [number] 

### function sqrt

```sql
sqrt()
```

**Description**:

Return square root of expr. 

**Parameters**: 

  * **expr** It is a single argument in radians.


**Since**:
0.1.0


Example:



```sql
SELECT SQRT(100);
-- output 10.000000
```


**Supported Types**:

* [number] 

### function strcmp

```sql
strcmp()
```

**Description**:

Returns 0 if the strings are the same, -1 if the first argument is smaller than the second according to the current sort order, and 1 otherwise. 

**Since**:
0.1.0


Example:



```sql
select strcmp("text", "text1");
-- output -1
select strcmp("text1", "text");
-- output 1
select strcmp("text", "text");
-- output 0
```


**Supported Types**:

* [string, string] 

### function string

```sql
string()
```

**Description**:


**Supported Types**:

* [bool]
* [date]
* [number]
* [timestamp] 

### function substr

```sql
substr()
```

**Description**:

Return a substring from string `str` starting at position `pos`. 

**Parameters**: 

  * **str** 
  * **pos** define the begining of the substring.


**Since**:
0.1.0


Example: : 

```sql
select substr("hello world", 2);
-- output "llo world"
```



* If `pos` is positive, the begining of the substring is `pos` charactors from the start of string.
* If `pos` is negative, the beginning of the substring is `pos` characters from the end of the string, rather than the beginning.

**Supported Types**:

* [string, int32]
* [string, int32, int32] 

### function substring

```sql
substring()
```

**Description**:

Return a substring from string `str` starting at position `pos`. 

**Parameters**: 

  * **str** 
  * **pos** define the begining of the substring.


**Since**:
0.1.0


Example: : 

```sql
select substr("hello world", 2);
-- output "llo world"
```



* If `pos` is positive, the begining of the substring is `pos` charactors from the start of string.
* If `pos` is negative, the beginning of the substring is `pos` characters from the end of the string, rather than the beginning.

**Supported Types**:

* [string, int32]
* [string, int32, int32] 

### function sum

```sql
sum()
```

**Description**:

Compute sum of values. 

**Supported Types**:

* [list_number]
* [list_timestamp] 

### function sum_cate

```sql
sum_cate()
```

**Description**:

Compute sum of values grouped by category key and output string. Each group is represented as 'K:V' and separated by comma in outputs and are sorted by key in ascend order. 

**Parameters**: 

  * **value** Specify value column to aggregate on. 
  * **catagory** Specify catagory column to group by.



Example:


| value   | catagory    |
|  -------- | -------- |
| 0   | x    |
| 1   | y    |
| 2   | x    |
| 3   | y    |
| 4   | x    |




```sql
SELECT sum_cate(value, catagory) OVER w;
-- output "x:6,y:4"
```

**Supported Types**:

* [list_number, list_date]
* [list_number, list_int16]
* [list_number, list_int32]
* [list_number, list_int64]
* [list_number, list_string]
* [list_number, list_timestamp] 

### function sum_cate_where

```sql
sum_cate_where()
```

**Description**:

Compute sum of values matching specified condition grouped by category key and output string. Each group is represented as 'K:V' and separated by comma in outputs and are sorted by key in ascend order. 

**Parameters**: 

  * **catagory** Specify catagory column to group by. 
  * **value** Specify value column to aggregate on. 
  * **condition** Specify condition column.



Example:


| value   | condition   | catagory    |
|  -------- | -------- | -------- |
| 0   | true   | x    |
| 1   | false   | y    |
| 2   | false   | x    |
| 3   | true   | y    |
| 4   | true   | x    |




```sql
SELECT sum_cate_where(catagory, value, condition) OVER w;
-- output "x:4,y:3"
```

**Supported Types**:

* [list_number, list_bool, list_date]
* [list_number, list_bool, list_int16]
* [list_number, list_bool, list_int32]
* [list_number, list_bool, list_int64]
* [list_number, list_bool, list_string]
* [list_number, list_bool, list_timestamp] 

### function sum_where

```sql
sum_where()
```

**Description**:

Compute sum of values match specified condition. 

**Supported Types**:

* [list_number, list_bool] 

### function tan

```sql
tan()
```

**Description**:

Return the tangent of expr. 

**Parameters**: 

  * **expr** It is a single argument in radians.


**Since**:
0.1.0


Example:



```sql
SELECT TAN(0);
-- output 0.000000
```


**Supported Types**:

* [number] 

### function timestamp

```sql
timestamp()
```

**Description**:


**Supported Types**:

* [date]
* [string] 

### function top

```sql
top()
```

**Description**:

Compute top k of values and output string separated by comma. The outputs are sorted in desc order. 

**Supported Types**:

* [list_date, list_int32]
* [list_date, list_int64]
* [list_number, list_int32]
* [list_number, list_int64]
* [list_string, list_int32]
* [list_string, list_int64]
* [list_timestamp, list_int32]
* [list_timestamp, list_int64] 

### function top_n_key_avg_cate_where

```sql
top_n_key_avg_cate_where()
```

**Description**:

Compute average of values matching specified condition grouped by category key. Output string for top N keys in descend order. Each group is represented as 'K:V' and separated by comma. 

**Parameters**: 

  * **catagory** Specify catagory column to group by. 
  * **value** Specify value column to aggregate on. 
  * **condition** Specify condition column. 
  * **n** Fetch top n keys.



Example:


| value   | condition   | catagory    |
|  -------- | -------- | -------- |
| 0   | true   | x    |
| 1   | false   | y    |
| 2   | false   | x    |
| 3   | true   | y    |
| 4   | true   | x    |
| 5   | true   | z    |
| 6   | false   | z    |




```sql
    SELECT top_n_key_avg_cate_where(value, condition, catagory, 2)
OVER w;
    -- output "z:5,y:3"
```

**Supported Types**:

* [list_number, list_bool, list_date, list_int32]
* [list_number, list_bool, list_date, list_int64]
* [list_number, list_bool, list_int16, list_int32]
* [list_number, list_bool, list_int16, list_int64]
* [list_number, list_bool, list_int32, list_int32]
* [list_number, list_bool, list_int32, list_int64]
* [list_number, list_bool, list_int64, list_int32]
* [list_number, list_bool, list_int64, list_int64]
* [list_number, list_bool, list_string, list_int32]
* [list_number, list_bool, list_string, list_int64]
* [list_number, list_bool, list_timestamp, list_int32]
* [list_number, list_bool, list_timestamp, list_int64] 

### function top_n_key_count_cate_where

```sql
top_n_key_count_cate_where()
```

**Description**:

Compute count of values matching specified condition grouped by category key. Output string for top N keys in descend order. Each group is represented as 'K:V' and separated by comma. 

**Parameters**: 

  * **catagory** Specify catagory column to group by. 
  * **value** Specify value column to aggregate on. 
  * **condition** Specify condition column. 
  * **n** Fetch top n keys.



Example:


| value   | condition   | catagory    |
|  -------- | -------- | -------- |
| 0   | true   | x    |
| 1   | true   | y    |
| 2   | false   | x    |
| 3   | true   | y    |
| 4   | false   | x    |
| 5   | true   | z    |
| 6   | true   | z    |




```sql
    SELECT top_n_key_count_cate_where(value, condition, catagory, 2)
OVER w;
    -- output "z:2,y:2"
```

**Supported Types**:

* [list_number, list_bool, list_date, list_int32]
* [list_number, list_bool, list_date, list_int64]
* [list_number, list_bool, list_int16, list_int32]
* [list_number, list_bool, list_int16, list_int64]
* [list_number, list_bool, list_int32, list_int32]
* [list_number, list_bool, list_int32, list_int64]
* [list_number, list_bool, list_int64, list_int32]
* [list_number, list_bool, list_int64, list_int64]
* [list_number, list_bool, list_string, list_int32]
* [list_number, list_bool, list_string, list_int64]
* [list_number, list_bool, list_timestamp, list_int32]
* [list_number, list_bool, list_timestamp, list_int64] 

### function top_n_key_max_cate_where

```sql
top_n_key_max_cate_where()
```

**Description**:

Compute maximum of values matching specified condition grouped by category key. Output string for top N keys in descend order. Each group is represented as 'K:V' and separated by comma. 

**Parameters**: 

  * **catagory** Specify catagory column to group by. 
  * **value** Specify value column to aggregate on. 
  * **condition** Specify condition column. 
  * **n** Fetch top n keys.



Example:


| value   | condition   | catagory    |
|  -------- | -------- | -------- |
| 0   | true   | x    |
| 1   | false   | y    |
| 2   | false   | x    |
| 3   | true   | y    |
| 4   | true   | x    |
| 5   | true   | z    |
| 6   | false   | z    |




```sql
    SELECT top_n_key_max_cate_where(value, condition, catagory, 2)
OVER w;
    -- output "z:5,y:3"
```

**Supported Types**:

* [list_number, list_bool, list_date, list_int32]
* [list_number, list_bool, list_date, list_int64]
* [list_number, list_bool, list_int16, list_int32]
* [list_number, list_bool, list_int16, list_int64]
* [list_number, list_bool, list_int32, list_int32]
* [list_number, list_bool, list_int32, list_int64]
* [list_number, list_bool, list_int64, list_int32]
* [list_number, list_bool, list_int64, list_int64]
* [list_number, list_bool, list_string, list_int32]
* [list_number, list_bool, list_string, list_int64]
* [list_number, list_bool, list_timestamp, list_int32]
* [list_number, list_bool, list_timestamp, list_int64] 

### function top_n_key_min_cate_where

```sql
top_n_key_min_cate_where()
```

**Description**:


**Parameters**: 

  * **catagory** Specify catagory column to group by. 
  * **value** Specify value column to aggregate on. 
  * **condition** Specify condition column. 
  * **n** Fetch top n keys.


Compute minimum of values matching specified condition grouped by category key. Output string for top N keys in descend order. Each group is represented as 'K:V' and separated by comma.


Example:


| value   | condition   | catagory    |
|  -------- | -------- | -------- |
| 0   | true   | x    |
| 1   | true   | y    |
| 2   | false   | x    |
| 3   | true   | y    |
| 4   | false   | x    |
| 5   | true   | z    |
| 6   | true   | z    |




```sql
    SELECT top_n_key_min_cate_where(value, condition, catagory, 2)
OVER w;
    -- output "z:5,y:1"
```

**Supported Types**:

* [list_number, list_bool, list_date, list_int32]
* [list_number, list_bool, list_date, list_int64]
* [list_number, list_bool, list_int16, list_int32]
* [list_number, list_bool, list_int16, list_int64]
* [list_number, list_bool, list_int32, list_int32]
* [list_number, list_bool, list_int32, list_int64]
* [list_number, list_bool, list_int64, list_int32]
* [list_number, list_bool, list_int64, list_int64]
* [list_number, list_bool, list_string, list_int32]
* [list_number, list_bool, list_string, list_int64]
* [list_number, list_bool, list_timestamp, list_int32]
* [list_number, list_bool, list_timestamp, list_int64] 

### function top_n_key_sum_cate_where

```sql
top_n_key_sum_cate_where()
```

**Description**:

Compute sum of values matching specified condition grouped by category key. Output string for top N keys in descend order. Each group is represented as 'K:V' and separated by comma. 

**Parameters**: 

  * **catagory** Specify catagory column to group by. 
  * **value** Specify value column to aggregate on. 
  * **condition** Specify condition column. 
  * **n** Fetch top n keys.



Example:


| value   | condition   | catagory    |
|  -------- | -------- | -------- |
| 0   | true   | x    |
| 1   | true   | y    |
| 2   | false   | x    |
| 3   | true   | y    |
| 4   | false   | x    |
| 5   | true   | z    |
| 6   | true   | z    |




```sql
    SELECT top_n_key_sum_cate_where(value, condition, catagory, 2)
OVER w;
    -- output "z:11,y:4"
```

**Supported Types**:

* [list_number, list_bool, list_date, list_int32]
* [list_number, list_bool, list_date, list_int64]
* [list_number, list_bool, list_int16, list_int32]
* [list_number, list_bool, list_int16, list_int64]
* [list_number, list_bool, list_int32, list_int32]
* [list_number, list_bool, list_int32, list_int64]
* [list_number, list_bool, list_int64, list_int32]
* [list_number, list_bool, list_int64, list_int64]
* [list_number, list_bool, list_string, list_int32]
* [list_number, list_bool, list_string, list_int64]
* [list_number, list_bool, list_timestamp, list_int32]
* [list_number, list_bool, list_timestamp, list_int64] 

### function truncate

```sql
truncate()
```

**Description**:

Return the nearest integer that is not greater in magnitude than the expr. 

**Parameters**: 

  * **expr** 


**Since**:
0.1.0


Example:



```sql
SELECT TRUNCATE(1.23);
-- output 1.0
```


**Supported Types**:

* [bool]
* [number] 

### function week

```sql
week()
```

**Description**:


**Supported Types**:

* [date]
* [int64]
* [timestamp] 

### function weekofyear

```sql
weekofyear()
```

**Description**:


**Supported Types**:

* [date]
* [int64]
* [timestamp] 

### function year

```sql
year()
```

**Description**:


**Supported Types**:

* [date]
* [int64]
* [timestamp] 




