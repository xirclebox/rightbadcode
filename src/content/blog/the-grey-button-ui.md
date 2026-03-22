---
title: "The Grey: Button UI"
description: ""
author: "Homer Gaines, CPACC"
pubDate: 
tags: [A11y, UX]
draft: true
heroImage: '../../assets/blog-placeholder-3.jpg'
---

The question, “Does the hover state of a button need to be accessible?”

The answer is " no ", according to the WCAG.

> The pointer itself, via its location, is the indicator of whether the user is hovering on a component. Therefore, additional author-supplied visual treatments for hover are not "required to identify" the hover state. Those treatments can be considered supplemental and do not themselves need to contrast 3:1 against the background. - [Non-text Contrast (Level AA) - first paragraph](https://www.w3.org/WAI/WCAG21/Understanding/non-text-contrast.html#:~:text=Therefore%2C%20additional%20author%2Dsupplied%20visual%20treatments%20for%20hover,say%20that%20other%20hover%20effects%20are%20discouraged.)

Now, before you go skipping off, ready to leave your hover states in limbo, take a look at this:

> The key consideration for any hover effect is that it does not cause a component itself to lose sufficient contrast against adjacent colors, or cause the visual indicators for other states, such as focus or selection, to lose sufficient contrast. - [Non-text Contrast (Level AA) - second paragraph](https://www.w3.org/WAI/WCAG21/Understanding/non-text-contrast.html#:~:text=However%2C%20other%20users%20may%20find%20strong%20hover,focus%20or%20selection%2C%20to%20lose%20sufficient%20contrast.)

Beyond Compliance

Let me ask you one question: Why wouldn’t you want your buttons to be accessible in any circumstance?

What is the purpose of the button? We want the user to interact with it in order to complete some task. We do not have control over that person’s choice of how to interact with that element. Not all users have a mouse. And not all mouse users have the fine motor skills to control the device accurately or consistently.

## Possible Example:

A user with low color vision using methods to navigate other than a mouse or keyboard, such as eye tracking, sip and puff, or a pointer stick.

## Edge Detection

Someone with low visual acuity or contrast sensitivity may not be able to perceive the control if the hover state does not have enough contrast or if the contrast of the outline of a UI element is not strong enough.

[https://www.ncbi.nlm.nih.gov/books/NBK580542/#:~:text=Contrast%20sensitivity%20(CS)%20is%20the,and%20clinical%20implications%20of%20CS](<https://www.ncbi.nlm.nih.gov/books/NBK580542/#:~:text=Contrast%20sensitivity%20(CS)%20is%20the,and%20clinical%20implications%20of%20CS>).

## WCAG 2.2

- Non-text Contrast (Level AA) - https://www.w3.org/WAI/WCAG21/Understanding/non-text-contrast.html
- Contrast (Minimum) (Level AA) - https://www.w3.org/WAI/WCAG21/Understanding/contrast-minimum
- Contrast (Enhanced) (Level AAA) - https://www.w3.org/WAI/WCAG21/Understanding/contrast-enhanced

## COGA

- list itemClearly Identify Controls and Their Use - https://www.w3.org/WAI/WCAG2/supplemental/patterns/o1p05-clear-controls/
- Help Users Understand What Things are and How to Use Them - https://www.w3.org/WAI/WCAG2/supplemental/objectives/o1-understandable/
