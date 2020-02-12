---
theme: dark
---

# Implementation
### and
# Pitfalls

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

===

desaturate foreground colors

---

# Shadow

---

# Check Your Assets

===

<img class="small" src="./assets/fails/white-bg.png">

===

<video class="small" v-if="active" src="~./assets/fails/white-video.webm" autoplay="true" loop="true"/>

===

<img class="small" src="./assets/fails/dark-content.png">

===

<img class="small" src="./assets/fails/illustration2.svg">

---

# 3rd Party Integrations

===

<img class="small" src="./assets/fails/iframe.png">

---

# Implementation

===

```css
@media(prefers-color-scheme: dark) {
	body {
		background-color: #263238;
		color: #FFF;
	}
}
```

===

<fragment>

```css
@media(prefers-color-scheme: dark) {
	:root {
		--color-background: #263238;
		--color-text: #FFF;
	}
}
```

</fragment>

===

<fragment>

```html
<link href="base.css" rel="stylesheet">
<link href="theme.css" rel="stylesheet"
      media="prefers-color-scheme: dark">
```

</fragment>

===

<fragment>

```html
<picture>
  <source srcset="dark.svg" media="prefers-color-scheme: dark">
  <img src="default.svg" />
</picture>
```

</fragment>

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

:::notes

- CSS Color Level 5

:::

===

# Bundlers

:::notes
- Webpack
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
