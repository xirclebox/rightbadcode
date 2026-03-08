---
title: "Getting Started with Accessibility"
description: ""
author: "Homer Gaines, CPACC"
pubDate: 2026-02-22
tags: [A11y, UX]
draft: true
---

I'm often asked a couple of questions: "How do I get started with accessibility?" and "What are some good resources for learning about accessibility?" Because of the vast amount of information available, digging into the topic of accessibility can feel overwhelming. That's because it crosses disciplines. For instance, a Copywriter will view accessibility differently than a Front-end Engineer. So, understanding how it supports your interests is a tough question to answer unless we're diving directly into your role.

WCAG

Every skill that is learned has fundamental rules that serve as the foundation. I like to direct people to the Web Content Accessibility Guidelines, or WCAG for short. This is where you'll find all you need to know about the various guidelines governing how products should be built to be more inclusive. The WCAG 2.1 is the current version, with version 2.2 close behind. The current version is broken into five principles: Perceivable, Operable, Understandable, Robust, and Conformance. These principles each have varying guidelines (success criteria) that total 78. Each of these 78 success criteria represents a conformance level. There are three conformance levels in total. It's important to know and understand that your product only needs to comply with the success criteria that apply to your product. For example, if your product doesn't contain live video, you don't have to worry about Success Criterion 1.2.4 Captions (Live)

HTML

Hypertext Markup Language sets the foundation for web-based products. Understanding how to properly structure your HTML document will offer tremendous accessibility support. For example, learning how the <div> element is not a focusable element and, therefore, should not be used as a button because doing so can prevent keyboard users from accessing the control. Learning about the use of the various HTML elements and how to correctly apply them will help avoid accessibility issues that arise due to semantic issues.

Screen Readers

Whether you are a Mac, PC, or Linux user, screen readers are available. They are a very useful tool for everyone. There's a misconception that only blind people use screen readers, which isn't the case. Learning how to use screen readers can help with testing your code as well as show how the accessible user experience differs from that of someone who uses a mouse, for example.

Apple

VoiceOver

PC

NVDA

JAWS

Linux

Orca

Design Tools

https://w3.org/WAI/WCAG21/quickref/#top

https://dequeuniversity.com/screenreaders/survival-guide

https://dequeuniversity.com/screenreaders/voiceover-keyboard-shortcuts

https://webaim.org/resources/contrastchecker/

https://a11ysupport.io

https://deque.com/blog/category/accessibility-resources-for-developers/
