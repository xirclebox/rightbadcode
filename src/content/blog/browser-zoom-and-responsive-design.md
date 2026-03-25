---
title: "Browser Zoom and Responsive Design"
description: ""
author: "Homer Gaines, CPACC"
pubDate: 
tags: [A11y, UX, UI]
draft: true
heroImage: '../../assets/post2.jpg'
---

As we talk about devices, it's common to refer to screen sizes or breakpoints as "desktop," "tablet," or "mobile." However, these terms represent the device and do not accurately describe how content is rendered. For example, a 13-inch MacBook Pro physically has a small screen, but it has a 1440 x 900 resolution. This is larger than [1024 x 768](https://www.nngroup.com/articles/computer-screens-getting-bigger/#:~:text=The%201024%C3%97768%20became,%C3%97768%2C%20according%20to%20StatCounter.), [which was standard](https://www.nngroup.com/articles/computer-screens-getting-bigger/#:~:text=The%201024%C3%97768%20became,%C3%97768%2C%20according%20to%20StatCounter.) for desktops at one point. And, with [split-screen capabilities](https://support.apple.com/en-us/111788) that divide the screen into smaller parts, users will often [dedicate sections](https://www.microsoft.com/en-us/edge/features/split-screen?form=MA13FJ) to a particular application. Instead, don't think of screens in terms of the type of device but more along the idea of size, such as "large," "medium," and "small." While the user's devices may have a set physical size and pixel dimension, when using browser zoom to increase the size of the interface, the UI must respond accordingly. This response causes the content to appear as if the site is rendering at a smaller breakpoint. For example, here's a screenshot of the WCAG website on a large screen at its normal size, showing two columns.

https://cdn.hashnode.com/res/hashnode/image/upload/v1708397338437/93a40459-0cf4-4b7d-a709-02f61ac2ee5b.png

Here is the same site scaled to 200% using browser zoom. Notice how the UI has taken on the visual characteristics of the smaller breakpoint, arranging the content into one column instead of two. When done successfully, the content is still visible and in a logical reading order.

https://cdn.hashnode.com/res/hashnode/image/upload/v1708397388636/f9db9040-3a49-49cf-bd97-2289b2ada853.png

Media queries

When thinking about media queries, we should consider them as the starting points for that particular view, not the destination.

The WCAG 2.2 provides guidance on how to accommodate browser zoom, which is device agnostic.

WCAG 2.2 Success Critiera

Orientation
https://www.w3.org/WAI/WCAG22/Understanding/orientation

Resize Text
https://www.w3.org/WAI/WCAG22/Understanding/resize-text

Reflow
https://www.w3.org/WAI/WCAG22/Understanding/reflow

Testing

When targeting a particular screen resolution size, that size should be seen as the starting point for testing. For example, observing what the UI looks like at the 800 x 600 breakpoint is the first step. The next step should be to use browser zoom and observe how the UI adjusts. If the UI begins to break or content becomes hard to read, this reveals accessibility issues that should be addressed.
