---
title: "Bad Form"
description: ""
author: "Homer Gaines, CPACC"
pubDate: January 15, 2024
tags: [A11y, UX]
draft: false
heroImage: '../../assets/blog-placeholder-2.jpg'
---

Regardless of your industry, customer service can make or break your business. Your website is an extension of your customer service. If you own a business and choose to have a form on your website to communicate with the public, make sure that form works. Statistics show that [76% of users who encounter UX issues](https://www.zippia.com/advice/website-statistics/#Website_User_Behavior_Statistics) on a website will take their money elsewhere. That's because people judge your company and services based on how your website looks and how it functions within seconds. A negative experience either way can lead to a negative perception of your company and services, which can directly impact your bottom line.

I faced a few UX challenges while filling out a form to get a cost estimate. Filling out the form was fairly straightforward until I hit the "Schedule moving consulting" button at the bottom of the form. Immediately after hitting the button, I received the following error in big blue letters...

> "There was a problem with your submission. Please review the fields below."

Cool, but which fields are wrong?

Now, my curiosity has peeked, and I begin to pick apart the form and as a consumer, I began questioning whether or not I wanted to do business with this company.

**Strike 1.**

[None of the inputs had labels](https://www.w3.org/TR/UNDERSTANDING-WCAG20/minimize-error-cues.html), nor did any input have a [visual indicator that something was wrong](https://www.w3.org/TR/UNDERSTANDING-WCAG20/minimize-error-identified.html). This, from a UX and accessibility perspective, is a red flag.

**Strike 2.**

Change blindness is real. It wasn't until after re-reading the form that I noticed the reCAPTCHA message at the bottom.

> The reCAPTCHA was invalid. Go back and try it again.

What reCAPTCHA?

Mind you, while filling out the form and submitting it, there was never an option to engage with reCAPTCHA. In addition to this, using the back button or refreshing the page didn't clear the form or the validation errors.

**Strike 3.**  
As I scanned the page looking for the reCAPTCHA, I noticed the use of the overlay button, which blended in with the blue background of the site. In case you're unaware, [overlays are bad](https://rightbadcode.com/overlays-are-bad) for many reasons and should not be used to "fix" accessibility issues.

It's safe to say that this particular company lost out on my potential business due to issues with their form. If a communication method with the company is broken, what else in their process is broken?

![A section of a website with a form that has 6 inputs without lables and errors that are not apparent.](https://cdn.hashnode.com/res/hashnode/image/upload/v1696088616469/00990348-6375-4469-8eaf-f0f3bbc3c59e.jpeg align="center")

## Correcting the Issues

So, how can these issues be resolved to improve the user experience for all users?

- For starters, get rid of the overlay. Nuke it from orbit and salt the Earth afterward.
- Use semantic markup, especially for elements that require interaction. This will [improve support for non-mouse users](https://www.w3.org/TR/UNDERSTANDING-WCAG20/keyboard-operation-keyboard-operable.html).
- Ensure each interactive element has a [focus ring](https://www.w3.org/TR/UNDERSTANDING-WCAG20/navigation-mechanisms-focus-visible.html), allowing non-mouser users to know where they are in the UI.
- [Add labels to each input](https://www.w3.org/TR/UNDERSTANDING-WCAG20/minimize-error-cues.html) so that users know what each input field represents during their interaction with the form.
- When there's a validation error, there should be a [perceivable indicator](https://www.w3.org/TR/UNDERSTANDING-WCAG20/minimize-error-identified.html) that lets the user know which input is incorrect.
- [CAPTCHAs pose accessibility challenges](https://www.w3.org/TR/turingtest/) and should be reviewed carefully. If the use of a CAPTCHA is necessary, ensure it's working properly and doesn't become a blocker in general.
- And last but not least, get rid of the overlay. Nuke it from orbit and salt the Earth afterward. I put this twice on purpose.

As I stated, anytime someone engages with your website, it's an extension of your customer services. When users face blockers or friction points in your product, this leads to frustration. Frustration leads to dissatisfaction, broken trust, and/or abandonment. Abandonment leads to lost revenue.

While caring about the user experience and accessibility should be the focus, many only pay attention to money. So, if you care about the bottom line, take the time to invest in and improve the UX and accessibility of your products. Your future customers will thank you.
