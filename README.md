# Firefox HWA

### Detects whether hardware acceleration is in use in Firefox and adds a class of "hwa" or "no-hwa" to the html tag where appropriate

Firefox on Windows renders elements differently (especially with regards to font-sizes and line-heights) depending on whether hardware acceleration is enabled or not. Also, without hardware acceleration, some CSS3 transforms may not be very performant.

This plugin allows you to identify when hardware acceleration is enabled, and change elements accordingly through CSS using the classes applied to `html`.

It requires [Layout Engine](https://github.com/stowball/Layout-Engine) and [CssUserAgent](http://cssuseragent.org) to be included before it to work

#### Usage example:

```html
<script src="layout.engine.min.js"></script>
<script src="cssua.min.js"></script>
<script src="firefox.hwa.min.js"></script>
```

```css
.hwa .foo {
  // do something
}

.no-hwa .foo {
  // do something else
}
```

---

Copyright (c) 2013 Izilla Partners Pty Ltd    
Licensed under the MIT license (see LICENSE for details)  
Minified version created with Online YUI Compressor: http://www.refresh-sf.com/yui/