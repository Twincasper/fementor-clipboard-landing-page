# Frontend Mentor - Clipboard landing page solution

This is a solution to the [Clipboard landing page challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/clipboard-landing-page-5cc9bccd6c4c91111378ecb9). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

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

- View the optimal layout for the site depending on their device's screen size
- See hover states for all interactive elements on the page

### Screenshot

![](https://imgur.com/1KpItuD.jpg)

### Links

- Solution URL: [Solution URL]()
- Live Site URL: [Github Page](https://twincasper.github.io/fementor-clipboard-landing-page/)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- CSS Grid
- Bootstrap 5


### What I learned

The header took me a lot longer than I would have liked to figure out, but eventually I learned a lot from it and reused that style throughout the project.

```html
<header class="bg-header">
    <section class="header-content">
      <div class="container">
        <div class="row justify-content-center text-center">
          <div class="col-md-8">
            <img src="images/logo.svg" alt="Clipboard logo" class="mb-5 mx-auto" width="125" height="125">
            <h1 class="fw-semibold mb-4">A history of everything you copy</h1>
            <p class="lead mb-5">Clipboard allows you to track and organize everything you copy. Instantly access your clipboard on all your devices.</p>
            <div class="d-flex justify-content-center gap-3">
              <button type="button" class="btn btn-primary btn-lg rounded-pill custom-btn">Download for iOS</button>
              <button type="button" class="btn btn-secondary btn-lg rounded-pill custom-btn">Download for Mac</button>
            </div>
          </div>
        </div>
      </div>
    </section>
  </header>
```

I enjoyed establishing variables in my css to use later. I think in the future I will store the percentages without them being wrapped in hsl, so I can always customize the alpha value if necessary as Kevin Powell has shown in some of his videos. This was also my first time using ::before and understanding it's potential use cases. My header was oddly layering over my buttons, so the hover effect was not kicking in at first until I utilized this.
```css
:root {
  /* Colors */
  --strong-cyan: hsl(171, 66%, 44%);
  --light-blue: hsl(233, 100%, 69%);
  --dark-grayish-blue: hsl(210, 10%, 33%);
  --grayish-blue: hsl(201, 11%, 66%);
  --footer-dark-gray: hsl(210, 10%, 33%);

  /* Typography */
  --font-family: 'Bai Jamjuree', sans-serif;
  --font-weight-regular: 400;
  --font-weight-semibold: 600;
}


.bg-header::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: linear-gradient(180deg, white 0%, rgba(255, 255, 255, 0) 100%);
  opacity: 0.25;
  z-index: -1;
}
```

### Continued development

I think my use of bootstrap, and making my html more semantic and accessibility friendly could use some work.

### Useful resources

- [Bootstrap Docs](https://getbootstrap.com/docs/5.3/getting-started/introduction/) - I found myself using this more than google, since this was a challenge to myself to stick with bootstrap as much as possible.

## Author

- Website - [Github Profile](https://github.com/Twincasper)
- Frontend Mentor - [@Twincasper](https://www.frontendmentor.io/profile/Twincasper)
