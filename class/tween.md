---
title: Tween
description: Documentation of Tween class.
published: true
tags: 
---

## Purpose

Tweening is when you generate intermediate steps be*tween* a starting goal and end goal. It's useful for animating or otherwise making smooth transitions. So, this service is provided to allow you to tween tevObjects.

## Easings

Easings are how the intermediate steps are generated. By default, they're generated linearly (easing = "linear"). However, there are many kinds of easings avaliable to you.

The first part of the easing's name indicates the direction the easing has. The second part will tell you how style of the easing.

| Direction | Description |
| --- | --- |
| in | The size of each step starts at 0 unit, then increases over time. |
| out  | The size of each step starts at 1 unit, then decreases over time. |
| inOut | The size of each step starts at 0 and increases over time. Then, it peaks at the middle of the tween. and decreases over time. |

---

| Easing Names |
| --- |
| linear |
| inQuad |
| outQuad |
| inOutQuad |
| outInQuad |
| inCubic |
| outCubic |
| inOutCubic |
| outInCubic |
| inQuart |
| outQuart |
| inOutQuart |
| outInQuart |
| inQuint |
| outQuint |
| inOutQuint |
| outInQuint |
| inSine |
| outSine |
| inOutSine |
| outInSine |
| inExpo |
| outExpo |
| inOutExpo |
| outInExpo |
| inCirc |
| outCirc |
| inOutCirc |
| outInCirc |
| inElastic |
| outElastic |
| inOutElastic |
| outInElastic |
| inBack |
| outBack |
| inOutBack |
| outInBack |
| inBounce |
| outBounce |
| inOutBounce |
| outInBounce |
---
