### Swap image based on media query

---

This is so cool and self explanatory.

```html

<picture>
  <source media="(min-width:650px)" srcset="images/image-tablet.jpg">
  <source media="(min-width:465px)" srcset="images/image-mobile.jpg">
  <img src="images/image-default.jpg" alt="some image" style="width:auto;">
</picture>

```