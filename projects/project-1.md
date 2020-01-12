# Project 1 - *Interactive Sandbox* (DRAFT):

## I. Overview

## II. Theme
- Explore one of the *themes* that we covered in class:
  - Dynamical Systems (Periodic functions, Phylotaxis, ...)
  - Randomness (Random walks, Perlin noise)
  - Emergence (Life, Reaction Diffusion)
  - or ??? (getting permission in advance is required):
    - particle systems/falling sand app: https://github.com/pineapplemachine/websand
    - more ideas: https://medium.com/better-programming/heres-what-i-learned-from-30-days-of-creative-coding-a-codevember-retrospective-8c05a8497d24
    - [Intro to Creative Coding](https://github.com/mattdesl/workshop-p5-intro/blob/master/README.md)
    - Shiffman, of course: https://www.youtube.com/user/shiffman/featured
    

## III. Media
- procedural drawing via canvas:
  - rectangles, arcs, lines
  - `ctx.save()` and `ctx.restore()`
  - use of convenience methods `ctx.fillRect()` and 
- embedded font and CSS is required

## IV. JavaScript

### IV-A. Coding standards
- `let` and `const` only. `var` is NOT allowed
- For DOM traversal, `document.querySelector()` and `document.querySelectorAll()` only. `document.getElementById()`, `document.getElementsByTagName()`, `document.getElementByClassName()` etc are NOT allowed

### IV-B. User-created JS library
- the file - named `abcLIB.js` - where `abc` are your initials - will:
  - contain at least XX utility functions
  - these functions are contained in an IIFE
  - these functions will be exported to a global object named `abcLIB` - where `abc` are your initials
  - as "utility" functions these are ["pure functions"](https://en.wikipedia.org/wiki/Pure_function) - meaning that ...
  
### IV-C. ES6 Class
- the app must utilize at least one ES6 class

### IV-D. Third-party libraries
- NOT allowed without advance approval
  

## VI. User Experience
- At least XX distinct DOM controls that have a **meaningful effect on the experience**, in at least XX of the following categories:
  - buttons
  - sliders
  - pulldowns
  - radio buttons
  - checkboxes
- mouse interaction would be a nice plus, but is not required

## VII. Examples

### Spiral Generator

![image](_images/spiral-generator.gif)

![image](_images/life-example.gif)

## VIII. Rubric

- HTML/CSS
  - use semantic HTML where possible - `<header>`, `<footer>`, `<main>`, `<section>` etc
  - use an external CSS style sheet with at least 5 rules ("mobile friendly" CSS would be nice, but is not required)
- JavaScript
  - coding standards not followed (-1 to -5 per infraction)


## IX. Submission
- Documentation is required and consists of:
  - ...
- See dropbox for deliverables and due dates
