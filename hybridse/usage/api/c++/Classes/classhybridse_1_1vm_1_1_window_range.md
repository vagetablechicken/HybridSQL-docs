---
title: hybridse::vm::WindowRange

---
# hybridse::vm::WindowRange



`#include <mem_catalog.h>`

## Summary
## Public Types

|                | Name           |
| -------------- | -------------- |
| enum| **[WindowPositionStatus](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_window_range.md#enum-windowpositionstatus)** { kInWindow, kExceedWindow, kBeforeWindow} |



|  Public functions|            |
| -------------- | -------------- |
|**[WindowRange](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_window_range.md#function-windowrange)**()|  |
|**[WindowRange](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_window_range.md#function-windowrange)**([Window::WindowFrameType](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_window.md#enum-windowframetype) frame_type, int64_t start_offset, int64_t end_offset, uint64_t rows_preceding, uint64_t max_size)|  |
|**[~WindowRange](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_window_range.md#function-~windowrange)**()|  |
|**[GetWindowPositionStatus](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_window_range.md#function-getwindowpositionstatus)**(bool out_of_rows, bool before_window, bool exceed_window) const| const [WindowPositionStatus](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_window_range.md#enum-windowpositionstatus)  |
|**[CreateRowsWindow](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_window_range.md#function-createrowswindow)**(uint64_t rows_preceding)| [WindowRange](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_window_range.md)  |
|**[CreateRowsRangeWindow](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_window_range.md#function-createrowsrangewindow)**(int64_t start_offset, int64_t end_offset, uint64_t max_size =0)| [WindowRange](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_window_range.md)  |
|**[CreateRowsMergeRowsRangeWindow](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_window_range.md#function-createrowsmergerowsrangewindow)**(int64_t start_offset, uint64_t rows_preceding, uint64_t max_size =0)| [WindowRange](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_window_range.md)  |



| Public attributes|    |
| -------------- | -------------- |
| [Window::WindowFrameType](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_window.md#enum-windowframetype) | **[frame_type_](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_window_range.md#variable-frame_type_)**  |
| int64_t | **[start_offset_](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_window_range.md#variable-start_offset_)**  |
| int64_t | **[end_offset_](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_window_range.md#variable-end_offset_)**  |
| uint64_t | **[start_row_](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_window_range.md#variable-start_row_)**  |
| uint64_t | **[end_row_](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_window_range.md#variable-end_row_)**  |
| uint64_t | **[max_size_](/hybridse/usage/api/c++/Classes/classhybridse_1_1vm_1_1_window_range.md#variable-max_size_)**  |

## Public Types

### enum WindowPositionStatus

| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| kInWindow | |   |
| kExceedWindow | |   |
| kBeforeWindow | |   |




## Public Functions

#### function WindowRange

```cpp
inline WindowRange()
```


#### function WindowRange

```cpp
inline WindowRange(
    Window::WindowFrameType frame_type,
    int64_t start_offset,
    int64_t end_offset,
    uint64_t rows_preceding,
    uint64_t max_size
)
```


#### function ~WindowRange

```cpp
inline virtual ~WindowRange()
```


#### function GetWindowPositionStatus

```cpp
inline const WindowPositionStatus GetWindowPositionStatus(
    bool out_of_rows,
    bool before_window,
    bool exceed_window
) const
```


#### function CreateRowsWindow

```cpp
static inline WindowRange CreateRowsWindow(
    uint64_t rows_preceding
)
```


#### function CreateRowsRangeWindow

```cpp
static inline WindowRange CreateRowsRangeWindow(
    int64_t start_offset,
    int64_t end_offset,
    uint64_t max_size =0
)
```


#### function CreateRowsMergeRowsRangeWindow

```cpp
static inline WindowRange CreateRowsMergeRowsRangeWindow(
    int64_t start_offset,
    uint64_t rows_preceding,
    uint64_t max_size =0
)
```


## Public Attributes

### variable frame_type_

```cpp
Window::WindowFrameType frame_type_;
```


### variable start_offset_

```cpp
int64_t start_offset_;
```


### variable end_offset_

```cpp
int64_t end_offset_;
```


### variable start_row_

```cpp
uint64_t start_row_;
```


### variable end_row_

```cpp
uint64_t end_row_;
```


### variable max_size_

```cpp
uint64_t max_size_;
```


-------------------------------

Updated on 29 March 2021 at 18:05:16 PDT