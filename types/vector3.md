---
title: vector3
description: 
published: true
tags: 
---

# Vector3

Vector3s consist of three components: `x`, `y`, `z`.

## Constructors

`vector3(float x, float y, float z)`

## Methods

`vector3` `a:cross(vector3 b)`  
Returns the cross vector between `a` and `b`

`vector3` `a:dot(vector3 b)`  
Returns the dot product vector between `a` and `b`

`float` `a:length()`  
Returns `a`'s length

`vector3` `a:normal()`  
Returns a normalised version of `a`

`vector3` `a:min(vector3 b)`  
Returns a vector composed of the minimum values between `a` and `b`

`vector3` `a:max(vector3 b)`  
Returns a vector composed of the maximum values between `a` and `b`

`float` `a:angle(vector3 b)`  
Returns the angle between vectors `a` and `b`

`vector3` `a:lerp(vector3 b, float alpha)`  
Returns a vector lerped from `a` to `b`

`vector3` `a:rotate(quaternion rotation)`  
Returns the `a` vector rotated by `rotation`
