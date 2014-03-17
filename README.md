rework-plugin-at2x
====================

[![Build Status](https://travis-ci.org/reworkcss/rework-plugin-at2x.png)](https://travis-ci.org/reworkcss/rework-plugin-at2x)

at2x() plugin for rework, formerly included in core

### .at2x()

  Adds `at-2x` keyword to `background` and `background-image`
  declarations to add retina support for images.

```css
.logo {
  background-image: url('component.png') at-2x;
  width: 289px;
  height: 113px
}
```

yields:

```css
.logo {
  background-image: url('component.png');
  width: 289px;
  height: 113px
}

@media all and (-webkit-min-device-pixel-ratio: 1.5) {
  .logo {
    background-image: url("component@2x.png");
    background-size: contain
  }
}
```
