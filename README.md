# Frontend Mentor - NFT preview card component solution

This is my solution to the [NFT preview card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/nft-preview-card-component-SbdUL_w0U). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

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
- [Project structure](#project-structure)
- [Getting started](#getting-started)
- [Author](#author)
- [Acknowledgments](#acknowledgments)

## Overview

### The challenge

Users should be able to:

- View the optimal layout for the component depending on their device's screen size
- See hover states for interactive elements

### Screenshot

![Screenshot of the NFT preview card component](/preview.jpg)

### Links

- Solution URL: [Add solution URL here](https://your-solution-url.com)
- Live Site URL: [Add live site URL here](https://your-live-site-url.com)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom styling
- Flexbox
- Mobile-first workflow
- [BEM](https://getbem.com/)-inspired class naming (`block__element`)
- [Google Fonts](https://fonts.google.com/) - Outfit

### What I learned

This project helped me practice building a small, self-contained component and polishing its interactive states.

Some of the key takeaways:

- **Semantic structure:** using an `<article>` for the card and a `<footer>` for the attribution instead of generic `<div>` elements.
- **Image overlay on hover:** combining `position: relative` on the container with `position: absolute; inset: 0` on the overlay, and animating `opacity` for a smooth transition.

```css
.overlay__image {
  position: absolute;
  inset: 0;
  display: flex;
  align-items: center;
  justify-content: center;
  background: #00fff771;
  opacity: 0;
  transition: opacity 0.3s ease;
}

.overlay__image:hover {
  opacity: 1;
}
```

- **Consistent hover states:** applying the same cyan accent (`#00fff7`) with a short `transition` on the title and the creator link.
- **Layout with Flexbox:** centering the card on the page and distributing the price and time-left tags using `justify-content: space-between`.
- **Responsive tweaks:** using a `max-width` on the card with `width: 100%`, plus a small media query to add breathing room on very narrow screens.

### Continued development

Things I want to keep improving in future projects:

- Making the layout more resilient on small screens by using `min-height: 100vh` instead of a fixed `height: 100vh` on the `body`.
- Using relative image paths (`./images/...`) so the project works when opened locally or deployed to a subfolder.
- Adding meaningful `alt` text for images that convey information and reviewing the color contrast of secondary text.
- Adding `:focus-visible` styles so keyboard users get the same feedback as mouse users.
- Cleaning up small CSS details (e.g. valid `font-weight` values such as `200`, not `200px`).

### Useful resources

- [Frontend Mentor style guide for this challenge](https://www.frontendmentor.io/challenges/nft-preview-card-component-SbdUL_w0U) - Colors, fonts, and design assets.
- [MDN - Using CSS transitions](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_transitions/Using_CSS_transitions) - Helped me build smooth hover effects.
- [CSS-Tricks - A Complete Guide to Flexbox](https://css-tricks.com/snippets/css/a-guide-to-flexbox/) - A great reference for alignment and spacing.
- [BEM methodology](https://getbem.com/introduction/) - For keeping class names clear and consistent.

## Project structure

```
.
├── images/
│   ├── favicon-32x32.png
│   ├── icon-clock.svg
│   ├── icon-ethereum.svg
│   ├── icon-view.svg
│   ├── image-avatar.png
│   └── image-equilibrium.jpg
├── index.html
├── styles.css
└── README.md
```

## Getting started

1. Clone the repository:

   ```bash
   git clone https://github.com/nicolascorera/your-repo-name.git
   ```

2. Open the project folder:

   ```bash
   cd your-repo-name
   ```

3. Open `index.html` in your browser, or serve it with a local server such as the VS Code **Live Server** extension.

## Author

- GitHub - [@nicolascorera](https://github.com/nicolascorera)

## Acknowledgments

Thanks to [Frontend Mentor](https://www.frontendmentor.io) for providing the challenge and the design assets, and to the community for the feedback and inspiration.
