---
title: Control flows
description: Tutorial on control flows.
published: true
tags: 
---

## What are they?

Control flows, as the name implies, are constructs that control the flow of a program. They're use to...

- Minimizing the amount of repeating code.
- Allow the program to do different actions dependent on given inputs.

To illustrate both points, let's take a recipe for making a salad.

1. Gather 2 prepared tomatoes, 1/2 of prepared cucumbers, 1/8th of onion chopped, small bowl of lettuce.
2. Get 1/4th cup of avocado oil.
3. Get 2 teaspoons of salt.
4. Accquire mixing utensils.
5. Prepare a large bowl.
6. Dump the prepared tomatoes into the large bowl.
7. Dump the prepared cucumber into the large bowl.
8. Dump the lettuce into the large bowl.
9. Dump the prepared onion into the large bowl.
10. Distribute evenly the salt and oil throughout the surface of the salad.
11. Mix well with mixing utensils.
12. You now have a salad to eat!

You may notice that we are repeating the same action throughout step 4 to 7. However, we're only changing the content we're dumping. Additionally, the contents we're dumping is conviently gathered in step 1. So, let's change step one to...

- Gather 2 prepared tomatoes, 1/2 of prepared cucumbers, 1/8th of onion chopped, small bowl of lettuce. Set these aside as solids.

Then, let's replace step 6 through 9 with

- Dump each of the soilds set aside into the large bowl.

We have eliminated 3 steps and now its more concise. We have minimized the amount of repeating ~~code~~ actions. Additionally, now we can change what is gathered and the program will respond as intended (dumping those gathered solids). An equivelent of this in Lua is the for loop statement to do this.

We can also replace the 2nd instruction since not everyone has avocado oil to fallback to an alternative.

- If you have avocado oil, get 1/4th cup of avocado oil. Otherwise, use 1/4th cup olive oil.

Now, just because they don't have avocado oil (which may be unexpected) doesn't mean they can't make it! Thus, we made the program responsive to different inputs. An equivelent of this would be an if-statement in Lua.

So, what control flow constructs are there?

## Types of control flow structures

### If statement

`if (condition) then ... end`

Where it will execute the block of if the conditions are true.

```lua
local num1 = 1
local num2 = 0

-- Execute a block of code if true.
if num1 > num2 then
    print("Ran since num1 > num2 is true!")
end

if num1 == num2 then
    print("This won't run.")
end

-- Else can be used as a default case.
if not num1 < num2 then
    print("Ran!")
else
    print("Didn't run...")
end

if num1 == num2 then
    print("This wont run...")
else
    print("But this will!")
end

-- You can chain as many elseif statements as desired. Just note that there can only be one else and it should be the last block.

local printNumEquality = function(x1, x2)
    if num1 == num2 then
        print(num2 .. " is equal to " .. num1)
    elseif num1 > num2 then
        print(num2 .. " is greater than " .. num1)
    else
        print(num2 .. " must be less than " .. num1)
    end
end

printNumEquality(0, 0) --> 0 is equal to 0
printNumEquality(1, 0) --> 1 is greater than 0
printNumEquality(0, 1) --> 0 must be less than 1
```

### While loop

`while (condition) do ... end`

Where the condition must be true to execute the execute the loop.

```lua
local counter = 1

-- It'll print 1, 2, ..., 10
while counter > 10 do
    print(counter)
    counter = counter + 1
end
```

### For loop

#### `i` Loop

`for iteratorVariable = start, goal, [incrementBy = 1] do ... end`

A type of while loop which there is an iterator variable that's being kept track of. Every successful loop, it increments it by the amount set. When it reaches the goal, it will break out of the loop.

```lua
-- Prints 1, 2,  ... 10
for i = 1, 10, 1 do
    print(i)
end
```

#### Iterator function

`for iteratorVariable, ... in iteratorFunction, invariant, initalValue do ... end`

A type of loop take in an iterator function that itself takes an invariant and a state value. This function also has to return atleast one value. This is captured with the `... in` part of the construct. If it returns nil, that demarks the end of the iteration.

```lua
-- 'next' is a built in function that can iterate through every table field.
-- Giving it nil will ask it to find the first table field (it may or may not be a numerical field!)

for key, value in next, {1, 2, 3, 4}, nil do
    print(value)
end

-- We should expect 1, 2, 3, 4.
```

> *Note*: We do not have to explicitly pass `nil` as the starting value. If we didn't pass anything, it would still be `nil`. As in, this is the same as the above: `for key, value in next, {1, 2, 3, 4} do ...`

> *Challenge*: Try to make the `ipair` iterator constructor function! This function allows you to iterates through the table starting from 1 and incrementing by 1 until it reaches a nil field. You will have to make a function that returns a function, invariant, and inital value. If you're having trouble, search up an implementation.
  
### repeat until

`repeat ... until (condition)`

Where the block is executed then it will repeat the execution until the condition is true.

```lua
local counter = 10

repeat
    print(counter) --> Will be ran regardless of condition.
until not(counter > 10)
```

### Break

A control flow statement which allows you to break out of a loop. This works with repeat until loop, for loop, and while do loop. Doing it anywhere else will cause an error.

```lua
-- This will print 10, 9, ..., 1
do
    local i = 10

    while true do
        print(i)
        i = i - 1
        if i < 0 then
            break -- It will "break" out of the loop and continue down the code.
        end
    end
end

-- This will print 1, 2, ..., 10
for i = 1, 10 do
    print(i)
end
```

> *Note*: They look oddly familar... What do you think of it?
