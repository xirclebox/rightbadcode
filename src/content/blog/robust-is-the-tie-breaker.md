---
title: "Robust is the tie breaker"
description: ""
author: "Homer Gaines, CPACC"
pubDate: 2026-02-22
tags: [A11y, UX]
draft: true
heroImage: '../../assets/blog-placeholder-3.jpg'
---

I was testing a tooltip component the other day, and I noticed something. Testing with my screen reader and using the keyboard to navigate, when the tooltip was in focus, the label was announced as expected. However, my automated tests failed because the button didn’t have an accessible name. So I took a look at the code so I could see what was going on.

Here’s the basic setup. To support keyboard navigation, the trigger was a semantic button with an SVG icon. The tooltip label text was in a span just below the button in the DOM, which appeared when the button was in focus or on hover. So far, so good. The button had an aria-describedby that was tied to the id of the tooltip label span. Technically, it works, but my eyebrow still went up, and here’s why. The aria-describedby attribute creates an accessible name by referencing visible text located in a different element in the DOM. “Visible” is the key word here. While the button and label are associated correctly, the label is not a visible text element. The correct attribute to use in this case is aria-labelledby. By using the aria-labelledby attribute instead, it provides an accessible name for elements that don’t have visible text, such as the button.

Ok, so the test doesn’t pass but it still works, so what’s the problem?

So, when the assistive tech works as it should but the tests fail, what should you do?
