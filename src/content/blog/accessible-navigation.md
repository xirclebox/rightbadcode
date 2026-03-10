---
title: "Accessible Navigation"
description: ""
author: "Homer Gaines, CPACC"
pubDate: March 31, 2025
tags: [A11y, UX]
draft: false
heroImage: '../../assets/blog-placeholder-2.jpg'
---

When building a nav, avoid using divs with aria attributes like this...

```xml
<div role="list">
 <a href="foo.html" role="list-item">Link Label</a>
</div>
```

Instead, author your navigation starting with this bare-bones solution. Using semantic markup exposes the navigation structure to a wider range of assistive tech.

```xml
<nav>
 <ul>
   <li>
     <a href="#"">Nav item 1</a>
   </li>
 </ul>
</nav>
```

Using the correct aria attributes in conjunction with the semantic elements will provide a more robust and informed experience for assistive tech users.

```xml
<h2 id="primaryMenu" class="sr-only">Primary Menu</h2>
<nav aria-labelledby="primaryMenu">
 <ul role="menu">
   <li>
     <a href="foo.html" role="menuitem">Link Label</a>
  </li>
 </ul>
</nav>
```

```xml
<nav aria-label="Main navigation">
 <ul role="menu">
   <li>
     <a href="#" role="menuitem">Nav item 1</a>
   </li>
 </ul>
</nav>
```
