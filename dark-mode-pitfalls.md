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

<img src="./assets/fails/oversaturated.svg">

===

<img src="./assets/fails/desaturated.svg">

===

<div class="shadow"></div>

===

<video class="small" v-if="active" src="~./assets/fails/shadow.mp4" autoplay="true" loop="true"/>

===

<div class="bordered"></div>

---

# Check Your Assets

===

<img class="small" src="./assets/fails/white-bg.png">

===

<img class="small" src="./assets/fails/transparent.svg">

===

<video class="small" v-if="active" src="~./assets/fails/white-video.webm" autoplay="true" loop="true"/>

===

<img class="small" src="./assets/fails/dark-content.png">

===

<img class="small" src="./assets/fails/inverted.png">

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

:::notes
- custom properties
:::

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

# Bundlers / Frameworks

:::notes
- Webpack
- Generate multiple stylesheets with different variables
- vue single file components
- css-in-js
:::

---

:::notes
- app settings theme switch / override
- prefers-contrast
:::
