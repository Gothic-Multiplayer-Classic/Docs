---
title: 'setTimer'
---
# `function` setTimer <font size="4">(shared-side)</font>

Creates a new timer that calls the given function at a fixed interval.

The timer passes any additional arguments to the callback when it executes.
If execute_times is 0 or negative, the timer repeats indefinitely.

## Declaration
```cpp
int setTimer(function func, int interval, int execute_times, ... ...)
```

## Parameters
* `function` **func**: Callback function executed by the timer.
* `int` **interval**: Interval in milliseconds.
* `int` **execute_times**: How many times to execute the callback (<= 0 means infinite).
* `...` **...**: Additional arguments forwarded to the callback.
  
## Returns `int`
Timer ID.
