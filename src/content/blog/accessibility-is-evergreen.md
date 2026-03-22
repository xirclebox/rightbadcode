---
title: "Accessibility is Evergreen"
description: ""
author: "Homer Gaines, CPACC"
pubDate: 
tags: [A11y, UX]
draft: true
heroImage: '../../assets/blog-placeholder-3.jpg'
---

Years ago, I had a VP ask my team and me to reduce the size of the images on our websites. The VP was using Lighthouse, which always suggested the images could be made smaller. To demonstrate why the use of this tool was presenting a false negative, we scheduled a demo. During this demo, we took one of our current production images and ran it through Lighthouse. As expected, Lighthouse advised us to reduce the image size. After a couple of rounds, the image compression was so bad that it was nowhere near the quality fit for the website, let alone the brand, and yet, Lighthouse still advised us to reduce the image size even more. This is because Lighthouse takes a snapshot of the current state without any record of the previous scan or additional context. Accessibility audits are similar. They are a snapshot of the current state of your product and lack any additional context. For example, a full audit of your product is being conducted. This audit was planned and scheduled, all the teams are aware it's happening. In parallel, the teams continue to ship updates and new features.
