---
title: "My Accessibility Review Process"
description: ""
author: "Homer Gaines, CPACC"
pubDate: July 09, 2026
tags: [A11y]
draft: false
heroImage: '../../assets/post2.jpg'
---

The accessibility review process is when process flows, content, user experience (UX), user interface (UI) design, and code are reviewed to mitigate possible accessibility issues. Ideally, such reviews begin at the start of the product development process until the launch. Reviews are conducted with the knowledge of the [Web Content Accessibility Guidelines (WCAG)](https://www.w3.org/WAI/WCAG22/Understanding/) and other resources that pertain to accessibility. There are four sections of the WCAG and three testable conformance levels. The four sections are Perceivable, Operable, Understandable, and Robust. The three levels are A, AA, and AAA. With a starting goal to comply with Level AA, the various guidelines within the four sections must be passed. The following high-level descriptions explain the process necessary to evaluate the conformance level of our applications. The reviews are categorized as "Project" and "Product."

## Project Reviews
---
### UX Review
The user experience review aims to look for friction points during the user's flow. This involves but is not limited to reviewing content and UX patterns.

### UX Patterns
Users have mental models that they use to recognize, interpret, and interact with common user interface components. The goal is to ensure disruptive patterns are not introduced.

### UI Review
Just like how mental models are employed to understand how to interact with common processes that involve UI elements, it's important to use design patterns that are familiar to users. This helps with the perception, operation, and understanding of the various UI elements a user may interact with.

### Content
It's important to use plain language when communicating with users. The copy should be informative, meaningful, and clear. An example would be avoiding the heavy use of industry jargon and acronyms.

### Code Review
The development of UI components, app features, and app views impact how users interact with and complete tasks. It's imperative that the code authored does not negatively affect the various methods used to interact with our products. For example, the lack of semantic markup in a form can result in input errors, lost data, and wasted time. Another example would be how the lack of semantic markup could prevent a keyboard user from simply navigating the application. 

Dev teams should include Accessibility Specialist in the code review process by:
- Requesting reviews on Github Pull Requests
- Adding to tickets to provide or evaluate acceptance criteria

### Reporting on Project Reviews
After the review process, recommended fixes are communicated to the responsible party. If the resolution requires minimal effort, the expectation is the fix should be applied before the work is considered complete. However, if the solution requires more research or the level of effort is too great, the issue will be recorded in a ticket, added to the backlog, and prioritized for a later date.

## Product Review
Application development is continuous and changes often. Over time, new features collide with old features,  new design patterns conflict with new patterns, and so on. As a result of these conflicts, accessibility issues can and do arise and negatively affect the application. To keep track of such issues, it's important to conduct regular accessibility audits. I prefer to conduct a quarterly audit and use the results to populate a public-facing Accessibility Conformance Report, using the Voluntary Product Accessibility Template (VPAT®).Read more about [what VPATs are and what they are not.](/accessibility-conformance-reports-setting-expectations) 

### Reporting on Product Reviews
If the solution requires more research or the level of effort is too great, the issue will be recorded in a ticket, added to the backlog, and prioritized for a later date.
