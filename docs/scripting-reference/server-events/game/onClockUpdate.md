---
title: 'onClockUpdate'
---
# `event` onClockUpdate <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

This event is triggered every time the server clock updates.

## Parameters
```c++
void onClockUpdate(int day, int hour, int min)
```

* `int` **day**: The current ingame day.
* `int` **hour**: The current ingame hour.
* `int` **min**: The current ingame minute.
