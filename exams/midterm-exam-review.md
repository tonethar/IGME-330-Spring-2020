# Midterm Exam Notes

## I. Overview

**When:**
- Thursday 3/05/2020 - start of class

**What is tested:**
- Everything we've covered this semester so far, either in the Study Guides, in-class exercises, or lectures/demos is fair game - from [week 1A](../weekly/week-01A-notes.md) to [week 8A](../weekly/week-08-notes.md)

**What else:**
- No make up's allowed without prior permission.

**And:**
- a "cheat sheet" is allowed: 
  - 3x5 index card. You may write on the front and back.
  - Put your name on it as we are collecting it at the end of the exam.

## II. Test Format
- True/False
- Multiple Choice
- Short Answer
- "Write some code"
- *See the sample exam linked below*

## III. Study Resources
- **Note:** Some of these JavaScript concepts are covered in these IGME-230 notes:
  - IGME-230 JavaScript Web App notes:
    - https://github.com/tonethar/IGME-230-GDD-Spring-2018/blob/master/notes/web-apps-0.md
  - An intro to ES6 classes is here: https://github.com/tonethar/IGME-230-Master/blob/master/notes/pixi-js-2.md
- All of our **weekly notes** beginning with [week-01A-notes.md](../weekly/week-01A-notes.md) and ending with [week-08A-notes.md](../weekly/week-08A-notes.md)
- All of our **in-class demos** - which are linked from the weekly notes above
- All of our **HW assignments** - which are linked from the weekly notes above

## IV. Sample Questions
- [Midterm Review: Variables, Scope & Functions](./midterm-variables-scope-functions-review.md)
- [Midterm Review: Objects & Classes](./midterm-objects-classes-review.md)
- [Midterm Review: DOM](./midterm-dom-review.md)
- [Midterm Review: JS Modules](./midterm-js-modules-review.md)
- [Midterm Review: Web Audio](./midterm-webaudio-review.md)
- [sample-midterm-exam.md](./sample-midterm-exam.md)

## V. Major Topics (but everything is fair game)

### A. Canvas 
- Obtaining a drawing context obejct
- Drawing State Variables
- Drawing State Stack - `ctx.save()` and `ctx.restore()`
- Commonly used methods for drawing rectangles, ovals, lines, curves, etc:
  - paths
  - stroke
  - fill
- creating linear and radial gradients
- Canvas Transformations & CTM:
  - does the order of transformations matter?
  - what is the "trick" for drawing and rotating shapes around a center point?
- `.globalCompositeOperation`
- Animating via `window.requestAnimationFrame()`

### B. Image Manipulation
- pixel data
- typed arrays
- writing filters (brighten, darken, tint, etc)

### C. Web Audio
- Audio Routing Graph
  - source node
  - destination node
  - analyzer node
  - effect node(s)
- Frequency Data
- Time Domain Data
- JS Typed Arrays

### D. DOM
**A lot of this was covered in our week 1A demo**
- `querySelector(`) & `querySelectorAll()`
- event handlers and listeners
- working with buttons & form fields
- creating HTML:
  - `.innerHTML`
  - `document.createElement()`, `element.appendChild()`, ...
  - string concatenation & ES6 string templates 

### E. JavaScript Concepts
- see IGME-230 sample questions [here - Section III-B and onward](https://github.com/tonethar/IGME-230-GDD-2018-Spring/blob/master/notes/final-exam-review.md)
- variables - `var`, `let`, `const`
- scope - function, block, global, script, module
- "hoisting" - when are variables available when using `var` or `let` or `function`?
- "use strict"
- reference types v. value types
- function declarations
- function expressions
- anonymous functions
- ES6 arrow functions
- looping through arrays
- passing data from HTML elements to JavaScript: [HW-shape-viewer.md](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-shape-viewer.md)
- ES6 Classes
- ES6 Module Pattern
- Protypical Inheritance

