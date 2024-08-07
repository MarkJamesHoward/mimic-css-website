---
layout: ../layouts/mdLayout.astro
title: mimic-css
---

<!-- **mimic-css** is a design system that allows you use standard CSS styles within the class attribute ALONG with Media Queries and Modifiers. From this you gain the benefits of using a design system but without the downside of losing your CSS knowledge
at the same time

So you are enabled to write standard CSS such as `display:flex` and apply a media query inline within the class e.g.

```html
<div class="large?display:flex">Some Text</div>
```

Which will result in the below class being generated for you and ensuring that the flex container is only applied when the screen size is greater than 1280px wide

```css
@media (min-width: 1280px) {
  .large\?display\:flex {
    display: flex;
  }
}
``` -->
<!-- 
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
``` -->
<!-- 
## Pseudo Classes

You can also apply pseudo class like **hover** and **focus** inline with the class attribute

```html
<div class="background-color:blue:hover">Some Text</div>
```

Which will create a class for you like this

```css
.background-color\:blue\:hover:hover {
  background-color: blue;
}
``` -->

<!-- ## Install:

`npm install --save-dev mimic-css`

mimic-css is a development time process that watches for file changes to your web pages and create classes from them. -->

<!-- ## Usage

`npx mimic`

The app will search in the current folder (and all subfolders) for .html, .ts, .js and .astro files.
Ouput will be sent to the file mimic.css which you can link:

```html
<link rel="stylesheet" href="mimic.css" />
```

You can override where to base your scan for web pages using the -i flag

```
npx mimic-css -i ./src
```

You can also override where to output the generated CSS file using the -o flag

```
npx mimic-css -o ./styles/customname.css
```

Other options:

- i: { type: "string", default: "./", alias: "input" },
- o: { type: "string", default: "./mimic.css", alias: "output" },
- e: { type: "string", default: "", alias: "exclude" },
- l: { type: "boolean", default: false, alias: "lit" }, -->

<!-- ## Design systemmappings

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
</ul> -->

<!-- ### An example for Padding

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
``` -->

Normal CSS will remain unchanged (bar a space inserted)

**So the below:**

```html
<div class="display:flex">Some Text</div>
```

**Becomes:**

```css
.display\:flex {
  display: flex;
}
```

<!-- ## Media Breakpoints

The 5 options we have for specifying media breakpoints are below:

<ul>
<li>extrasmall</li>
<li>small</li>
<li>medium</li>
<li>large</li>
<li>extralarge</li>
</ul> -->

<!-- ## Configuration

By default mimic-css will search ".html", ".js", ".astro", "ts" files for classes to process

In order to serch additional files we can create a file named 'mimic.config.mjs'

So to also search javascript and react files we would create the below:

```js
let config;

export default config = {
  extensions: [".html", ".js", ".astro", "ts"],
}; -->
```

<!-- ## Lit Integration

To include CSS in LitElements a good approach to take is Constructable Style Sheets. These require the CSS to be in a JS string and mimic-css provide this output in the file **mimic.css.js** for us when using the -l flag.

The generated file can be imported to a LitElement using the below syntax

```javascript
import { TWStyles } from "../styles/mimic.css.js";

export class Header extends
  LitElement { static styles = [css``, TWStyles];
``` -->
