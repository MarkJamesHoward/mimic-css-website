---
title: mimic-css
---

**mimic-css** is a design system that allows you use standard CSS styles within the class attribute ALONG with Media Queries and Modifiers. From this you gain the benefits of using a design system but without the downside of losing your CSS knowledge
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
```


