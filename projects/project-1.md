# Project 1 - *Interactive Sandbox* (DRAFT):

## I. Overview

***\*\*Note: the description and rubric of this project will be complete and assigned on Tuesday 1/28/2020 (beginning of week 3)\*\****

***\*\*Prior to that date, it's not too early to think about what you'd like to make!\*\****

You will create a compelling interactive media experience that allows the user to explore a media-related theme (of your choice)

<a id="theme"/>

## II. Theme/Impact
- Explore **one** of the *themes* that we covered in class:
  - Randomness:
    - Random walks --> see [HW-random-walker.md](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-random-walker.md)
  - Dynamical Systems:
    - Chaotic Systems --> see [HW - Lorenz Attractor](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-lorenz-attractor.md)
    - Periodic functions --> see [HW - Sine Wave](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-sine-wave.md)
    - Phyllotaxis --> see [HW - Algorithmic Botany](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-algorithmic-botany.md)
    - Perlin Noise --> RESOURCES: Coding Train [Coding Challenge #136.1: Polar Perlin Noise Loops](https://www.youtube.com/watch?v=ZI1dmHv3MeM) & [Noisejs](https://github.com/josephg/noisejs)
  - Emergence:
    - Life (IGME-330 video coming soon)
    - Reaction Diffusion --> RESOURCE: Coding Train [Coding Challenge #13: Reaction Diffusion Algorithm in p5.js](https://www.youtube.com/watch?v=BV9ny785UNc&t=1431s)
  - or ??? (getting permission in advance is required) - here are some ideas:
    - Particle systems/falling sand app: https://github.com/pineapplemachine/websand
    - https://medium.com/better-programming/heres-what-i-learned-from-30-days-of-creative-coding-a-codevember-retrospective-8c05a8497d24
    - [Intro to Creative Coding](https://github.com/mattdesl/workshop-p5-intro/blob/master/README.md)
    - Shiffman, of course: https://www.youtube.com/user/shiffman/featured
- **Impact:**
  - 
    
<a id="media"/>

## III. Media
- Procedural drawing via canvas:
  - rectangles, arcs, lines
  - `ctx.save()` and `ctx.restore()`
  - use of convenience methods `ctx.fillRect()` and 
- HTML
  - use semantic HTML where possible - `<header>`, `<footer>`, `<main>`, `<section>` etc
- CSS
  - use an external CSS style sheet with at least 5 rules ("mobile friendly" CSS would be nice, but is not required)
  - embedded font and CSS is required

<a id="code"/>

## IV. Code

### IV-A. Coding standards
- `"use strict";` at the top of every JS file
- `let` and `const` only. `var` is NOT allowed
- For DOM traversal, `document.querySelector()` and `document.querySelectorAll()` only. `document.getElementById()`, `document.getElementsByTagName()`, `document.getElementByClassName()` etc are NOT allowed
- Avoid ["magic numbers"](https://en.wikipedia.org/wiki/Magic_number_(programming)#Unnamed_numerical_constants) and instead declare these values as variables or constants
- "inline" event handlers - ex. `<button onclick="doStuff();">My Button</button> are NOT allowed

### IV-B. User-created JS library
- we did this in class - see "Screen Saver With Controls-5" and "Screen Saver With Controls-6" linked at the bottom of [week-02A-notes.md](../weekly/week-02A-notes.md)
- the file - named `abcLIB.js` - where `abc` are your initials - will:
  - contain some or all of utility functions that we created in class (such as `getRandomColor()`, `getRandomInt()`, `drawRectangle()` etc ...)
  - contain at least 3 (and probably more) useful utility functions that were **created by you**
  - these functions are contained in an IIFE (as was shown in the videos)
  - these functions will be exported to a global object named `abcLIB` - where `abc` are your initials (as was shown in the videos)
  - as "utility" functions these must be "pure functions" - [Wikipedia - Pure Function](https://en.wikipedia.org/wiki/Pure_function) - see #1 and #2 in the definition
  
### IV-C. ES6 Class
- the app must utilize at least one [ES6 class](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes)

### IV-D. Third-party libraries
- NOT allowed without advance approval
  
<a id="user-experience"/>

## V. User Experience
- Text Content:
  - title the app - in an &lt;h1></h1>, probably using an embedded font
  - a description of the project and instructions
  - if needed, use the `title` attribute to provide tooltips to the user
- Controls:
  - *At least* 3 distinct DOM controls that have a **meaningful effect on the experience**, in at least 2 of the following categories:
    - buttons
    - sliders
    - pulldowns
    - radio buttons
    - checkboxes
  - Mouse interaction would be a nice plus, but is not required


## VI. Examples

### Spiral Generator (Procedural flower petal generation - *phylotaxis*)

![image](_images/spiral-generator.gif)

### Conway's Game of Life

![image](_images/life-example.gif)

## VII. Rubric

- HTML/CSS
  - use semantic HTML where possible - `<header>`, `<footer>`, `<main>`, `<section>` etc
  - use an external CSS style sheet with at least 5 rules ("mobile friendly" CSS would be nice, but is not required)
- JavaScript
  - coding standards not followed (-1 to -5 per infraction)
  
  Your project will be graded on the following criteria:

| Criteria | Weight | Your Score |
| -------- | ------ | ---------- |
| **A. [Overall Theme/Impact](#theme)** | **25** | |
|    - Does the app have an coherent and identifiable theme? | |
|    - Does the app work as intended and visually engaging? | |
|    - Does the app functionality and programming go beyond what we did in class? | |
|    - Is the app at least *approaching/approximating* "portfolio quality" that you would not hesitate to show a potential employer? | |
| **B. [User Experience](#user-experience)** | **25** | |
|    1. Has required controls | |
|    2. Runs without errors | |
|    3. Starts in a pleasing state | |
|    4. Visual design is pleasing (or at a minimum, "not ugly") | |
|    5. Widgets are well labeled and follow interface conventions | |
|    6. Users should be able to figure out how to use the app with minimal instruction | |
|    - *Missing controls* | *(-5 each)* |
|    - *Errors* | *(-? depending on severity)* |
| **C. [Media](#canvas)**  | **25** | |
|    1. Valid HTML | |
|    2. Valid CSS | |
|    3. Images properly optimized | |
|    - *Majority of CSS not in external file* | *(-5)* |
|    - *Missing required HTML elements* | *(-5 each)* |
| **D. [Code](#code)**  | **25** | |
|    1. *Standards NOT followed* | *(-1 to -5)* |
|    2. *Inline event handlers used* | *(-5)* |

| **Above and Beyond (You need to document this)** | **5** | |
| **Possible Total Points** | **100** | |
| **Deductions** | **&darr; Don't lose points for any of these! &darr;** | |
| *Deduction if missing an embedded font* | *(-5)* | |
| *Deduction if missing a CSS framework or modern web layout* | *(-10)* | |
| *Deduction if missing ES6 Module Pattern* | *(-15)* | |
| *Deduction if required prototype is not submitted to dropbox on time* | *(-10)* | |
| *Deduction if final and complete documentation is not submitted to dropbox on time* | *(-10)* | |

Note:
- **Good** (Meet all requirements above reasonably well) = 90%
- **Better** (Go beyond expectations in 2 or more areas) = 95%
- **Best** (Go significantly beyond expectations in 2 or more areas) = 100%



## VIII. Submission
- Documentation is required and consists of:
  - ...
- See dropbox for deliverables and due dates
