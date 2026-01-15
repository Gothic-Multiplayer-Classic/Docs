---
title: 'disableKey'
---
# `function` disableKey <font size="4">(client-side)</font>

This function will disable/enable specified keyboard key, like: ESCAPE, TAB, etc.

## Declaration
```cpp
void disableKey(int keyId, bool toggle)
```

## Parameters
* `int` **keyId**: The key code to disable. For more information about key codes, see [Key Constants](../../client-constants/Key.md).
* `bool` **toggle**: true when you want to disable specified keyboard key, otherwise false
