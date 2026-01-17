---
title: 'setTimerExecuteTimes'
---
# `function` setTimerExecuteTimes <font size="4">(shared-side)</font>
!!! info "Available since version: 0.3.0"

Sets how many times the timer should execute.

If execute_times is 0 or negative, the timer repeats indefinitely.

## Declaration
```cpp
void setTimerExecuteTimes(int timer_id, int execute_times)
```

## Parameters
* `int` **timer_id**: Timer ID returned by setTimer.
* `int` **execute_times**: How many times to execute (<= 0 means infinite).
