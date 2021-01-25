---
title: nil
description: description of nil type. 
published: true
tags: 
---

## Purpose

Everything has some form of a value, such as the number 1. Another example would be a boolean `true`. However, it is useful to indicate that there is a lack of a value. Such examples are...

1. Representing unintialized values.
2. An empty table field.
3. Representing a lack of argument for a paramter in a function.
4. And more...

 This is where `nil` comes in. `nil` is the representation of no value. *Understand, `nil` is the opposite of a value. It is not a valid value!*

## Usage

### Variables

If a variable is not initalized, it will store `nil`.

```lua
local uninitalizedValue

print(uninitalizedValue == nil) -- true
```

Setting a variable equal to nil is effectively deleting the value stored in that variable.

```lua
local aReference = {}

aReference = nil --> The reference to the table is deleted now.
```

### Boolean

`nil` evaluates to `false` when coerced into a boolean. However, note that doesn't make it equal to `false`.

```lua
if nil == false then
    print("Nil does not equal false.")
end

if not(nil) == not(false) then
     print("Using the not operator, force nil to evaluate into false (then inverted to true)!")
end
```

### Tables

An empty table field stores `nil`.

```lua
local someTable = {}
print(someTable[1] == nil) --> true
print(someTable.field == nil) --> true
```

If you set a table field to `nil`, you're effectively deleting that field.

```lua
local someTable = { aField = 1 }
someTable.aField = nil -- Now, it's deleted.
```

It's used as a terminator for arrays. This means if you have `nil` inserted at some point, that will be the end of the array.

```lua
local someArray = {1, 2, nil, 4}

-- It'll only print the first 2 fields, since the third field is nil.
for key, value in ipairs(someArray) do
    print(key, value)
end
```

### Functions

If an argument is not passed to a function, it will default to `nil`.

```lua
local nilTest = function(arg1)
     return arg1 == nil
end

print(nilTest()) --> true
print(nilTest("arg1")) --> false
```
