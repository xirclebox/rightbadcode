---
title: "Mapping the Revised 508/255 ICT Accessibility Standards to the WCAG 2.2"
description: ""
author: "Homer Gaines, CPACC"
pubDate: Aug 8, 2026
tags: [A11y, WCAG, "508", Governance]
draft: false
heroImage: '../../assets/post2.jpg'
---

I have this thing about [connecting the dots](https://rightbadcode.com/aligning-jakob-nielsens-10-usability-heuristics-with-the-wcag-22/) between the current Web Content Accessibility Guidelines (WCAG) and other documents that relate to accessibility. That way, the relationships are easier to see, reference, and teach. Seeing as how there's a lot of buz around making government sites accessible and agencies scrambling to [make the new deadline](https://www.hhs.gov/press-room/hhs-extends-mobile-and-web-accessibility-deadline.html), I wanted to highlight the similarities between the WCAG and the Revised 508/255 ICT Standards.

## Table of contents

- [How the ICT rule references WCAG](#how-the-ict-rule-references-wcag)
- [ICT rules that align with the WCAG success criteria](#ict-rules-that-align-with-the-wcag-success-criteria)
- [WCAG 2.0 A & AA criteria required by the ICT rule, mapped to WCAG 2.2](#wcag-20-a--aa-criteria-required-by-the-ict-rule-mapped-to-wcag-22)
- [WCAG 2.2 criteria not required by the ICT](#wcag-22-criteria-not-required-by-the-ict)
- [ICT rules with no WCAG equivalent](#ict-rules-with-no-wcag-equivalent)
- [Legacy cross-reference: original 2000 Section 508 Standards (§1194.22) to WCAG 1.0](#legacy-cross-reference-original-2000-section-508-standards-119422-to-wcag-10)

## How the ICT rule references WCAG

Being behind the ball a bit, the Information and communication technology (ICT) rule doesn't point to the current version of the WCAG. It incorporates the [WCAG 2.0](https://www.w3.org/TR/WCAG20/) by reference [702.10.1](https://www.access-board.gov/ict/#702-10-1) and requires Level A and Level AA conformance. Because the WCAG 2.2 is backward compatible, every 2.0 success criterion (SC) carries the same number, except for "SC 4.1.1 Parsing" which was deprecated. The WCAG 2.0 Levels along with the ICT rules map one-to-one onto a subset of today's WCAG 2.2 Levels. The ICT rule's text does not require the newer criteria added to the WCAG 2.2 however, it would be in the best interest for agencies to apply 2.2. That way, when the old requirements catch up to modern times, those who have been aiming for 2.2 will be ahead of the game.

## ICT rules that align with the WCAG success criteria

| ICT rule| What it covers | WCAG Level | Exceptions |
|---|---|---|---|
| [E205.4 (508, Electronic Content)](https://www.access-board.gov/ict/#E205-content) | Public-facing and certain non-public agency electronic content | A and AA | Non-Web documents excused from [2.4.1](https://www.w3.org/WAI/WCAG22/Understanding/bypass-blocks), [2.4.5](https://www.w3.org/WAI/WCAG22/Understanding/multiple-ways), [3.2.3](https://www.w3.org/WAI/WCAG22/Understanding/consistent-navigation), [3.2.4](https://www.w3.org/WAI/WCAG22/Understanding/consistent-identification) |
| [E207.2 (508, Software)](https://www.access-board.gov/ict/#E207-software) | UI components and content of platforms/applications | A and AA | Non-Web software excused from the same four criteria, and from Conformance Requirement 3 (Complete Processes) |
| [C203.1 (255, Electronic Content)](https://www.access-board.gov/ict/#C203-electronic-content) | Content integral to telecom or Customer Premises Equipment use | A and AA | Non-Web documents excused from [2.4.1](https://www.w3.org/WAI/WCAG22/Understanding/bypass-blocks), [2.4.5](https://www.w3.org/WAI/WCAG22/Understanding/multiple-ways), [3.2.3](https://www.w3.org/WAI/WCAG22/Understanding/consistent-navigation), [3.2.4](https://www.w3.org/WAI/WCAG22/Understanding/consistent-identification) |
| [C205.2 (255, Software)](https://www.access-board.gov/ict/#C205-software) | UI components and content of telecom platforms/applications | A and AA | Same exceptions as E207.2 |
| [504.2 / 504.3 / 504.4 (Authoring Tools)](https://www.access-board.gov/ict/#504-authoring-tools) | Content produced or edited by authoring tools, prompts, templates | A and AA | Applies "to the extent supported by the destination format"; not required for direct editing of plain text source code |
| [602.3 (Electronic Support Documentation)](https://www.access-board.gov/ict/#602-support-documentation) | Web-based/electronic help and self-service documentation | A and AA | None stated |
| [501.1 Exception (Software, general)](https://www.access-board.gov/ict/#501-general) | Web applications lacking platform accessibility service access | A and AA (in lieu of 502/503) | Applies only when the app has no access to platform accessibility services |
| [408.3 Exception (Hardware, Flashing)](https://www.access-board.gov/ict/#408-display-screens) | Flashing on ICT display screens | General flash / red flash thresholds | Defined by reference to WCAG 2.0's flash thresholds (see [2.3.1](https://www.w3.org/WAI/WCAG22/Understanding/three-flashes-or-below-threshold)) |

Where a document or non-Web software substitution applies, the rule also swaps the term "Web page" or "page" for "document" or "software" in the SC text [E205.4.1](https://www.access-board.gov/ict/#E205-content), [E207.2.1](https://www.access-board.gov/ict/#E207-software), [C203.1.1](https://www.access-board.gov/ict/#C203-electronic-content), [C205.2.1](https://www.access-board.gov/ict/#C205-software).

## WCAG 2.0 A & AA criteria required by the ICT rule, mapped to WCAG 2.2

The following 38 success criteria are the ones the ICT rule requires. Numbering and titles are unchanged, so each maps directly to the current WCAG 2.2 SC.

### Level A

| SC | WCAG 2.2 Title | Status |
|---|---|---|
| 1.1.1 | [Non-text Content](https://www.w3.org/WAI/WCAG22/Understanding/non-text-content) | Unchanged |
| 1.2.1 | [Audio-only and Video-only (Prerecorded)](https://www.w3.org/WAI/WCAG22/Understanding/audio-only-and-video-only-prerecorded) | Unchanged |
| 1.2.2 | [Captions (Prerecorded)](https://www.w3.org/WAI/WCAG22/Understanding/captions-prerecorded) | Unchanged |
| 1.2.3 | [Audio Description or Media Alternative (Prerecorded)](https://www.w3.org/WAI/WCAG22/Understanding/audio-description-or-media-alternative-prerecorded) | Unchanged |
| 1.3.1 | [Info and Relationships](https://www.w3.org/WAI/WCAG22/Understanding/info-and-relationships) | Unchanged |
| 1.3.2 | [Meaningful Sequence](https://www.w3.org/WAI/WCAG22/Understanding/meaningful-sequence) | Unchanged |
| 1.3.3 | [Sensory Characteristics](https://www.w3.org/WAI/WCAG22/Understanding/sensory-characteristics) | Unchanged |
| 1.4.1 | [Use of Color](https://www.w3.org/WAI/WCAG22/Understanding/use-of-color) | Unchanged |
| 1.4.2 | [Audio Control](https://www.w3.org/WAI/WCAG22/Understanding/audio-control) | Unchanged |
| 2.1.1 | [Keyboard](https://www.w3.org/WAI/WCAG22/Understanding/keyboard) | Unchanged |
| 2.1.2 | [No Keyboard Trap](https://www.w3.org/WAI/WCAG22/Understanding/no-keyboard-trap) | Unchanged |
| 2.2.1 | [Timing Adjustable](https://www.w3.org/WAI/WCAG22/Understanding/timing-adjustable) | Unchanged |
| 2.2.2 | [Pause, Stop, Hide](https://www.w3.org/WAI/WCAG22/Understanding/pause-stop-hide) | Unchanged |
| 2.3.1 | [Three Flashes or Below Threshold](https://www.w3.org/WAI/WCAG22/Understanding/three-flashes-or-below-threshold) | Unchanged |
| 2.4.1 | [Bypass Blocks](https://www.w3.org/WAI/WCAG22/Understanding/bypass-blocks) | Unchanged (excepted for non-Web docs/software) |
| 2.4.2 | [Page Titled](https://www.w3.org/WAI/WCAG22/Understanding/page-titled) | Unchanged |
| 2.4.3 | [Focus Order](https://www.w3.org/WAI/WCAG22/Understanding/focus-order) | Unchanged |
| 2.4.4 | [Link Purpose (In Context)](https://www.w3.org/WAI/WCAG22/Understanding/link-purpose-in-context) | Unchanged |
| 3.1.1 | [Language of Page](https://www.w3.org/WAI/WCAG22/Understanding/language-of-page) | Unchanged |
| 3.2.1 | [On Focus](https://www.w3.org/WAI/WCAG22/Understanding/on-focus) | Unchanged |
| 3.2.2 | [On Input](https://www.w3.org/WAI/WCAG22/Understanding/on-input) | Unchanged |
| 3.3.1 | [Error Identification](https://www.w3.org/WAI/WCAG22/Understanding/error-identification) | Unchanged |
| 3.3.2 | [Labels or Instructions](https://www.w3.org/WAI/WCAG22/Understanding/labels-or-instructions) | Unchanged |
| 4.1.1 | [Parsing](https://www.w3.org/WAI/WCAG22/Understanding/parsing) | **Obsolete/removed in WCAG 2.2** — no longer testable; treat as satisfied |
| 4.1.2 | [Name, Role, Value](https://www.w3.org/WAI/WCAG22/Understanding/name-role-value) | Unchanged |

### Level AA

| SC | WCAG 2.2 Title | Status |
|---|---|---|
| 1.2.4 | [Captions (Live)](https://www.w3.org/WAI/WCAG22/Understanding/captions-live) | Unchanged |
| 1.2.5 | [Audio Description (Prerecorded)](https://www.w3.org/WAI/WCAG22/Understanding/audio-description-prerecorded) | Unchanged |
| 1.4.3 | [Contrast (Minimum)](https://www.w3.org/WAI/WCAG22/Understanding/contrast-minimum) | Unchanged |
| 1.4.4 | [Resize Text](https://www.w3.org/WAI/WCAG22/Understanding/resize-text) | Unchanged |
| 1.4.5 | [Images of Text](https://www.w3.org/WAI/WCAG22/Understanding/images-of-text) | Unchanged |
| 2.4.5 | [Multiple Ways](https://www.w3.org/WAI/WCAG22/Understanding/multiple-ways) | Unchanged (excepted for non-Web docs/software) |
| 2.4.6 | [Headings and Labels](https://www.w3.org/WAI/WCAG22/Understanding/headings-and-labels) | Unchanged |
| 2.4.7 | [Focus Visible](https://www.w3.org/WAI/WCAG22/Understanding/focus-visible) | Unchanged |
| 3.1.2 | [Language of Parts](https://www.w3.org/WAI/WCAG22/Understanding/language-of-parts) | Unchanged |
| 3.2.3 | [Consistent Navigation](https://www.w3.org/WAI/WCAG22/Understanding/consistent-navigation) | Unchanged (excepted for non-Web docs/software) |
| 3.2.4 | [Consistent Identification](https://www.w3.org/WAI/WCAG22/Understanding/consistent-identification) | Unchanged (excepted for non-Web docs/software) |
| 3.3.3 | [Error Suggestion](https://www.w3.org/WAI/WCAG22/Understanding/error-suggestion) | Unchanged |
| 3.3.4 | [Error Prevention (Legal, Financial, Data)](https://www.w3.org/WAI/WCAG22/Understanding/error-prevention-legal-financial-data) | Unchanged |

## WCAG 2.2 criteria not required by the ICT

As I mentioned above, since the ICT rule references the WCAG 2.0, the newer criteria (introduced in 2.1 or 2.2) are not required by 508/255. Though, that doesn't mean they sould be ignored.

| SC | WCAG Title | Level | WCAG version |
|---|---|---|---|
| 1.3.4 | [Orientation](https://www.w3.org/WAI/WCAG22/Understanding/orientation) | AA | 2.1 |
| 1.3.5 | [Identify Input Purpose](https://www.w3.org/WAI/WCAG22/Understanding/identify-input-purpose) | AA | 2.1 |
| 1.3.6 | [Identify Purpose](https://www.w3.org/WAI/WCAG22/Understanding/identify-purpose) | AAA | 2.1 |
| 1.4.10 | [Reflow](https://www.w3.org/WAI/WCAG22/Understanding/reflow) | AA | 2.1 |
| 1.4.11 | [Non-text Contrast](https://www.w3.org/WAI/WCAG22/Understanding/non-text-contrast) | AA | 2.1 |
| 1.4.12 | [Text Spacing](https://www.w3.org/WAI/WCAG22/Understanding/text-spacing) | AA | 2.1 |
| 1.4.13 | [Content on Hover or Focus](https://www.w3.org/WAI/WCAG22/Understanding/content-on-hover-or-focus) | AA | 2.1 |
| 2.1.4 | [Character Key Shortcuts](https://www.w3.org/WAI/WCAG22/Understanding/character-key-shortcuts) | A | 2.1 |
| 2.2.6 | [Timeouts](https://www.w3.org/WAI/WCAG22/Understanding/timeouts) | AAA | 2.1 |
| 2.3.2 | [Three Flashes](https://www.w3.org/WAI/WCAG22/Understanding/three-flashes) | AAA | 2.1 |
| 2.3.3 | [Animation from Interactions](https://www.w3.org/WAI/WCAG22/Understanding/animation-from-interactions) | AAA | 2.1 | [Link]
| 2.4.11 | [Focus Not Obscured (Minimum)](https://www.w3.org/WAI/WCAG22/Understanding/focus-not-obscured-minimum) | AA | 2.2 |
| 2.4.12 | [Focus Not Obscured (Enhanced)](https://www.w3.org/WAI/WCAG22/Understanding/focus-not-obscured-enhanced) | AAA | 2.2 |
| 2.4.13 | [Focus Appearance](https://www.w3.org/WAI/WCAG22/Understanding/focus-appearance) | AAA | 2.2 |
| 2.5.1 | [Pointer Gestures](https://www.w3.org/WAI/WCAG22/Understanding/pointer-gestures) | A | 2.1 |
| 2.5.2 | [Pointer Cancellation](https://www.w3.org/WAI/WCAG22/Understanding/pointer-cancellation) | A | 2.1 |
| 2.5.3 | [Label in Name](https://www.w3.org/WAI/WCAG22/Understanding/label-in-name) | A | 2.1 |
| 2.5.4 | [Motion Actuation](https://www.w3.org/WAI/WCAG22/Understanding/motion-actuation) | A | 2.1 |
| 2.5.5 | [Target Size (Enhanced)](https://www.w3.org/WAI/WCAG22/Understanding/target-size-enhanced) | AAA | 2.1 |
| 2.5.6 | [Concurrent Input Mechanisms](https://www.w3.org/WAI/WCAG22/Understanding/concurrent-input-mechanisms) | AAA | 2.1 |
| 2.5.7 | [Dragging Movements](https://www.w3.org/WAI/WCAG22/Understanding/dragging-movements) | AA | 2.2 |
| 2.5.8 | [Target Size (Minimum)](https://www.w3.org/WAI/WCAG22/Understanding/target-size-minimum) | AA | 2.2 |
| 3.2.5 | [Change on Request](https://www.w3.org/WAI/WCAG22/Understanding/change-on-request) | AAA | 2.1 |
| 3.2.6 | [Consistent Help](https://www.w3.org/WAI/WCAG22/Understanding/consistent-help) | A | 2.2 |
| 3.3.5 | [Help](https://www.w3.org/WAI/WCAG22/Understanding/help) | AAA | 2.1 |
| 3.3.6 | [Error Prevention (All)](https://www.w3.org/WAI/WCAG22/Understanding/error-prevention-all) | AAA | 2.1 |
| 3.3.7 | [Redundant Entry](https://www.w3.org/WAI/WCAG22/Understanding/redundant-entry) | A | 2.2 |
| 3.3.8 | [Accessible Authentication (Minimum)](https://www.w3.org/WAI/WCAG22/Understanding/accessible-authentication-minimum) | AA | 2.2 |
| 3.3.9 | [Accessible Authentication (Enhanced)](https://www.w3.org/WAI/WCAG22/Understanding/accessible-authentication-enhanced) | AAA | 2.2 |
| 4.1.3 | [Status Messages](https://www.w3.org/WAI/WCAG22/Understanding/status-messages) | AA | 2.1 |

## ICT rules with no WCAG equivalent

Because the WCAG governs electronic content, a large part of the ICT rules are out of the WCAG's scope since they govern support services, hardware, platform-level software services.

- [Chapter 3, Functional Performance Criteria (301–302)](https://www.access-board.gov/ict/#301-general)
vision/hearing/speech/manipulation-based outcome criteria used as a fallback where Chapters 4–5 don't address a function.
- [Chapter 4, Hardware (401–415)](https://www.access-board.gov/ict/#401-general)
 physical device requirements, closed-functionality speech output, volume, reach ranges, key layouts, TTY connectivity, caption/audio-description decoder circuitry, etc.
- [502 Interoperability with Assistive Technology](https://www.access-board.gov/ict/#502-interoperability-assistive-technology) / [503.2–503.3](https://www.access-board.gov/ict/#503-applications)
platform accessibility-services requirements (object role/state exposure, focus tracking, etc.) related to [4.1.2 Name, Role, Value](https://www.w3.org/WAI/WCAG22/Understanding/name-role-value), but scoped to platform software rather than Web content.
- [Chapter 6, Support Documentation and Services (601–603)](https://www.access-board.gov/ict/#601-general)
non-electronic alternate formats and help-desk and communication-accommodation requirements.

## Legacy cross-reference: original 2000 Section 508 Standards (§1194.22) to WCAG 1.0

Going back this far is over kill, but hey, here we are. So for context, the Access Board's preamble maps the original 2000-era [§1194.22 paragraphs (a)-(k)](https://www.access-board.gov/ict/#notes) to [WCAG 1.0 Priority 1 guidelines or checkpoint](https://www.w3.org/TR/WCAG10/#priorities). This mapping is is only relevant when evaluating legacy ICT under the [safe-harbor provision (E202.2)](https://www.access-board.gov/ict/#6-extended-compliance-date-and-incorporation-of-safe-harbor-prov).

| §1194.22 Paragraph | WCAG 1.0 Checkpoint |
|---|---|
| (a) | 1.1 |
| (b) | 1.4 |
| (c) | 2.1 |
| (d) | 6.1 |
| (e) | 1.2 |
| (f) | 9.1 |
| (g) | 5.1 |
| (h) | 5.2 |
| (i) | 12.1 |
| (j) | 7.1 |
| (k) | 11.4 |

Not shown here, [paragraphs (l)–(p)](https://www.access-board.gov/ict/#d22), of the original §1194.22 have no WCAG 1.0 equivalent and were 508-specific additions. Full checkpoint text is available in the [WCAG 1.0 specification](https://www.w3.org/TR/WCAG10/).

---

### References

U.S Access Board, Revised 508 Standards and 255 Guidelines  
[https://www.access-board.gov/ict/](https://www.access-board.gov/ict/)

Understanding WCAG 2.2  
[https://www.w3.org/WAI/WCAG21/quickref/](https://www.w3.org/WAI/WCAG22/quickref/?versions=2.2)
