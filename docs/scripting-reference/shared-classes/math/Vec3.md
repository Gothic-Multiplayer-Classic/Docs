---
title: 'Vec3'
---
# `class` Vec3 <font size="4">(shared-side)</font>
!!! info "Available since version: 0.3.0"

3D vector with basic math utilities.

### Constructor
```cpp
Vec3.new(number value)
```

**Parameters:**

* `number` **value**: Value assigned to x, y and z.
### Constructor
```cpp
Vec3.new(number x, number y, number z)
```

**Parameters:**

* `number` **x**: X component.
* `number` **y**: Y component.
* `number` **z**: Z component.

## Properties
### `number` x 

X component.

----
### `number` y 

Y component.

----
### `number` z 

Z component.

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
number distance(Vec3 vec)
```

**Parameters:**

* `Vec3` **vec**: Other vector.
  
**Returns `number`:**

Distance between vectors.

----
### distance2d

Returns the 2D distance to another vector (ignores Z component).

```cpp
number distance2d(Vec3 vec)
```

**Parameters:**

* `Vec3` **vec**: Other vector.
  
**Returns `number`:**

2D distance between vectors.

----
### normalize

Normalizes the vector in-place.

If the vector length is zero, no change is applied.

```cpp
Vec3 normalize()
```

  
**Returns `Vec3`:**

This vector (normalized).

----
### normalizeSafe

Normalizes the vector in-place using an epsilon check.

If the vector length is below a small threshold, no change is applied.

```cpp
Vec3 normalizeSafe()
```

  
**Returns `Vec3`:**

This vector (normalized).

----
### normalizeApprox

Normalizes the vector in-place using an approximate inverse square root.

```cpp
Vec3 normalizeApprox()
```

  
**Returns `Vec3`:**

This vector (normalized).

----
### set

Sets all components of the vector.

```cpp
void set(number x, number y, number z)
```

**Parameters:**

* `number` **x**: X component.
* `number` **y**: Y component.
* `number` **z**: Z component.
  

----
### isEqualEps

Compares this vector with another vector using an epsilon tolerance.

```cpp
bool isEqualEps(Vec3 vec)
```

**Parameters:**

* `Vec3` **vec**: Other vector.
  
**Returns `bool`:**

True if all components are equal within epsilon.

----
### abs

Returns a vector with absolute component values.

```cpp
Vec3 abs()
```

  
**Returns `Vec3`:**

Vector with abs(x), abs(y) and abs(z).

----
### reflect

Returns the reflection of this vector around a surface normal.

```cpp
Vec3 reflect(Vec3 normal)
```

**Parameters:**

* `Vec3` **normal**: Surface normal (typically normalized).
  
**Returns `Vec3`:**

Reflected vector.

----
### `static` swap

Swaps two vectors.

```cpp
void swap(Vec3 vec1, Vec3 vec2)
```

**Parameters:**

* `Vec3` **vec1**: First vector.
* `Vec3` **vec2**: Second vector.
  

----
### `static` min

Returns the component-wise minimum of two vectors.

```cpp
Vec3 min(Vec3 vec1, Vec3 vec2)
```

**Parameters:**

* `Vec3` **vec1**: First vector.
* `Vec3` **vec2**: Second vector.
  
**Returns `Vec3`:**

Component-wise minimum.

----
### `static` max

Returns the component-wise maximum of two vectors.

```cpp
Vec3 max(Vec3 vec1, Vec3 vec2)
```

**Parameters:**

* `Vec3` **vec1**: First vector.
* `Vec3` **vec2**: Second vector.
  
**Returns `Vec3`:**

Component-wise maximum.

----
### `static` prod

Returns the component-wise product of two vectors.

```cpp
Vec3 prod(Vec3 vec1, Vec3 vec2)
```

**Parameters:**

* `Vec3` **vec1**: First vector.
* `Vec3` **vec2**: Second vector.
  
**Returns `Vec3`:**

Component-wise product.

----
### `static` dot

Returns the dot product of two vectors.

```cpp
number dot(Vec3 vec1, Vec3 vec2)
```

**Parameters:**

* `Vec3` **vec1**: First vector.
* `Vec3` **vec2**: Second vector.
  
**Returns `number`:**

Dot product.

----
### `static` cross

Returns the cross product of two vectors.

```cpp
Vec3 cross(Vec3 vec1, Vec3 vec2)
```

**Parameters:**

* `Vec3` **vec1**: First vector.
* `Vec3` **vec2**: Second vector.
  
**Returns `Vec3`:**

Cross product.

----
### `static` lerp

Linearly interpolates between two vectors.

```cpp
Vec3 lerp(number t, Vec3 v1, Vec3 v2)
```

**Parameters:**

* `number` **t**: Interpolation factor (typically 0..1).
* `Vec3` **v1**: Start vector.
* `Vec3` **v2**: End vector.
  
**Returns `Vec3`:**

Interpolated vector.

----

## Callbacks
No callbacks.

----
