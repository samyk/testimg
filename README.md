Latest Chrome blocks downloading any images on my (`samyk`) [github repos](https://github.com/samyk) when Right Clicking->Save Image As, but does not affect other repos using the same exact image. Specifically affects images on https://raw.githubusercontent.com/samyk

Chrome bug filed: https://bugs.chromium.org/p/chromium/issues/detail?id=954791

Example:
- original: https://raw.githubusercontent.com/Khan/graphie-to-png/master/static/images/throbber.gif
- mine: https://raw.githubusercontent.com/samyk/testimg/master/throbber.gif

```
tigerblood:/tmp$ curl -so - https://raw.githubusercontent.com/Khan/graphie-to-png/master/static/images/throbber.gif | sha256sum
878f766cb7a7fbde6e1a4f53fc65f6e35b066618682553743f2edb34c223316b  -
tigerblood:/tmp$ curl -so - https://raw.githubusercontent.com/samyk/testimg/master/throbber.gif | sha256sum
878f766cb7a7fbde6e1a4f53fc65f6e35b066618682553743f2edb34c223316b  -
```

Tested on 74.0.3729.91 (Official Build) beta (64-bit), macOS 10.13.6
Tested by others, macOS High Sierra v 10.13.6 & Chrome 73.0.3683.103 (Official Build) (64-bit) 
