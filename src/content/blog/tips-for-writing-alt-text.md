---
title: "Tips for Writing Alt Text"
description: ""
author: "Homer Gaines, CPACC"
pubDate: 2026-02-22
tags: [A11y, UX]
draft: true
---

Alt text, also known as "alt descriptions" or "alternative text," is used to describe images on websites and other digital media. When asked, I like to tell the person to imagine they are describing an image to someone over the phone. Alt descriptions are [an essential accessibility feature](https://www.w3.org/TR/WCAG21/#text-alternatives) that can significantly improve the usability of your website for people with disabilities. Here are some tips for writing helpful alt descriptions:

1. **Consider the image's purpose:**  
   Ask yourself why the image is included on the page and what information it conveys. This will help you create an effective alt description.
2. **Keep it brief:**  
   Alt text should be brief and to the point, usually no more than a sentence or two.
3. **Descriptive the image:**  
   Alt text should provide a clear and accurate description of the image by including details such as the subject matter, colors, and other relevant information.
4. **Don't include unnecessary details:**  
   While it's important to be descriptive, avoid including unnecessary details that don't add value.
5. **Avoid subjective language:**  
   Stick to objective descriptions that are factual and free of bias.
6. **Don't use the filename as the alt text:**  
   The filename of an image is often not descriptive and may not provide any useful information about the image. Instead, use a meaningful alt description.
7. **Don't start with “screenshot”, "image", "gif", “jpeg”, "image of" or "picture of":**  
   Screen readers already announce that an image is present, so these phrases and labels are redundant and add unnecessary noise.
8. **And last but not least, test your alt text:**  
   Test your alt descriptions to ensure they are read aloud by screen readers and convey the intended meaning.

## Implementation Examples

```plaintext
✅ Do this:
<img alt=”A black German Shepherd puppy looking up.” src=”puppy.jpg” />

❌ Don't do this:
<img src=”puppy.jpg” />
Screen reader will announce the image name and extension

❌ Don't do this:
<img alt="puppy.jpg" src=”puppy.jpg” />
Screen reader will also announce the image name and extension

❌ Don't do this either:
<img alt="puppy" src=”puppy.jpg” />
"puppy" ? cool story bro
```

## WCAG 2.1 Success Criteria

- [https://www.w3.org/TR/WCAG21/#text-alternatives](https://www.w3.org/TR/WCAG21/#text-alternatives)
- [https://www.w3.org/WAI/tutorials/images/](https://www.w3.org/WAI/tutorials/images/)

## Screen Readers

- JAWS: [https://www.freedomscientific.com/products/software/jaws/](https://www.freedomscientific.com/products/software/jaws/)
- NVDA: [https://www.nvaccess.org/](https://www.nvaccess.org/)
- VoiceOver: [https://support.apple.com/guide/voiceover/welcome/mac](https://support.apple.com/guide/voiceover/welcome/mac)
