---
title: 'addEventHandler'
---
# `function` addEventHandler <font size="4">(client-side)</font>

This function will bind function to specified event.

## Declaration
```cpp
boolean addEventHandler(string eventName, function func)
```

## Parameters
* `string` **eventName**: The name of the event.
* `function` **func**: The reference to a function, keep in mind that function must have the same amount of arguments as event.
  
## Returns `boolean`
True on success, false on failure.

