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
- [AI Collaboration](#ai-collaboration)
- [Author](#author)

## Overview

### The challenge

Users should be able to:
- See hover and focus states for all interactive elements on the page
- Experience a fluid layout that snaps cleanly between mobile and desktop viewport specifications.

### Screenshot

![](./screenshot.jpg)

### Links

- Solution URL: [Add your GitHub repository link here]
- Live Site URL: [Add your GitHub Pages or Vercel live link here]

## My process

### Built with

- Semantic HTML5 structural markup
- CSS Custom Properties (Variables for design system tokens)
- CSS Flexbox (Viewport calibration & axis controls)
- Mobile-first responsive workflow
- Google Fonts API integration (`Inter`)

### What I learned

This challenge provided a great opportunity to practice debugging layout containment and managing default Flexbox axis assumptions.

1. **Flex Axis Synchronization:** I caught a layout bug where the attribution footer was forcing itself to sit as a horizontal sibling to the right of the card. Resolving this required enforcing a explicit `column` direction on the layout root and adding a minimum viewport height constraint:

```css
body {
  display: flex;
  flex-direction: column; /* Forces vertical stacking of the card and footer */
  justify-content: center;
  align-items: center;
  min-height: 100vh;
}