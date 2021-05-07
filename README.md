# Frontend Mentor - Stats preview card component solution

This is a solution to the [Stats preview card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/stats-preview-card-component-8JqbgoU62). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [Useful resources](#useful-resources)
- [Author](#author)

## Overview

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size

### Screenshot

![](../challenge-screenshots/card-mobile.png)
![](../challenge-screenshots/card-desktop.png)

### Links

- Solution URL: [Add solution URL here](https://your-solution-url.com)
- Live Site URL: [Add live site URL here](https://your-live-site-url.com)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- CSS Grid
- Mobile-first workflow

### What I learned

When I started the project I thought it would be easy to get throught, but man, I was wrong. I spent much more time than I like to admit trying to make the image and the text inside the .card have the correct proportion, all because I forgot to specify a height for the .card, and because I used percentages for the child elements, they didn't have any value for reference, so it kinda screwed up the layout.

At first I was using flex in the .card, but I realized it would be easier (and good for practice) to use grid, as I would be able to "swap" the child elements using grid areas. I remembered (and learnt) a couple of things using grid, I had tottaly forgot how nice is to use grid.

And lastly, I got some ideas on the design part:

- How the elements are spaced: (for example: the heading and the paragraph have a margin in-beetwen them of 0.75em; the paragraph and the stats have a margin in-beetwen them of 1.25em. It makes the design looks cleaner and more understandable, as you can differentiate more easily each element)
- How the "blank" space plays a big role (at least for me) on the design. When elements have space for breathing, things look less claustrophobic and nicer, so it's a good ideia to use padding (and sometimes margin) to give items some room to breath.

### How I built it

First I took the measurements of each design preview and I got this:

|                   | Mobile | Desktop |
| ----------------- | ------ | ------- |
| Gutter            | 24 px  | --      |
| Card width (max)  | 327 px | 1100 px |
| Card height (max) | 780 px | 446 px  |

After that, I converted from `px` to `rem`:

|                   | Mobile     | Desktop    |
| ----------------- | ---------- | ---------- |
| Gutter            | 1.5 rem    | --         |
| Card width (max)  | 20.438 rem | 68.75 rem  |
| Card height (max) | 43.75 rem  | 27.875 rem |

The reason why I converted from `px` to `rem` is responsiviness. `px` is an absolute unit, meaning that if the user increase the font size of the browser, all the texts would get bigger, but not the containers, so using `rem` should help with that. (I'm still testing and learning about this btw)

---

For the `.card` class, I used grid to create two areas: `image` and `content`. The content area was for all the text, while the image was for (guess what....) the image. Why grid and not flex? Well, because in the desktop design, I would need to swap positions, so I found it easier to use grid to make that magic happen (I just remembered that I could have used row-reverse from flex.... dang)

---

The rest of the code is pretty straighforward, the only thing that I think is worth mentioning is that the `.cards` grid can hold up to three cards in a row, "wrapping" the next cards, meaning that the project is responsible.

### Continued development

There a few things that I want to be more comfortable/have more knowledge with:

- Flexbox / Grid: I need to have a deeper understanding of how flexbox and grid work to implement in more complex projects. I'm comfortable with the both of them, but I don't think that this is enought if I want to have cleaner codes with reusability.
- Quality of code: I've been using BEM for a while, and it has helped me a lot with reusable classes and "hierarchy", but I have that feeling that I can still improve a lot my code, make it cleaner, more concise, and simpler, without losing or having negative impacts on its final result.
- Design: Knowing how to develop and implement other people's design is good, but far from enought. I've noticed that a lot of times I play around with values (font-size, padding, letter-spacing, etc) to see how they will display, so it kinda gave me a basic "perception" if something is looking good or no, if a paragraph would look better with a different font-size, color and more margim, these kind of things. I'm finding very helpful, because it gives wings to my imagination (knowing how to use the tools and how to create things that I like with them) and it also helps if I want to make suggestions on a design (I think that it will be handy when I start to freelance or something).

### Useful resources

- [Complete Grid Guide from css-tricks](https://css-tricks.com/snippets/css/complete-guide-grid/) - This complete tutorial helped to remember and understand better (wait for it!) grid.
-

## Author

- Github - [joaoHass](https://www.your-site.com)
- Frontend Mentor - [@joaoHass](https://www.frontendmentor.io/profile/joaoHass)
