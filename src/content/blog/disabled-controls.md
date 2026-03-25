---
title: "Disabled Controls"
description: ""
author: "Homer Gaines, CPACC"
pubDate: 
tags: [A11y, UX, UI]
draft: true
heroImage: '../../assets/post2.jpg'
---

There's no shortage of opinions about what to do with disabled controls like buttons in the UI. This post may even attract some negative comments, but whatever. Show or hide the disabled control; people fall on both sides of the fence. However, regardless of which side of the fence you're on, one thing still applies — the control itself has to be accessible.

Sticking with buttons as an example. If the button is hidden, well, there's not much there to perceive until the condition that makes it visible is met. But for those visible yet greyed-out buttons, according to SC 1.4.11 Non-text Contrast in the WCAG, disabled elements do not need to meet the contrast requirements.

This is trash for discoverability and for anyone with low vision. A disabled control that doesn't meet the minimum requirement might as well not be visible at all then.

The goal, make disabled controls discoverable

The use case

The user is a keyboard user

The user has low vision

The user does not use a screen reader

The legacy method for disabling a control is to add the disabled attribute to the element and call it a day. While this does disable the control, it also prevents

Don't use the disabled attribute. This will prevent the control from being focusable via keyboard.

Why? The browser-controlled disabled state doesn't provide enough contrast Allowing for keyboard access allows for discoverability for user who have low vision and / or not using a screen reader.
