---
title: vector2
description: 
published: true
tags: 
---

# Vector2

Vector2s consist of two components: `x`, `y`.

## Constructors

### `vector2(float x, float y)`

## Methods

### `vector2` `a:dot(vector2 b)`  
Returns the dot product vector between `a` and `b`
The dot product is a very useful tool for finding the angle between two vectors:

a · b = |a| × |b| × cos(θ) 

This means that the dot product of a and b is equal to the length of a multiplied by the length of b, multiplied by the cosine of θ, the angle between them.

To find the angle between them, you can divide the dot product by the length of the two vectors multiplied together and then pass it to negative cosine.

#### Example
```lua
local vector1 = vector2(5, 10)
local vector2 = vector2(6, -10)

local dotProduct = vector1:dot(vector2)
local angleCos = dotProduct / ( vector1.length * vector2.length )

-- Fun fact: If angleCos == 0 they're at right angles.
-- Note: This angle is in Radians.
local angle = math.acos(angleCos)

local angleInDegrees = math.deg(angle)
```
[Source 1](https://en.wikipedia.org/wiki/Dot_product), [Source 2](https://www.mathsisfun.com/algebra/vectors-dot-product.html)

### `float` `a:length()`  
Returns `a`'s length

### `vector2` `a:normal()`  
Returns a normalised version of `a`

### `vector2` `a:min(vector3 b)`  
Returns a vector composed of the minimum values between `a` and `b`

### `vector2` `a:max(vector3 b)`  
Returns a vector composed of the maximum values between `a` and `b`
