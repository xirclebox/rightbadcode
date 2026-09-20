---
title: "CSS Media Features and Privacy: A Word of Caution"
description: ""
author: "Homer Gaines, CPACC"
pubDate:
tags: [A11y, CSS, Privacy]
draft: true
heroImage: "../../assets/post2.jpg"
---

Working with medical software over the years has made me aware of potential ways a person's protected info could be accidentally exposed through practical means. <a href="https://rightbadcode.com/aria-labels-and-privacy-a-word-of-caution/" rel="noopener noreferrer" target="_blank">My first word of caution</a> was about how unique `aria-labels` could expose personally identifiable information (PII) in analytic software. Something I've been thinking about as of late is how CSS `@media` features could be used to infer a person's disability. Now, before we get too deep in this, let me start by saying that someone's <a href="https://www.ada.gov/topics/intro-to-ada/" rel="noopener noreferrer" target="_blank">disability status is a protected class</a> under the Americans with Disabilities Act (ADA) and a special category of personal data under the <a href="https://gdpr-info.eu/art-9-gdpr/" rel="noopener noreferrer" target="_blank">General Data Protection Regulation (GDPR) Article 9</a>. Inferring a protected status from the user's settings or behavioral patterns and acting on that knowledge is highly **unethical** and **illegal**. The content within this post should not be used a blueprint for such behavior. Now, with that being said, I'm sure anyone working in accessibility has been asked or has heard this question...

> "Can't we just check to see if someone is using assistive tech?"

TL;DR answer ... **No**.

The reason is because <a href="https://www.w3.org/TR/design-principles/#do-not-expose-use-of-assistive-tech" rel="noopener noreferrer" target="_blank">browsers don't expose the use of assistive tech</a> to protect the user's privacy and to prevent discrimination. In addition to this, assistive tech, such as screen readers, don't run in the browser so there's nothing to detect.

I will acknowledge the fact that the person asking may truly not know or understand and their motivation behind asking is benign. Unfortunately, in my experience, it's asked in conjunction with pushing back on having to make something accessible. Typically because the person pushing back is hyper-focused on the disability related to the error and are convinced that a user with said disability does not use the product.

For example, if the UI contains a bunch of icon buttons that are missing accessible labels. A Blind screen reader user will not understand what those buttons mean. This prompts the person who is pushing back to say something like "Can't we just detect if someone is using a screen reader?" The thought is, if it's possible to add a band-aid "fix" or provide and alternative experience, do that instead of fixing the issue correctly. This takes on a "separate-but-equal" vibe which is similar to the pattern that lands <a href="https://www.lflegal.com/category/digital-accessibility/overlays/" rel="noopener noreferrer" target="_blank">overlay vendors in hot water</a>.

Another motivating factor is that the person pushing back wants to collect data to try and prove the need to make the product accessible is not necessary.

## The potential risk

Knowing that we can't detect assistive tech directly, using JavaScript, there are CSS features that map to current Success Criteria (SC) in the Web Content Accessibility Guidelines (WCAG) that can be detected.

For example, this script checks the value of the `prefers-reduced-motion` feature which is related to <a href="https://www.w3.org/WAI/WCAG22/Understanding/animation-from-interactions" rel="noopener noreferrer" target="_blank">WCAG SC 2.3.3 Animation from Interactions</a>. The `console.log`, for demo purposes, prints `reduce` or `no-preference` depending on the state.

```
// Example code for science only. Don't use this in prod

(function () {
  var QUERY = "(prefers-reduced-motion: reduce)";
  var mediaQuery = window.matchMedia(QUERY);

  function report(matches) {
    console.log("prefers-reduced-motion:", matches ? "reduce" : "no-preference");
  }

  report(mediaQuery.matches);

  function onChange(event) {
    report(event.matches);
  }

  if (typeof mediaQuery.addEventListener === "function") {
    mediaQuery.addEventListener("change", onChange);
  } else {
    mediaQuery.addListener(onChange);
  }
})();
```

Take this scenario. Say it's a small team and they use analytics to inform their design decisions. They use this method to gain insight into how their visitors feel about the use of parallax. Before user testing became more common, my team used anonymous data to determine if our users were interacting with the tooltips at all. Turns out they weren't. As a result, we pulled tooltips from the UI and changed the UX pattern.

However, keeping the original question about "can't we just check?" in mind, collecting data like this crosses the line when the state of `prefers-reduced-motion` is used to assume the use of assistive tech and/or pairing it with a user to infer that user's protected status. I've seen some weak and unsuccessful attempts to sidestep accessibility, and this argument is just as loose because it's speculative. Just because a person has this feature active does not mean they have a vestibular disorder. They could be someone who simply can't stand parallax animations.

