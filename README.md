rework-plugin-at2x
====================

[![Build Status](https://travis-ci.org/reworkcss/rework-plugin-at2x.png)](https://travis-ci.org/reworkcss/rework-plugin-at2x)

at2x() plugin for rework, formerly included in core

### .at2x()

  Adds `at-2x` keyword to `background` and `background-image`
  declarations to add retina support for images.

  If the rule defines a `background-size`, it will be respected,
  otherwise, the plugin will try to detect real image size and use it.

  Optionally you can define a base directory for the images
  with `at2x({ baseDir: 'assets/images' })`.

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
    background-size: 100px 50px;
  }
}
```
