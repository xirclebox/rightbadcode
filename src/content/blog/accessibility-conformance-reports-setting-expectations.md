---
title: "Accessibility Conformance Reports: Setting Expectations"
description: "An Accessibility Conformance Report (ACR), more commonly referred to as a VPAT® (Voluntary Product Accessibility Template), is a report that’s typically completed by an Accessibility Professional. It’s an important document to have, and companies should understand what they are and what they are not."
pubDate: "January 19, 2026"
heroImage: "../../assets/acr-expectations.jpg"
---

| Acronym | Definition                             |
| ------- | -------------------------------------- |
| ACR     | Accessibility Conformance Report VPAT® |

Voluntary Product Accessibility Template

An Accessibility Conformance Report (ACR), more commonly referred to as a VPAT® (Voluntary Product Accessibility Template), is a report that’s typically completed by an Accessibility Professional. It’s an important document to have, and companies should understand what they are and what they are not.

For organizations looking to purchase software, technology, or services, ACRs based on the VPAT provide a standardized way to determine whether a product meets their accessibility requirements before committing to a purchase. Many government agencies and large companies are legally required to procure accessible technology, so these reports help them make informed decisions.

Produced by the Information Technology Industry Council (ITI), there are currently five variations of the VPAT to choose from:

- VPAT 2.5Rev EU (April 2025)
- VPAT 2.5Rev INT (April 2025)
- VPAT 2.5Rev 508 (April 2025)
- VPAT 2.5Rev WCAG (April 2025)
- VPAT 2.5Rev Change Tracking (April 2025)

Depending on which template you choose, within each VPAT® are criteria that align with the Web Content Accessibility Guidelines (WCAG), Section 508, or EN 301 549. Each of these criteria is evaluated and given a conformance level of “Supports”, “Partially supports”, Does not support”, “Not applicable”, or “Not evaluated”. The result of completing a VPAT is known as an ACR.

| Criteria                         | Conformance Level | Remarks and Explanations |
| -------------------------------- | ----------------- | ------------------------ |
| 1.1.1 Non-text Content (Level A) | Supports          |

For vendors, this is great because having an ACR shows a commitment to accessibility even when all the criteria aren’t fully met. Being upfront about your product’s limitations is often better than making vague or misleading accessibility claims. This level of transparency also helps to build trust and credibility. ACRs serve as documentation that organizations are meeting accessibility standards. This becomes crucial if accessibility issues lead to complaints or legal action, as the report shows what is known and discloses specific gaps where the product doesn’t meet accessibility standards.

While it’s possible to count the number of “Supports” vs. “Does not support”, and use those values as a metric to track conformance, the ACR should not be viewed as a report card with a passing or failing numerical score. Yes, a company can strive to maintain support levels like “60% Supports", “30% Partially Supports", and “10% Does Not Support”, but it’s not suitable for tracking individual accessibility errors.

For example, say an accessibility audit reveals that 20 images out of 100 are missing alt text. The corresponding conformance level would be recorded as “Partially Supports”. It’s not horrible. I’ve seen worse, but there’s definitely room for improvement. So the team gets to work, and the next audit reveals that only 1 image out of 100 is missing alt text. While this is a big improvement, an honest assessment would not change the conformance level for that criterion. Expecting such a granular result will not provide an accurate picture and does a disservice to the work completed by the team.

The ACR provides a high-level snapshot of your product’s accessibility support at that specific point in time and should not be seen as something set in stone. Until that moment when all work stops and the product is frozen in time, never to be used again, maintaining accessibility conformance will continue to be an evergreen process, and the ACR should be updated accordingly. What that schedule looks like should be determined by how much code is written and how often code is shipped.

Here are my recommendations:

For products that receive multiple updates every month, consider scheduling an accessibility audit and an ACR update every 3 to 6 months.

For much slower release cycles, consider every 6 to 12 months or when a major update is shipped.

So again, having an ACR is great. But also having realistic expectations for the ACR and recognizing that accessibility conformance is a product-life commitment, not just a one-off project, is equally important.
