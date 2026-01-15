---
title: 'sscanf'
---
# `function` sscanf <font size="4">(shared-side)</font>

Split the specified text, interprets it according to format and stores the results into array.

## Declaration
```cpp
array|nil sscanf(string format, string text)
```

## Parameters
* `string` **format**: Format by which the text will be splitted. Each letter in the format represents one argument in the text. If the number of letters in the format will be greater than the number of arguments in the text, then function will fail. Currently supported data formats: `d` integer, `f` float, `s` string.
* `string` **text**: Text which will be splitted into parts.
  
## Returns `array|nil`
The array which contains splitted text, or null if text couldn't be converted.
