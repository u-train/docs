---
title: Breaking Changes
description: 
published: true
tags: 
---

## Breaking Changes

- `tevurl:` no longer works, locating resources with this identifier will fail. Please use `deviap:` instead.
  
  e.g. `"tevurl:fonts/openSansBold.ttf"` is now `deviap:fonts/openSansBold.ttf`
- `tevgit:` no longer works for locating assets such as images and fonts, use `devgit:` instead.

## Deprecations

Please immediately update your code to fix any deprecation warnings.

- `teverse` namespace forwarded to `core`.
- `tevgit:` for locating scripts in require has been deprecated.
