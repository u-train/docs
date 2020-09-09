---
title: colour
description: 
published: true
tags: 
---

# Colour

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
