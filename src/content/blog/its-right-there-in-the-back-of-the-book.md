---
title: "It's Right There In the Back of the Book"
description: ""
author: "Homer Gaines, CPACC"
pubDate: Feb 17, 2025
tags: [A11y, Tips]
draft: false
heroImage: '../../assets/tips.jpg'
---

## The Cocky Kid

My parents bought the Encyclopedia Britannica collection when I was a kid. Over my summer breaks, they would have me write book reports on any of the subjects. When I was in Elementry, I remember one of my homework assignments for my Science class was to write the definitions of our keywords. Science has always been one of my favorite subjects and because of the book reports, my grades were great. So, feeling confident (cocky) in my ability, I didn’t bother to copy the answers in the back of the book but instead wrote my own definition of the words based on what I’d learned over the Summer.

## Getting Humbled

I got an “F”!

What the? I was shook! I went to my teacher and asked, “Why?” because there was no way my definitions were wrong. After all, I had written book reports about this before. Book reports my smart, college degree having parents would read, so how did I get an “F”? Oh! Also, with this teacher, any work that received an “F” had to be signed by a parent and returned the next day. Now I’m terrified.

I reluctantly showed my parents my failing grade and immediately went into defense mode, trying to get them on my side. It didn’t work. The first question my Dad asked, with a hint of frustration in his tone, was, “Where did these definitions come from? They’re not bad, but where did you get them?” When I told him I got them from my encyclopedia, he answered, “That’s the problem.” Now I’m thoroughly confused because how can the encyclopedia be wrong? Responding to my expression, he said, “So you didn’t think to look at the glossary at the back of the book? The encyclopedia is not your textbook.”

## The Lesson

He flipped to the glossary in the back of my textbook and with even more frustration in his voice, he pointed out that if I had used my textbook and copied the answers that were already provided for me, I wouldn’t have failed the assignment. His frustration was rooted in the fact that this mess was completely avoidable had I followed the text instead of relying on my own knowledge. Yes, I may “know” the information based on my own learning, but “my good answers were not the right answers, and I have to pay attention to the details.”

Now before you judge me, ask yourself if you’ve ever used a `<div>` as a button?

## Fast Forward to Now

Now that I’m wiser, I have a better appreciation for my father’s frustration with past me. While this lesson can be applied elsewhere in life, it always comes back to me when I conduct accessibility audits or code reviews. That’s because I often see a `<span>` or a `<div>` being used incorrectly as buttons or some other control. Now if you’re thinking this is easy and shouldn’t be an issue, you’d be correct; it’s very easy! I mean, for real, how hard are buttons? However, I lean on something so simple because the incorrect usage of these two elements, in particular, always turn up in whatever code I’m auditing. And as usual, I can’t help but think, “The correct element is right there! If \[you\] had used the correct semantic element in the first place, this wouldn’t be an issue.” Why? Because many semantic elements are plug-and-play and come with built-in behaviors out of the box. Sticking with buttons as an example, they provide keyboard accessibility and click handling by default, while a `<div>` or `<span>` would need these behaviors added manually.

So with this, I would like to just ask that if you ever catch yourself adding an `onclick` to a `<div>` or a `<span>` or using them for some other reason in place of a more suitable semantic element, for that matter, stop and [flip to the back of the book](https://html.spec.whatwg.org/#semantics) and choose to right bad code instead. Doing so will improve the structure of your code, reduce accessibility errors, and help with SEO.
