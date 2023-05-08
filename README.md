# Frontend Mentor - Results summary component solution

This is a solution to the [Results summary component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/results-summary-component-CE_K6s0maV). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of contents

- [Overview](#overview)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
- [Author](#author)

## Overview

### Screenshot

![Screenshot 2023-05-08 at 23 35 16](https://user-images.githubusercontent.com/69512496/236943383-9e8743ad-eecb-43de-b697-27a5045a833a.png)

### Links

- Solution URL: https://github.com/hassanidris/results-summary-component
- Live Site URL: https://hassanidris.github.io/results-summary-component/

## My process

### Built with

- SASS / CSS Variables
- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- CSS Grid
- Mobile-first workflow

### What I learned

To see how you can add code snippets, see below:

- CSS Variables

```scss
//  ### Neutral
--clr-nut-100-white: hsl(0, 0%, 100%);
--clr-nut-200-paleBlue-nut: hsl(221, 100%, 96%);
--clr-nut-300-lightLavender: hsl(241, 100%, 89%);
--clr-nut-700-darkGrayBlue: hsl(224, 30%, 27%);

//  ### Gradient
--gradient-background: linear-gradient(hsl(252, 100%, 67%), hsl(241, 81%, 54%));
--gradient-circle: linear-gradient(
  hsla(256, 72%, 46%, 1),
  hsla(241, 72%, 46%, 0)
);
```

- Nesting media queries inside the classes

```scss
.summary {
  padding: 2.5rem;

  &__title {
    font-weight: var(--fw-bold);
    font-size: var(--fs-600);
  }

  &__output {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 1rem;
    border-radius: 0.5rem;
    background-color: hsl(var(--clr-box), 0.1);

    &[data-item-type="box-1"] {
      --clr-box: var(--clr-box-1);
    }

    &[data-item-type="box-2"] {
      --clr-box: var(--clr-box-2);
    }

    &[data-item-type="box-3"] {
      --clr-box: var(--clr-box-3);
    }

    &[data-item-type="box-4"] {
      --clr-box: var(--clr-box-4);
    }

    &-icon {
      stroke: hsl(var(--clr-box));
    }

    &-title {
      color: hsl(var(--clr-box));
    }
  }

  &__btn {
    color: var(--clr-nut-100-white);
    line-height: 1;
    background: var(--clr-nut-700-darkGrayBlue);
    padding: 1rem 2rem;
    border: 0;
    border-radius: 100vw;
    cursor: pointer;

    &:is(:hover, :focus-visible) {
      background: var(--gradient-background);
    }
  }
}
```

## Author

- Github - [hassanidris](https://github.com/hassanidris)
- Frontend Mentor - [@hassanidris](https://www.frontendmentor.io/profile/hassanidris)
