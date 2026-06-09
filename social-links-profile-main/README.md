# Frontend Mentor - Social links profile solution

This is my official production solution to the [Social links profile challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/social-links-profile-UG32l9m6dQ).

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
- [Author](#author)

## Overview

### The challenge

Users should be able to:
- See hover and focus states for all interactive elements on the page
- Experience a fluid layout that snaps cleanly between mobile and desktop viewport specifications.

### Screenshot

![](./screenshot.jpg)

### Links

- Solution URL: [https://github.com/cl-js/social-links-profile-main](https://github.com/cl-js/social-links-profile-main)
- Live Site URL: [https://cl-js.github.io/social-links-profile-main/](https://cl-js.github.io/social-links-profile-main/)

## My process

### Built with

- Semantic HTML5 structural markup
- CSS Custom Properties (Variables for design system tokens)
- CSS Flexbox (Viewport centering & layout axis management)
- Mobile-first responsive workflow
- Google Fonts API integration (`Inter`)

### What I learned

This challenge provided an excellent opportunity to master vertical/horizontal container alignment and manage default Flexbox behavior.

1. **Flex Axis Standardization:** I diagnosed and fixed a bug where the attribution footer stood as a horizontal sibling to the right of the card. Resolving this required overriding the default row axis, enforcing a column structure on the body, and setting a minimum screen height constraint:

```css
body {
  display: flex;
  flex-direction: column; /* Forces vertical stacking of the card and footer */
  justify-content: center;
  align-items: center;
  min-height: 100vh;
}
```
2. Design Tokens Integration: Instead of loosely duplicating HSL values, I mapped out the entire style guide directly into native CSS variable tokens at the root level for cleaner, maintainable styling:
```css
:root {
  --clr-green: hsl(75, 94%, 57%);
  --clr-grey-800: hsl(0, 0%, 12%);
  --ff-sans: 'Inter', sans-serif;
}
```
## Continued development
In future layouts, I want to keep prioritizing web accessibility (WCAG compliance) by nesting my site mapping items cleanly within native navigation wrappers (<nav>, <ul>, <a>) to guarantee better assistant screen-reading flows.

## Author
- Frontend Mentor - [@cl-js](https://www.frontendmentor.io/profile/cl-js)