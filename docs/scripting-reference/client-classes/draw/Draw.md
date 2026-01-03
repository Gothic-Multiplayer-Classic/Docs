---
title: 'Draw'
---
# `class` Draw <font size="4">(client-side)</font>

2D text drawing helper for rendering overlay text on screen.

The Draw class stores position, text, font, color, alpha and visibility.
Call render() each frame to draw the text using current settings.

### Constructor
```cpp
Draw()
```

**Parameters:**

No parameters.
### Constructor
```cpp
Draw(int x, int y, string text)
```

**Parameters:**

* `int` **x**: Initial X position (virtual units).
* `int` **y**: Initial Y position (virtual units).
* `string` **text**: Initial text content.

## Properties
### `{x, y}` position 

Gets or sets the draw position in virtual screen units.

----
### `{x, y}` positionPx 

Gets or sets the draw position in pixel coordinates.

----
### `string` text 

Gets or sets the displayed text.

----
### `string` font 

Gets or sets the font identifier used for rendering.

----
### `{r, g, b}` color <font size="2">(read-only)</font>

Returns the current text color.

----
### `int` alpha 

Gets or sets the alpha (opacity).

----
### `bool` visible 

Gets or sets whether the Draw object is rendered.

----

## Methods
### setPosition

Sets the draw position in virtual screen units.

```cpp
void setPosition(int x, int y)
```

**Parameters:**

* `int` **x**: X position (virtual units).
* `int` **y**: Y position (virtual units).
  

----
### getPosition

Returns the draw position in virtual screen units.

```cpp
{x, y} getPosition()
```

  
**Returns `{x, y}`:**

Table containing x and y (virtual units).

----
### setPositionPx

Sets the draw position in pixel coordinates.

```cpp
void setPositionPx(int x, int y)
```

**Parameters:**

* `int` **x**: X position in pixels.
* `int` **y**: Y position in pixels.
  

----
### getPositionPx

Returns the draw position in pixel coordinates.

```cpp
{x, y} getPositionPx()
```

  
**Returns `{x, y}`:**

Table containing x and y in pixels.

----
### setText

Sets the text to render.

```cpp
void setText(string text)
```

**Parameters:**

* `string` **text**: Text to display.
  

----
### getText

Returns the current text.

```cpp
string getText()
```

  
**Returns `string`:**

Current text.

----
### setFont

Sets the font used for rendering.

```cpp
void setFont(string font)
```

**Parameters:**

* `string` **font**: Font file name.
  

----
### getFont

Returns the current font file name.

```cpp
string getFont()
```

  
**Returns `string`:**

Font file name.

----
### setColor

Sets the text color.

```cpp
void setColor(int r, int g, int b)
```

**Parameters:**

* `int` **r**: Red component (0-255).
* `int` **g**: Green component (0-255).
* `int` **b**: Blue component (0-255).
  

----
### getColor

Returns the current text color.

```cpp
{r, g, b} getColor()
```

  
**Returns `{r, g, b}`:**

Table containing r,g,b (0-255).

----
### setAlpha

Sets text alpha (opacity).

```cpp
void setAlpha(int alpha)
```

**Parameters:**

* `int` **alpha**: Opacity value (0-255).
  

----
### getAlpha

Returns the current alpha (opacity).

```cpp
int getAlpha()
```

  
**Returns `int`:**

Opacity value (0-255).

----
### setVisible

Sets whether the Draw object should render.

```cpp
void setVisible(bool visible)
```

**Parameters:**

* `bool` **visible**: True to render, false to hide.
  

----
### getVisible

Returns whether this Draw object is visible.

```cpp
bool getVisible()
```

  
**Returns `bool`:**

True if visible.

----

## Callbacks
No callbacks.

----
