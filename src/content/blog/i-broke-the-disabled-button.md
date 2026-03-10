---
title: "I Broke the Disabled Button"
description: ""
author: "Homer Gaines, CPACC"
pubDate: 2026-02-22
tags: [A11y, UX]
draft: true
heroImage: '../../assets/blog-placeholder-3.jpg'
---

How do you break a disabled button, Gaines? Easy!

This happened many years ago; I was fixing accessibility issues with a form and testing them using VoiceOver. As I tabbed through the UI, I eventually made my way to the disabled Submit button at the bottom of the page. Up to this point, the audit was going great, and the screen reader was announcing everything as expected. But what I didn’t expect was hearing the disabled button being announced as “dimmed.”

Dimmed? That’s not right.

That’s because, to me, “dimmed” didn't tell me the button was disabled. To me, I heard VoiceOver describing the visual state of the button, not the button’s functional state. So, thinking I was doing something great for accessibility, I added an aria-label with the word “Disabled”. Makes sense, right? The word “disabled” now conveys the correct functional state of the button. Yes! Good job, me!

Well, yeah, but not so fast.

I shared my update with some friends who were more proficient at using VoiceOver than I was at the time, and they all collectively smacked me on the hand and said, “Nope! Don't do that!”

No? Why not?

Well, here’s why. VoiceOver users are used to hearing “dimmed” being announced for disabled controls.  But me? Not being aware of this and assuming that VoiceOver was doing something wrong, I injected my own “fix” instead of letting the screen reader do its job. To add insult to injury, I also didn't realize that I had broken internationalization. Instead of the disabled state being announced in the user’s language of choice, they would hear the word “disabled” in English. The reason is that the [aria-label takes precedence](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Reference/Attributes/aria-label) over the element’s accessible label.

So the lessons I learned that day were to be mindful of over-engineering a solution. In this case, using aria to fit my expectation. As the old saying goes, “[No aria is better than bad aria](https://www.w3.org/WAI/ARIA/apg/practices/read-me-first/).” Also, as it pertains to internationalization, aria-labels are not translated when the user switches to a different language. And last, but definitely not least, in spite of my experience with Windows-based screen readers such as [NVDA](https://www.nvaccess.org/) and [JAWS](https://www.freedomscientific.com/products/software/jaws/), I was not aware of the differences with VoiceOver. By involving people who have lived experience, they were able to provide valuable insights and point out details I wasn’t aware of.

I hope you enjoyed this short story and the lessons learned. That way, if you find yourself over-engineering your code to fit your expectations, you can stop, regroup, and remember to right bad code.
