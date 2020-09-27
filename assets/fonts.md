---
title: Fonts
description: 
published: true
tags: 
---

# Fonts

You can package custom fonts in your app bundle, but be sure to check that the font you are including has an open license.

Deviap hosts a collection of fonts, it is reasonable to assume these fonts are already cached on the user's client, which allows for rapid loading of typography.

```lua
  local textbox = core.construct("guiTextBox", {
    textFont = "deviap:fonts/sourceCodeProRegular.ttf"
  })
```

## Font Locators

| Font Name | Style | Asset Locator |
| --- | --- | ------------- |
| Open Sans | Light | deviap:fonts/openSansLight.ttf |
| Open Sans | Light Italic | deviap:fonts/openSansLightItalic.ttf |
| Open Sans | Regular | deviap:fonts/openSansRegular.ttf |
| Open Sans | Regular Italic | deviap:fonts/openSansItalic.ttf |
| Open Sans | Semi Bold | deviap:fonts/openSansSemiBold.ttf |
| Open Sans | Semi Bold Italic | deviap:fonts/openSansSemiBoldItalic.ttf |
| Open Sans | Bold | deviap:fonts/openSansBold.ttf |
| Open Sans | Bold Italic | deviap:fonts/openSansBoldItalic.ttf |
| Open Sans | Extra Bold | deviap:fonts/openSansExtraBold.ttf |
| Open Sans | Extra Bold Italic | deviap:fonts/openSansExtraBoldItalic.ttf |

| Font Name | Style | Asset Locator |
| --- | --- | ------------- |
| Source Code | Extra Light | deviap:fonts/sourceCodeProExtraLight.ttf |
| Source Code | Extra Light Italic | deviap:fonts/sourceCodeProExtraLightItalic.ttf |
| Source Code | Light | deviap:fonts/sourceCodeProLight.ttf |
| Source Code | Light Italic | deviap:fonts/sourceCodeProLightItalic.ttf |
| Source Code | Regular | deviap:fonts/sourceCodeProRegular.ttf |
| Source Code | Regular Italic | deviap:fonts/sourceCodeProItalic.ttf |
| Source Code | Semi Bold | deviap:fonts/sourceCodeProSemiBold.ttf |
| Source Code | Semi Bold Italic | deviap:fonts/sourceCodeProSemiBoldItalic.ttf |
| Source Code | Medium | deviap:fonts/sourceCodeProMedium.ttf |
| Source Code | Medium Italic | deviap:fonts/sourceCodeProMediumItalic.ttf |
| Source Code | Black | deviap:fonts/sourceCodeProBlack.ttf |
| Source Code | Black Italic | deviap:fonts/sourceCodeProBlackItalic.ttf |
