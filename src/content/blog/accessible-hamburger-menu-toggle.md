---
title: "Accessible Hamburger Menu Toggle"
description: ""
author: "Homer Gaines, CPACC"
pubDate: 2026-02-22
tags: [A11y, UX]
draft: true
heroImage: '../../assets/blog-placeholder-3.jpg'
---

As someone who performs regular accessibility audits, I'm exposed to a variety of coding examples and techniques. Some are good, and many are bad. It's the bad ones that I see the most often in coding practices. One such blind spot is when to use an anchor versus a button. The general rule is to use an anchor if it manipulates the URL in any way. For all other actions, use a button. I've come across many hamburger menu toggles that are often constructed in ways that either aren't accessible or are over-engineered.

```
// inaccessible
<span onclick={toggleMenu()}>...</span>
<div onclick={toggleMenu()} aria-label="Menu">...</div>

```

Why are these examples inaccessible?

The main reason is that divs and spans are not focusable elements. Because of this, they are not accessible to keyboards, nor are they included in the [navigation tree structure](https://www.w3.org/WAI/ARIA/apg/patterns/treeview/examples/treeview-navigation/). This prevents anyone who doesn't use or have access to a mouse from interacting with the menu.

Over-engineered Toggles

```
// over-engineered
<a href="#" role="button" onclick={toggleMenu()} title="Menu">...</a>
<a href="#menu" onclick={toggleMenu()} aria-label="Menu">...</a>
<button aria-label="Menu" tabindex="0">...</button>
<input type="checkbox" id="menu" class="menu"/>
```

How are these examples over-engineered?

First off, in all fairness, will these options work? Technically, yes. But, they’re doing way too much.

Example of an accessible Hamburger menu

```
<button type="button" aria-expanded="false" class="hambuger__button">
 ...
</button>
```

...

```
<button type="button" aria-expanded="false" class="hambuger__button">
    <span class="sr-only">Toggle menu</span>
    <span class="hambuger__button-bar" aria-hidden="true"></span>
    <span class="hambuger__button-bar" aria-hidden="true"></span>
    <span class="hambuger__button-bar" aria-hidden="true"></span>
</button>
```

...

```
<button type="button" aria-expanded="false" aria-label="Toggle menu" class="hambuger__button">
    <img src="burger-icon.svg" aria-hidden="true" alt="" class="hambuger__button-icon">
</button>
```
