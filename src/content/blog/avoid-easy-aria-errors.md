---
title: "Avoid Easy Aria Errors"
description: ""
author: "Homer Gaines, CPACC"
pubDate: April 22, 2025
tags: [A11y, Aria, HTML]
draft: false
heroImage: '../../assets/tips.jpg'
---

Far too often, [aria attributes are used incorrectly](https://webaim.org/projects/million/#aria). Most devs, in good faith, probably think they are helping when in reality, over-engineering with [aria can do more harm than good](https://www.w3.org/WAI/ARIA/apg/practices/read-me-first/). When your semantic element is used, it's not necessary to use the `role` attribute. Here are some quick examples where aria attributes are not needed:

## Buttons

When your semantic `button` has a [valid type attribute](https://html.spec.whatwg.org/multipage/form-elements.html#attr-button-type), you don't need to include an aria attribute.

```xml
Do this:
<button type="button" onClick={functionCall}>Close</button>

Don't do this:
<button type="button" role="button" onClick={functionCall} />Close</button>

Don't do this either:
<button role="button" onClick={functionCall} />Close</button>
```

## Links

When using a semantic `anchor`, the role is implied, and therefore, the use of `role="link"` is not needed.

```xml
Do this:
<a href="more-info.html">where to find more info</a>

Don't do this:
<a href="more-info.html" role="link">where to find more info</a>

Don't do this either:
<a href="more-info.html" role="button">where to find more info</a>
```

## Inputs

When your semantic `input` has a [valid type attribute](https://html.spec.whatwg.org/multipage/input.html#attr-input-type), you don't need to include an aria attribute.

```xml
Do this:
<input type="checkbox" id="confirmed" name="isConfirmed">

Don't do this:
<input type="checkbox" role="checkbox" id="confirmed" name="isConfirmed">
```
