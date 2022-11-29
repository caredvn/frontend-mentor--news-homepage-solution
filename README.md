# Frontend Mentor - News homepage solution

This is a solution to the [News homepage challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/news-homepage-H6SWTa1MFl). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

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
- [Acknowledgments](#acknowledgments)

## Overview

### The challenge

Users should be able to:

- View the optimal layout for the interface depending on their device's screen size
- See hover and focus states for all interactive elements on the page
- **Bonus**: Toggle the mobile menu (CSS only)

### Screenshot

![screenshot1--desktop-version](https://user-images.githubusercontent.com/107898347/204391182-f559c1a9-904c-475b-a51e-3fb84084a9ea.png)
![screenshot2--desktop-version](https://user-images.githubusercontent.com/107898347/204391190-401d3beb-4be0-410a-8df0-efdd963472f5.png)
![screenshot3--mobile-version](https://user-images.githubusercontent.com/107898347/204391184-c418766f-3d10-4f04-92ee-17fdddca8f67.png)
![screenshot2--mobile-version](https://user-images.githubusercontent.com/107898347/204391185-88656218-0fe6-40b1-9747-99143ca86893.png)
![screenshot1--mobile-version](https://user-images.githubusercontent.com/107898347/204391186-010e0338-da9e-49ca-b469-65183c93f851.png)

### Links

- Solution URL: [News homepage solution](https://frontend-mentor-news-homepage-solution-wmdp.vercel.app)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- CSS Grid
- Mobile-first workflow

### What I learned

In this project, i improved my css and html architecture skills.
In the mobile version, i did the toggle button with the code below:

- First, in the html, on the nav i put an input type checkbox, and a div with another div within it:
```html
<nav class="header__nav">
	<input type="checkbox" class="header__menu-input">
	<div class="header__menu-burguer">
	   <div></div>
	</div>
  ...
</nav>
```

- Then, in the css, i started styling the input for it to be on the place i wanted it. When the user right-click the invisible input, it will activate the toggle.
```css
.header__menu-input {
  position: fixed;
  top: 1.5rem;
  right: 1rem;
  width: 50px;
  height: 40px;
  z-index: 2;
  opacity: 0;
  cursor: pointer;
}
```

- Only then i styled the toggle button. i first styled for the toggle to be behind the input, so the user can right-click right on top of the toggle and it will activate the input:
```css
.header__nav .header__menu-burguer {
  top: 1.5rem;
  right: 1rem;
  position: absolute;
  z-index: 1;
  width: 50px;
  height: 40px;
  display: flex;
  align-items: center;
}
```

- And then, i styled the toggle button to rotate when the input is marked with checked:
```css
.header__nav .header__menu-input:checked + .header__menu-burguer > div {
  transform: rotate(135deg);
}

.header__nav .header__menu-input:checked + .header__menu-burguer > div::before, .header__nav .header__menu-input:checked + .header__menu-burguer > div::after {
  top: 0;
  transform: rotate(90deg);
}
```

### Continued development

On my next projects, i wish to learn more about spacing, sizing units to use, other than rem, vh and vw units, for my code to be always responsive and well written.

## Author

- Frontend Mentor - [@CarenDivino](https://www.frontendmentor.io/profile/CarenDivino)
- Twitter - [@caredvn](https://twitter.com/caredvn)

## Acknowledgments

To help me with responsiveness with my toggle button, i used the video below. I thank and indicate this video for anyone who is struggling with the same thing. good luck! 
