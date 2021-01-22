---
title: colour
description: 
published: true
tags: 
---

## Fields

Colours consist of three components: `r`, `g`, `b`, which are red, green, and blue respectively.

## Constructors

`colour(float r, float g, float b)`  
Composes a colour from the R,G,B values between 0-1

`colour.rgb(float r, float g, float b)`  
Composes a colour from the R,G,B values between 0-255

`colour.hex(string hexValue)`  
Composes a colour from the provided hex value

`colour.white()`  
Shorthand for colour(1, 1, 1)

`colour.black()`  
Shorthand for colour(0, 0, 0)

`colour.random()`  
Shorthand for colour(math.random(), math.random(), math.random())

## Methods

`colour` `a:invert()`  
Returns the inverted colour

## Example

Let's imagine we have a three dimensional object, a `block` - it has no colour though, so we need to establish one for it. The following is how one would append the `colour` property to a block. Truly, it is quite simple!

```lua

block.colour = colour.white()

```
