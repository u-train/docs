# Tween

## Purpose

Tweening is when you generate intermediate steps be*tween* a starting goal and end goal. It's useful for animating or otherwise making smooth transitions. So, this service is provided to allow you to tween tevObjects.

## Easings

Easings are how the intermediate steps are generated. By default, they're generated linearly (easing = "linear"). However, there are many kinds of easings avaliable to you.

The first part of the easing's name indicates the direction the easing has. The second part will tell you how style of the easing. For example, "inOutCubic" means that it will increase the size of each step cubically, until it reaches the mid-point of the tween, which then it will decrease each step cubically.

|Names|
---
|linear
|inQuad
|outQuad
|inOutQuad
|outInQuad
|inCubic
|outCubic
|inOutCubic
|outInCubic
|inQuart
|outQuart
|inOutQuart
|outInQuart
|inQuint
|outQuint
|inOutQuint
|outInQuint
|inSine
|outSine
|inOutSine
|outInSine
|inExpo
|outExpo
|inOutExpo
|outInExpo
|inCirc
|outCirc
|inOutCirc
|outInCirc
|inElastic
|outElastic
|inOutElastic
|outInElastic
|inBack
|outBack
|inOutBack
|outInBack
|inBounce
|outBounce
|inOutBounce
|outInBounce
---
