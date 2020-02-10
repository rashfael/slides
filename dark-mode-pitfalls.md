---
theme: dark
---

# Dark Mode Pitfalls

---

# Choose Your Colors

===

<img src="./assets/fails/grey-palette.svg">

===

<img src="./assets/fails/grey-palette-2.svg">

===

<img src="./assets/fails/grey-palette-3.svg">

===

<img src="./assets/fails/grey-palette-4.svg">

===

<img src="./assets/fails/grey-palette-5.svg">

---

# Check Your Assets

===

<img class="small" src="./assets/fails/white-bg.png">

===

<video class="small" v-if="active" src="~./assets/fails/white-video.webm" autoplay="true" loop="true"/>

===

<img class="small" src="./assets/fails/dark-content.png">

===

<img class="small" src="./assets/fails/wrong-content.svg">

---

# 3rd Party Integrations

===

<img class="small" src="./assets/fails/iframe.png">

---

# Implementation

===

```html
<link href="base.css" rel="stylesheet">
<link href="theme.css" rel="stylesheet"
      media="prefers-color-scheme: dark">
```

===

```html
<picture>
  <source srcset="dark.svg" media="prefers-color-scheme: dark">
  <img src="default.svg" />
</picture>
```

===

# CSS Preprocessor Pains


:::notes
- css variables are awesome
- but, preprocessors
:::

===

```stylus
lightness(color) < 60% ? $clr-text-dark : $clr-text-light

alpha(color, 0.08)
```

===

# Genenerate Multiple Stylesheets

:::notes
- Generate multiple stylesheets with different variables
:::

<!-- - assets
- 3rd party integration iframes
- color theory
- shitty material design
- css preprocessors? how do? color computation
- app switch


HOW?

- link media / picture media
- Opting Into a Preferred Color Scheme: the color-scheme property

https://web.dev/prefers-color-scheme/

- high contrast -->
