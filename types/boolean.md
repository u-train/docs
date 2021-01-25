---
title: boolean
description: 
published: true
tags: 
---

## Purpose

Booleans are either `true` or `false`. Most of the time, you'll find yourself using them in conditionals. For example, an if statement requires a boolean to evaluate what to do next. If it is true, it will execute the block of code it is wrapped around. Otherwise, (if it is false), it will skip that block of code.

## Values

`nil` evaluates to `false` when coerced (implicitly changed) into a boolean. Every other value is cocerced to `true`. *This means even the number 0 is truthy!*

## Boolean logic

> *Note*: If something has the attribute of being `true`, you can refer to it as `truthy` value. The opposite would be `falsey`.

Besides having `true` and `false`, you also have boolean operators.

- `and`
- `or`
- `not`
- `<`, `>`, `<=`, `>=`, `~=`, `==`

These are all of the operators in Lua listed by their precendence (with `1` having most).

1. `^`
2. `not`, `-` (unary)
3. `*`, `/`
4. `+`, `-`
5. `..`
6. `<`, `>`, `<=`, `>=`, `~=`, `==`
7. `and`
8. `or`

Only `^` and `..` are right associative. The rest are left associative.

### `and`

This operator evaulates to `false` if either or both values are falsey. Otherwise, it will evaulate to the second value.

```lua
print(true and 100) --> 100
print(100 and "") --> ""
print(false and true) --> false
print(false and nil) --> false
```

### `or`

This operator evaulates to `false` if none of the values are truthy. Otherwise, it will evaulate to the first truthy value.

```lua
print(5 or 1) --> 5
print(false or 3) --> 3
print(false or false) --> false
```

### `not`

This is a uniary operator. That means it only takes in one value. It simply inverts the boolean to its opposite.

```lua
print(not true) --> false
print(not false) --> true
```

### Equality

The `==` evaulates to `true` if the values on each side are equal to each other. `~=` is the `not`ted version of `==`.

```lua
print(true == true) --> true
print(0 == 1) --> false (not the same number)
print(1 == 1) --> true
print({} == {}) --> false (not the same table)
print("" == "") --> true (the same content)
```

> *Note*: Tables can override both equality operator using a metatable and setting the corresponding metamethods. For example, `vector2(1, 1) == vector2(1, 1)` should really be true (since they're equal) and not false (even if they're different tables). So, the equal operator is overriden to do this. Read the documentation for tables for more information.

### Inequality

The `>` operator evaulates to `true` if the value on the left is greater than the one on the right. The `<` operator is the mirrored version of the `>` operator.

```lua
print(1 > 0) --> true
print(1 < 0) --> false
print(1 < 1) --> false
print({} > {}) --> ERROR! You can't compare two tables with inequality.
print("" > "") --> ERROR! You can't compare two strings with inequality.
print(true < false) --> ERROR! You can't compare two booleans with inequality.
```

`>=` operator evaulates to `true` if the value on the left is greater than or equal to the value on the left. `<=` is the mirrored version of `>=`.

```lua
print(1 >= 0) --> true
print(1 <= 0) --> false
print(1 <= 1) --> *true
```

> *Note*: Just like with equality operators, tables can override inequality operators as well. So, it may not necessarily error as shown above.

## Usages

### Control flow

Booleans are used for control flows such as the if-statement or while-do. Read the tutorial on control flows for more information.

### Variable variable declaration

Abusing how the `and` and `or` evaulate, you can simplify long statements into sunnict expressions. Let's simplify defaulting parameters.

```lua
local default = 10

do -- Long way...
    local a
    if a == nil then a = default end
end

do -- Nicer way.
    local a
    a = a or default -- 'or' will select one of the truthy values.
end
```

> *Note*: Keep in mind if `a` is false, it will still default anyways! Be sure you do not care about this.

Let's try another, conditional declarations.

```lua
do -- Long way...
    local bouncer = 0
    local antiBouncer

    if bouncer <= 1 then
        antiBouncer = 0
    else
        antiBouncer = bouncer * 2
    end
end

do -- Shorter way!
    local bouncer = 0
    local antiBouncer = bouncer <= 1 and 0 or bouncer * 2
end
```

> *Note*: There's a minor problem with the shorter way. Can you find it? Hint: replace 0 in the shorter example with a falsey value and evaulate.

You can also chain them along like so:

```lua
local cond1 = false
local cond2 = false

local value = (cond1 and 1) or (cond2 and 2) or 0

print(value) --> 0
```

> *Note*: You may note that the parathesis can be removed and it will still work as intended. However, they are there for the reader.
>
> *Experiment*: Change the values of cond1 and cond2 to something truthy. See what happens with both of them are truthy. Diagram which part of the if-statement is in the expression.
