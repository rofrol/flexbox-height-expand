# flexbox-height-expand

## Problem

Chrome/Safari needs `height` set in percentages for parent, if child has set `height` in percentages. It works in Firefox.

But when `#outer` has `height: 100vh`, then `#bottom` with `height 100%` and `flex-basis: auto` has `height` equal to `100vh` and that is why you can see scrollbar on the screenshot.

![](/screenshot.png)

## Solutions

1. Do not use `height: 100vh` on `#outer` and add `height: 100%;` to `#bottom`.
2. Change `flex-basis: 0` in `#bottom`.

- https://stackoverflow.com/questions/33636796/chrome-safari-not-filling-100-height-of-flex-parent
