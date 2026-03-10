---
title: "Over-engineering Aria-Live"
description: ""
author: "Homer Gaines, CPACC"
pubDate: 2026-02-22
tags: [A11y, UX]
draft: true
heroImage: '../../assets/blog-placeholder-3.jpg'
---

Coming in hot!
Rule number one, don't use aria when there's a suitable alternative. Don't agree with me? Cool, but you should probably read the [ARIA Authoring Practices Guide Read Me page](https://www.w3.org/WAI/ARIA/apg/practices/read-me-first/) anyway; just say'n.

'K, now that that's out of the way, there are times when aria attributes are needed. [The problem seems to be](https://webaim.org/projects/million/#aria) understanding exactly when, though. The use and overuse of aria attributes lead to over-engineering, which causes confusion and or issues for people who use assistive tech.

After I spoke about [keyboard traps](https://www.vuemastery.com/conferences/vueconf-us-2023/freakn-keyboard-traps) and other navigation woes related to accessibility at VueConf, one of the attendees approached me and told me about a plugin he and his team use in their Vue-based app called "vue-announcer". The purpose of this component is to add content for a screen reader to announce when the page loads or changes. Puzzled, I asked him why they'd need a plugin when the aria-live attribute does the same thing.

This is what the DOM looks like when the plugin is used.

```
<div class="toast">
    <p>Please add a valid email address.</p>
    <button @click="closeToast">close</button>
</div>
<div id="announcer" class="announcer" aria-atomic="true" aria-live="assertive">content announced by the plugin</div>
```

The component adds a DOM node that's independent of the rest of the content. Using the example above, this additional content isn't necessary since the text "Please add a valid email address." is already exposed to assistive tech. This degrades the user experience by duplicating the content and introducing unnecessary noise.

Here's what the DOM looks like when the aria-live attribute is used.

```
<div class="toast" aria-live="assertive">
    <p>Please add a valid email address.</p>
    <button @click="closeToast">close</button>
</div>
```

https://www.w3.org/WAI/ARIA/apg/practices/read-me-first/
