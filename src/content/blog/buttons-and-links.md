---
title: "Buttons and Links"
description: ""
author: "Homer Gaines, CPACC"
pubDate: 
tags: [A11y, UX]
draft: true
heroImage: '../../assets/blog-placeholder-3.jpg'
---

I regularly see spans and divs with an onClick used to trigger the action. This works with a mouse but lacks the various requirements for keyboard support. If you've attended my accessibility talks, then you've heard me mention when to use a button versus a link because It's a common issue that I see when conducting accessibility audits and code reviews.

Use links when explicitly changing the URL

```
<a href="a11y.html">Learn more about A11y</a>
```

Use buttons when the URL doesn't change

```
<button type="button">Open Modal</button>
<button type="button" aria-label="Close Modal" />
<button type="button" onClick={clickme()} aria-label="Icon">{svg}</button>
```

Examples

```
<span onClick={gotoSomeURL()}>NOPE!</span>
<span role="button" tabindex="0">Not the best either</span>
<i onClick={clickme()} tabindex="0">...</i>
```
