---
layout: ../layouts/mdLayout.astro
title: mimic-css
---

## Design System

In order to provide consistency across a website we provide a set of standard values taht can be used rather than specific pixel values. There are 6 values that are used across the board **xs, sm, md, lg, xl and 2xl**

```html
<div class="padding-top:md">Some Text</div>
```

**becomes**

```css
.padding-top\:md {
  padding-top: 8px;
}
```

## Design systemmappings

These specifiers will map to different **Pixel Values** depending upon the usage.

So for **Fonts** you'll have the below mapping:

<ul>
<li>xs:     8px</li>
<li>sm:     12px</li>
<li>md:     16px</li>
<li>lg:     24px</li>
<li>xl:     48px</li>
<li>2xl:    92px</li>
</ul>

Whereas for **Padding** the mappings will be different:

<ul>
<li>xs:     2px</li>
<li>sm:     4px</li>
<li>md:     8px</li>
<li>lg:     20px</li>
<li>xl:     50px</li>
<li>2xl:    200px</li>
</ul>

### An example for Padding

```html
<div class="padding-top:md">Some Text</div>
```

**becomes**

```css
.padding-top\:md {
  padding-top: 8px;
}
```

### And then for Font Size you will see

```html
<div class="font-size:md">Some Text</div>
```

```css
.font-size\:md {
  font-size: 16px;
}
```

```js
export const Sizes = {
  xs: "xs",
  sm: "sm",
  md: "md",
  lg: "lg",
  xl: "xl",
  xl2: "2xl",
};

export const BorderRadius = {
  xs: "2px",
  sm: "5px",
  md: "10px",
  lg: "20px",
  xl: "30px",
  xl2: "50px",
};

export const FontWeights = {
  xs: "200",
  sm: "300",
  md: "400",
  lg: "600",
  xl: "800",
  xl2: "900",
};

export const FontSizes = {
  xs: "8px",
  sm: "12px",
  md: "16px",
  lg: "24px",
  xl: "48px",
  xl2: "92px",
};

export const BoxShadowSizes = {
  xs: "2px",
  sm: "4px",
  md: "8px",
  lg: "20px",
  xl: "50px",
  xl2: "200px",
};

export const PaddingSizes = {
  xs: "2px",
  sm: "4px",
  md: "8px",
  lg: "20px",
  xl: "50px",
  xl2: "200px",
};

export const GapSizes = {
  xs: "1px",
  sm: "2px",
  md: "4px",
  lg: "6px",
  xl: "8px",
  xl2: "10px",
};

export const BorderSizes = {
  xs: "1px",
  sm: "2px",
  md: "4px",
  lg: "6px",
  xl: "8px",
  xl2: "10px",
};

export const MarginSizes = {
  xs: "2px",
  sm: "4px",
  md: "8px",
  lg: "20px",
  xl: "50px",
  xl2: "200px",
};

export const GenericSizes = {
  xs: "2px",
  sm: "8px",
  md: "20px",
  lg: "40px",
  xl: "60px",
  xl2: "100px",
};
```