Though the use of media features is very common in CSS and alone do not expose PII. It's the connecting of the dots to expose PII that is illegal. Staying aware of how PII can be exposed and understanding the risks can help protect your users, yourself, and the integrity of your application.

---

## Accessibility-related media features

Here's a list of `@media` features that map to WCAG SC

- [Prefers-reduced-motion](#prefers-reduced-motion)
- [Prefers-contrast](#prefers-contrast)
- [Forced-colors](#forced-colors)
- [Update](#update)
- [Pointer](#pointer)
- [Monochrome](#monochrome)

---

<div class="card__post-content">

### Prefers-reduced-motion

**Feature:** `@media (prefers-reduced-motion: <value>)`

A user would enabled this system setting to reduce motion, to avoid vestibular discomfort, seizures, migraines, or being distracted.

#### WCAG reference

- <a href="https://www.w3.org/WAI/WCAG22/Understanding/animation-from-interactions" rel="noopener noreferrer" target="_blank">2.3.3 Animation from Interactions</a>

#### CSS Reference

- <a href="https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/At-rules/@media/prefers-reduced-motion" rel="noopener noreferrer" target="_blank">prefers-reduced-motion</a>

</div>

---

<div class="card__post-content">

### Prefers-contrast

**Feature:** `@media (prefers-contrast: <value>)`

The user would enable this setting if they prefer higher or lower contrast due to low vision or contrast sensitivity.

#### WCAG reference

- <a href="https://www.w3.org/WAI/WCAG22/Understanding/contrast-enhanced" rel="noopener noreferrer" target="_blank">1.4.6 Contrast Enhanced</a>

#### CSS Reference

- <a href="https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/At-rules/@media/prefers-contrast" rel="noopener noreferrer" target="_blank">prefers-contrast</a>

</div>

---

<div class="card__post-content">

### Forced-colors

**Feature:** `@media (forced-colors: <value>)`

This is used to allow the user to define colors at the OS level to override colors with a system palette (e.g., Windows High Contrast Mode).

#### WCAG reference

- <a href="https://www.w3.org/WAI/WCAG22/Understanding/use-of-color" rel="noopener noreferrer" target="_blank">1.4.1 Use of Color</a>

- <a href="https://www.w3.org/WAI/WCAG22/Understanding/contrast-minimum" rel="noopener noreferrer" target="_blank">1.4.3 Contrast Minimum</a>

- <a href="https://www.w3.org/WAI/WCAG22/Understanding/contrast-enhanced" rel="noopener noreferrer" target="_blank">1.4.6 Contrast (Enhanced)</a>

- <a href="https://www.w3.org/WAI/WCAG22/Understanding/non-text-contrast" rel="noopener noreferrer" target="_blank">1.4.11 Non-text Contrast</a>

#### CSS Reference

- <a href="https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/At-rules/@media/forced-colors" rel="noopener noreferrer" target="_blank">Forced-colors</a>

</div>

---

<div class="card__post-content">

### Update

Feature: `@media (update: <value>)`

This applies to animation viability on E-ink and low-refresh devices.

#### WCAG reference

- <a href="https://www.w3.org/WAI/WCAG22/Understanding/pause-stop-hide" rel="noopener noreferrer" target="_blank">2.2.2 Pause, Stop, Hide</a>

#### CSS Reference

- <a href="https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/At-rules/@media/update" rel="noopener noreferrer" target="_blank">Update</a>

</div>

---

<div class="card__post-content">

### Pointer

Feature: `@media (pointer: <value>)`

Related to target sizing and hover-dependent UI which can impact users with limited motor control.

#### WCAG reference

- <a href="https://www.w3.org/WAI/WCAG22/Understanding/content-on-hover-or-focus" rel="noopener noreferrer" target="_blank">1.4.13 Content on Hover or Focus</a>

- <a href="https://www.w3.org/WAI/WCAG22/Understanding/target-size-enhanced" rel="noopener noreferrer" target="_blank">2.5.5 Target Size (Enhanced)</a>

- <a href="https://www.w3.org/WAI/WCAG22/Understanding/target-size-minimum" rel="noopener noreferrer" target="_blank">2.5.8 Target Size (Minimum)</a>

#### CSS Reference

- <a href="https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/At-rules/@media/pointer" rel="noopener noreferrer" target="_blank">Pointer</a>

</div>

<div class="card__post-content">

---

### Monochrome

Feature: `@media (monochrome <integer> )`

Color as sole information carrier

#### WCAG reference

- <a href="https://www.w3.org/WAI/WCAG22/Understanding/use-of-color" rel="noopener noreferrer" target="_blank">1.4.1 Use of Color</a>

#### CSS Reference

- <a href="https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/At-rules/@media/monochrome" rel="noopener noreferrer" target="_blank">monochrome</a>

</div>
