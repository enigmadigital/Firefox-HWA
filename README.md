#Firefox HWA

##Detects whether hardware acceleration is in use in Firefox and adds a class of "hwa" or "no-hwa" class to the html tag where appropriate

Firefox on Windows renders elements differently (especially with regards to font-sizes and line-heights) depending on whether hardware acceleration is enabled or not. Also, without hardware acceleration, some CSS3 transforms may not be very performant.

This plugin allows you to identify when its enabled, and change elements accordingly through CSS using the classes applied to `html`.

It does not detect Firefox specifically, however, so we recommend using [Modernizr](http://modernizr.com), [Layout Engine](https://github.com/stowball/Layout-Engine) and [CssUserAgent](http://cssuseragent.org) to conditionally load it.

## Usage example:

```
if (layoutEngine.vendor === 'mozilla' && cssua.ua.desktop === 'windows')
	Modernizr.load('firefox.hwa.min.js');
```

    
Minified version created with Online YUI Compressor: http://www.refresh-sf.com/yui/

---

Copyright (c) 2013 Izilla Partners Pty Ltd    
Licensed under the MIT license (see LICENSE for details)