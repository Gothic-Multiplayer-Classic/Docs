---
title: 'Vec2'
---
# `class` Vec2 <font size="4">(shared-side)</font>

2D vector with basic math utilities.

### Constructor
```cpp
Vec2(number value)
```

**Parameters:**

* `number` **value**: Value assigned to x and y.
### Constructor
```cpp
Vec2(number x, number y)
```

**Parameters:**

* `number` **x**: X component.
* `number` **y**: Y component.

## Properties
### `number` x 

X component.

----
### `number` y 

Y component.

----

## Methods
### len

Returns the vector length (magnitude).

```cpp
number len()
```

  
**Returns `number`:**

Vector length.

----
### len2

Returns the squared vector length.

```cpp
number len2()
```

  
**Returns `number`:**

Squared vector length.

----
### lenApprox

Returns an approximate vector length.

```cpp
number lenApprox()
```

  
**Returns `number`:**

Approximate vector length.

----
### distance

Returns the distance to another vector.

```cpp
number distance(Vec2 vec)
```

**Parameters:**

* `Vec2` **vec**: Other vector.
  
**Returns `number`:**

Distance between vectors.

----
### normalize

Normalizes the vector in-place.

If the vector length is zero, no change is applied.

```cpp
Vec2 normalize()
```

  
**Returns `Vec2`:**

This vector (normalized).

----
### normalizeSafe

Normalizes the vector in-place using an epsilon check.

If the vector length is below a small threshold, no change is applied.

```cpp
Vec2 normalizeSafe()
```

  
**Returns `Vec2`:**

This vector (normalized).

----
### normalizeApprox

Normalizes the vector in-place using an approximate inverse square root.

```cpp
Vec2 normalizeApprox()
```

  
**Returns `Vec2`:**

This vector (normalized).

----
### set

Sets both components of the vector.

```cpp
void set(number x, number y)
```

**Parameters:**

* `number` **x**: X component.
* `number` **y**: Y component.
  

----
### isEqualEps

Compares this vector with another vector using an epsilon tolerance.

```cpp
bool isEqualEps(Vec2 vec)
```

**Parameters:**

* `Vec2` **vec**: Other vector.
  
**Returns `bool`:**

True if both components are equal within epsilon.

----
### abs

Returns a vector with absolute component values.

```cpp
Vec2 abs()
```

  
**Returns `Vec2`:**

Vector with abs(x) and abs(y).

----
### `static` swap

Swaps two vectors.

```cpp
void swap(Vec2 vec1, Vec2 vec2)
```

**Parameters:**

* `Vec2` **vec1**: First vector.
* `Vec2` **vec2**: Second vector.
  

----
### `static` min

Returns the component-wise minimum of two vectors.

```cpp
Vec2 min(Vec2 vec1, Vec2 vec2)
```

**Parameters:**

* `Vec2` **vec1**: First vector.
* `Vec2` **vec2**: Second vector.
  
**Returns `Vec2`:**

Component-wise minimum.

----
### `static` max

Returns the component-wise maximum of two vectors.

```cpp
Vec2 max(Vec2 vec1, Vec2 vec2)
```

**Parameters:**

* `Vec2` **vec1**: First vector.
* `Vec2` **vec2**: Second vector.
  
**Returns `Vec2`:**

Component-wise maximum.

----
### `static` prod

Returns the component-wise product of two vectors.

```cpp
Vec2 prod(Vec2 vec1, Vec2 vec2)
```

**Parameters:**

* `Vec2` **vec1**: First vector.
* `Vec2` **vec2**: Second vector.
  
**Returns `Vec2`:**

Component-wise product.

----
### `static` dot

Returns the dot product of two vectors.

```cpp
number dot(Vec2 vec1, Vec2 vec2)
```

**Parameters:**

* `Vec2` **vec1**: First vector.
* `Vec2` **vec2**: Second vector.
  
**Returns `number`:**

Dot product.

----
### `static` lerp

Linearly interpolates between two vectors.

```cpp
Vec2 lerp(number t, Vec2 v1, Vec2 v2)
```

**Parameters:**

* `number` **t**: Interpolation factor (typically 0..1).
* `Vec2` **v1**: Start vector.
* `Vec2` **v2**: End vector.
  
**Returns `Vec2`:**

Interpolated vector.

----

## Callbacks
No callbacks.

----
