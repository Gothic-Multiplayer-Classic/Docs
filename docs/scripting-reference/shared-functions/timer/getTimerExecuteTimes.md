---
title: 'getTimerExecuteTimes'
---
# `function` getTimerExecuteTimes <font size="4">(shared-side)</font>
!!! info "Available since version: 0.3.0"

Returns how many times the timer will execute, or nil if the timer does not exist.

A value of 0 means the timer repeats indefinitely.

## Declaration
```cpp
int|nil getTimerExecuteTimes(int timer_id)
```

## Parameters
* `int` **timer_id**: Timer ID returned by setTimer.
  
## Returns `int|nil`
Execute count (0 = infinite), or nil if not found.
