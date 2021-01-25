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

## Easing Styles

The following is a list of easing styles to implement.

| Easing styles | Description |
| --- | --- |
| linear | Linear steps to goal. |
| inQuad | Increasing quadratic steps goal. |
| outQuad | Decreasing qudaratic steps to goal. |
| inOutQuad |  Decreasing qudaratic steps to goal. |
| outInQuad |  Decreasing qudaratic steps to goal. |
| inCubic |  Decreasing qudaratic steps to goal. |
| outCubic |  Decreasing qudaratic steps to goal. |
| inOutCubic |  Decreasing qudaratic steps to goal. |
| outInCubic |  Decreasing qudaratic steps to goal. |
| inQuart | Decreasing qudaratic steps to goal.  |
| outQuart |  Decreasing qudaratic steps to goal. |
| inOutQuart |  Decreasing qudaratic steps to goal. |
| outInQuart |  Decreasing qudaratic steps to goal. |
| inQuint |  Decreasing qudaratic steps to goal. |
| outQuint | Decreasing qudaratic steps to goal.  |
| inOutQuint |  Decreasing qudaratic steps to goal. |
| outInQuint | Decreasing qudaratic steps to goal. |
| inSine | Decreasing qudaratic steps to goal. |
| outSine |  Decreasing qudaratic steps to goal. |
| inOutSine |  Decreasing qudaratic steps to goal. |
| outInSine |  Decreasing qudaratic steps to goal. |
| inExpo |  Decreasing qudaratic steps to goal. |
| outExpo | Decreasing qudaratic steps to goal. |
| inOutExpo |  Decreasing qudaratic steps to goal. |
| outInExpo |  Decreasing qudaratic steps to goal. |
| inCirc |  Decreasing qudaratic steps to goal. |
| outCirc |  Decreasing qudaratic steps to goal. |
| inOutCirc |  Decreasing qudaratic steps to goal. |
| outInCirc | Decreasing qudaratic steps to goal.  |
| inElastic |  Decreasing qudaratic steps to goal. |
| outElastic |  Decreasing qudaratic steps to goal. |
| inOutElastic |  Decreasing qudaratic steps to goal. |
| outInElastic |  Decreasing qudaratic steps to goal. |
| inBack |  Decreasing qudaratic steps to goal. |
| outBack |  Decreasing qudaratic steps to goal. |
| inOutBack |  Decreasing qudaratic steps to goal. |
| outInBack |  Decreasing qudaratic steps to goal. |
| inBounce | Decreasing qudaratic steps to goal.  |
| outBounce |  Decreasing qudaratic steps to goal. |
| inOutBounce |  Decreasing qudaratic steps to goal. |
| outInBounce |  Decreasing qudaratic steps to goal. |

---
