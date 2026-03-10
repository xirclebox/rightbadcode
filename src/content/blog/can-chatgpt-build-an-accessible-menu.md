---
title: "Can ChatGPT build an Accessible Menu?"
description: ""
author: "Homer Gaines, CPACC"
pubDate: 2026-02-22
tags: [A11y, UX]
draft: true
heroImage: '../../assets/blog-placeholder-3.jpg'
---

I posted a [short accessibility navigation tip](https://rightbadcode.com/accessible-navigation) recently and out of curiosity, I asked ChatGPT to build an accessible menu. If you're not familiar with ChatGPT, in a nutshell, it's [a chatbot that was built by OpenAI](https://openai.com/blog/chatgpt/) that can hold a conversation with you as well as write code. Seeing as how people are using this and other AI tools to aid with simple coding tasks, I wanted to give it a simple coding task and evaluate the markup to see how it might impact accessibility on the web.

> **Me:**  
> Can you build an accessible navigation, please?
>
> **ChatGPT:**  
> Sure! Here are some general tips for building an accessible navigation system:
>
> 1. Use clear, descriptive labels for navigation links. This will help users understand the content they will find when they click on a link.
> 2. Use headings and subheadings to organize the content on your page. This will make it easier for users to scan and navigate to the information they need.
> 3. Use lists to group related links together. This will make it easier for users to find what they are looking for and will also make the page more organized and easier to understand.
> 4. Use skip links to allow users to skip over navigation and go directly to the main content of the page. This is particularly helpful for users who use assistive technologies such as screen readers.
> 5. Make sure the navigation is keyboard accessible. Users should be able to use the tab key to move between links and the enter key to activate them.
> 6. Consider using a mega menu or fly-out menu to organize your navigation links into categories or sub-categories. This can help users find what they are looking for more easily.
> 7. Use ARIA landmarks to help assistive technologies understand the purpose of different sections of the page. For example, you can use the "navigation" landmark to indicate that a section of the page is a navigation menu.
>
> I hope these tips are helpful! Let me know if you have any other questions.

Not quite what I was expecting but, ok. Thanks. I was expecting an HTML output to see if the AI wrote semantic code. Maybe I didn't ask the question correctly so I revised my original question. Round 2! Fight!

> **Me:**  
> Can you code an accessible menu, please?
>
> **ChatGPT:**  
> Certainly! Here is an example of how you could code an accessible navigation menu using HTML and CSS:

```xml
<nav role="navigation">
  <ul>
    <li><a href="/home">Home</a></li>
    <li><a href="/about">About</a></li>
    <li><a href="/products">Products</a></li>
    <li><a href="/contact">Contact</a></li>
  </ul>
</nav>
```

The results of the first group of markup isn't bad. I was happy to see that it used the `nav` element and an unordered list instead of a bunch of `div` elements. The `role="navigation"` is not needed since the correct element is being used which makes this role redundant. It's not going to hurt anything but devs should always be mindful of over-engineering. Speaking of over-engineering, the second block of HTML took a slight dive.

```xml
To make the menu keyboard accessible,
you can add the tabindex attribute to
the a elements and set the value to 0:

<nav role="navigation">
  <ul>
    <li><a href="/home" tabindex="0">Home</a></li>
    <li><a href="/about" tabindex="0">About</a></li>
    <li><a href="/products" tabindex="0">Products</a></li>
    <li><a href="/contact" tabindex="0">Contact</a></li>
  </ul>
</nav>
```

The glaring problem that I spotted here is the use of `tabindex="0"` on the links. Adding `tabindex="0"` to any element places that element in the accessible DOM tree structure making it focusable via keyboard. However, the `a` tag receives focus natively so the `tabindex` is redundant.

```css
nav ul {
  list-style: none;
  margin: 0;
  padding: 0;
}

nav li {
  display: inline-block;
}

nav a {
  display: block;
  padding: 8px;
  text-decoration: none;
  color: #333;
}

nav a:hover {
  background-color: #eee;
}
```

The CSS is straightforward. Glad to see there isn't an `outline="none"` on the links which would hide the focus ring from people who navigate content using other modes of input other than a mouse. There is a missing `:focus` state which can be used to mimic the `:hover` state. Because not all default focus rings are created equal, I would trigger the visual hover state on interaction for keyboards as well. The colors aren't bad but can be improved. The text color is a dark grey which is a good choice when on a white background because the stark contrast between [black and white can cause eye strain](https://www.nature.com/articles/s41598-018-28904-x) and fatigue. The hover state, compared to the text color has a [contrast ratio of 10.88:1](https://webaim.org/resources/contrastchecker/?fcolor=333333&bcolor=EEEEEE) which surpasses the [requirement of 3.1](https://www.w3.org/WAI/WCAG21/Understanding/non-text-contrast.html). My only concern with that tone of grey is that it could wash out on bright monitors.

Here are the results of the AI-generated code.

%[https://codepen.io/xirclebox/pen/YzjXBZE]

Here's my version of the generated code with a few tweaks.

%[https://codepen.io/xirclebox/pen/VwBLgWr]

In the spirit of fun and because I woke up this morning and chose violence, I asked for the same accessible navigation but with Tailwind CSS instead. Brace yourself.

> **Me:**  
> Can you code an accessible menu using tailwind, please?
>
> **ChatGPT:**  
> Certainly! Here is an example of how you could code an accessible navigation menu using HTML and Tailwind CSS:

```xml
<nav class="flex items-center justify-between px-4 py-3 bg-gray-800">
  <div class="flex items-center flex-shrink-0 text-white mr-6">
    <svg class="fill-current h-8 w-8 mr-2" width="54" height="54" viewBox="0 0 54 54" xmlns="http://www.w3.org/2000/svg"><path d="M13.5 22.1c1.8-7.2 6.3-10.8 13.5-10.8 10.8 0 12.15 8.1 17.55 9.45 3.6.9 6.75-.45 9.45-4.05-1.8 7.2-6.3 10.8-13.5 10.8-10.8 0-12.15-8.1-17.55-9.45-3.6-.9-6.75.45-9.45 4.05zM0 38.3c1.8-7.2 6.3-10.8 13.5-10.8 10.8 0 12.15 8.1 17.55 9.45 3.6.9 6.75-.45 9.45-4.05-1.8 7.2-6.3 10.8-13.5 10.8-10.8 0-12.15-8.1-17.55-9.45-3.6-.9-6.75.45-9.45 4.05z"/></svg>
    <span class="font-semibold text-xl tracking-tight">My Site</span>
  </div>
  <div class="block lg:hidden">
    <button class="flex items-center px-3 py-2 border rounded text-teal-200 border-teal-400 hover:text-white hover:border-white">
      <svg class="fill-current h-3 w-3" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><title>Menu</title><path d="M0 3h20v2H0V3zm0 6h20v2H0V9zm0 6h20v2H0v-2z"/></svg>
    </button>
  </div>
  <div class="w-full block flex-grow lg:flex lg:items-center lg:w-auto">
    <div class="text-sm lg:flex-grow">
      <a href="#responsive-header" class="block mt-4 lg:inline-block lg:mt-0 text-teal-200 hover:text-white mr-4">
        Home
      </a>
      <a href="#responsive-header" class="block mt-4 lg:inline-block lg:mt-0 text-teal-200 hover:text-white mr-4">
        About
      </a>
      <a href="#responsive-header" class="block mt-4 lg:inline-block lg:mt-0 text-teal-200 hover:text-white">
        Products
```

What in the world is that? There's so much to unpack here. So much regret. How is this everything I expected while simultaneously not what I expected? I mean, I knew it was going to be verbose but good grief! Did you notice the code didn't even complete? Even the AI knew this wasn't wise. Realistically, it probably hit a character limit or ran out of memory but I'd still like to think it just gave up out of shame.

Anyway...  
Now before the tech bros come for me, yes, this is AI-written code and AI is only as good as the data used to train it. Yep, I get it. However, as someone who conducts accessibility audits, I have seen production code in the wild that looks like this! Maybe I'll talk about Tailwind's impact on the developer experience and neurodivergence in a future post but for now, I'll leave this right here.

Did ChatGPT provide some decent coding examples of accessible navigation? I'd say so. Aside from the Tailwind example, the markup was clean. Even the list of tips from my first query wasn't bad. I can see people using this for learning or generating boilerplate markup, but I would strongly caution anyone [thinking about using AI-generated code in production](https://www.theregister.com/2022/12/21/ai_assistants_bad_code/) without grooming it first. For some, It may be a great starting point but it does not and should not replace the time it takes to right bad code.

Updated: 05/16/2023

I wanted to see how Bard would handle building an accessible menu. To keep is brief, I also asked it to use Tailwind so I could laugh.

```xml
<nav class="container nav text-2xl font-bold">
  <ul class="list-none">
    <li><a href="#" aria-label="Home">Home</a></li>
    <li><a href="#" aria-label="About">About</a></li>
    <li><a href="#" aria-label="Contact">Contact</a></li>
  </ul>
</nav>
```

No more jabs at Tailwind for now but let's talk about the markup. It's not bad but it's over-engineered. There's no need for the `aria-label` since the links have accessible names already. Aria-labels also override the accessible name which can be confusing for some users. In addition to this, `aria-label's` don't really play well with internationalization since they are not exposed to translation.
