---
title: Day Two - 100DaysOfCode
date: '2019-01-29T00:00:03.284Z'
---

Okay, finally got some time to write this post. Work is busy this day, and the pain in my back still.

### Sick-Fits Store

So the first thing worth mentioning is I finished one lesson of Wes Bos's [course about GraphQL](https://advancedreact.com/). I learnt some basic CRUD operations. Prisma is cool, it automatically helps you generate a bunch of basic mutation and query functions. The backend architecture of that course is using Yoga and Prisma. Which is kinda complicated, but thinking I will get more and more familiar with that in next couple of days.

### Styled-components

Today I got a chance to try the awesome CSS-in-JS library - [Styled-components](https://www.styled-components.com/). It was a quite enjoyable process for me. To be honest, I'm not good at CSS. So it's quite hard for me to figure out a good CSS architecture in a project. But the concept of CSS-in-JS is quite straightforward to me because all your styles are tightly combined with your component code. I don't need to worry about processing the layout and component code separately.  
A very good scenario is that one day my coworker wants to utilize a component wrote by me to his project. It's a table component. The traditional method would be importing the js file first, and then find and include the css files. However, now he just need to import the js file of that component. Quite straightforward and efficient, isn't?

### Background transparency

What's your method to make a background color transparent?

```css
background: rgba(0, 255, 255, 0.3);
```

Excellent, but do we have some other approaches?

I found an interesting way to make your background color transparent. We all know that you can write your color property in HEX code(like #00FFFF). Now you can add another two digits into your HEX code. It will work in the same way.

```css
background: #00ffff4d;
```

[8-Digit Hex Codes?](https://css-tricks.com/8-digit-hex-codes/)

### Some Good Resources

1. [codrops](https://tympanus.net/codrops/)
2. [Easing functions](https://easings.net/en#)
