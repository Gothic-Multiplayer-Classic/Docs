---
title: 'LOG_CRITICAL'
---
# `function` LOG_CRITICAL <font size="4">(shared-side)</font>
!!! info "Available since version: 0.3.0"

Logs a message with CRITICAL severity.

Critical messages report very severe errors that may require immediate
attention or application shutdown.

## Declaration
```cpp
void LOG_CRITICAL(string text)
```

## Parameters
* `string` **text**: The message text, may contain format specifiers.
