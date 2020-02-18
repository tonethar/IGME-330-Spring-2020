# Project 2 - *Audio Visualizer* (DRAFT)

[I. Overview](#overview)

  - A. [Mission](#mission)
  - B. [Resources](#resources)
  - C. [Examples](#examples)

[II. Theme & Impact](#theme)

[III. Media](#media)

[IV. Code](#code)

[V. User Experience](#user-experience)

[VI. Examples](#examples)

[VII. Rubric](#rubric)

[VIII. Documentation & Submission](#submission)

<a id="overview"/>

## I. Overview

<a id="mission"></a> 

- A) Your mission:
  - First, get a partner, and post both of your names to the discussion thread in mycourses. If you like, give your team a name. A partner is optional, you may work solo if you wish
  - *Both* partners must contribute *both* JavaScript code AND HTML/CSS to the project. This is NOT a project where team members are allowed to specialize into "Art Director" and "Software Developer" roles! Both team members shall be "Artist/Coders" (doing both) for this project
  - In this project you will build on the Web Audio Visualizer ICE and create a unique interactive audio visualization experience that utilizes the Web Audio and Canvas APIs:
  - This could be a great portfolio piece for you - so give it your best effort!
  - Ideally the experience will run in all modern browsers, but at a bare minimum it must run in recent versions of Chrome
  - The assignment is graded out of 100 points. An A grade will be awarded only for meeting the requirements below, AND going sufficiently "above and beyond" the what we did in the Audio Visualizer ICE
  - You will be evaluated on:
    - the quality of the experience you create
    - the soundness of your programming
    - meeting the requirements detailed below
    - how far you went beyond what we did in class, as described below
    
<a id="resources"></a> 
    
- B) Course Resources:
  - [HW - Audio Visualizer - Part I](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-AV-1.md)
  - [HW - Audio Visualizer - Part II](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-AV-2.md)
  - [HW - Audio Visualizer - Part III](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-AV-3.md) - *there is no dropbox for this and it will not be collected. But this is where some very helpful info on adding audio effect nodes to the visualizer (which is a requirement of the final project submission) is given to you.*
  - [Web Audio Demo](https://github.com/tonethar/IGME-330-Master/blob/master/notes/demo-web-audio-1.md)
  - [Canvas Image Data Demo](https://github.com/tonethar/IGME-330-Master/blob/master/notes/demo-canvas-image-data.md)
  - [More Web Audio](https://github.com/tonethar/IGME-330-Master/blob/master/notes/demo-more-web-audio.md)
  - [Week 5A - Tuning up our Audio Visualizers](https://github.com/tonethar/IGME-330-Spring-2019/blob/master/weekly/week-05A-notes.md)
  
<a id="examples"></a> 

 - C) Examples:
   - [Audio Visualizer Project Showcase Video (2181)](https://video.rit.edu/Watch/Si56JxGd) - projects are shown starting at 5:00
   - Here are some examples from 2171 & 2175 (most run best in Chrome, but because Chrome changed their security policy recently, it broke most of these examples, so try them in FireFox instead):
     - https://mcs2515.github.io/Magical_Visualizer/#
     - https://people.rit.edu/lpn4937/330/project1/audioVisualizer.html
     - https://people.rit.edu/bev4807/330/exercises/audio-visualizer-project/audio-visualizer-project.html
     - https://people.rit.edu/rep4975/330/project1/audio_visualizer.html
     - https://people.rit.edu/etn6701/330/Project%201/
     - https://people.rit.edu/sbm7101/330/projects/MayerWalker_AudioViz/WalkerMayer_AudioViz.html
     - https://people.rit.edu/bfc6072/330/projects/Project1_Audio_Visualizer/Audio_Visualizer.html
     - https://people.rit.edu/tjc3255/330/audio-visualizer/audio-visualizer-project.html
     - http://igm.rit.edu/~acjvks/courses/2015-fall/330/demos/p1-demo/web-audio-example.html
   - 2165 and older:
     - Conway's Game of Life Visualizer --> https://www.csh.rit.edu/~aidan/audioVisualizer/index.html

<a id="theme"/>

## II. Theme & Impact
- Explore **one** of the *themes* that we covered in class:
  - *Randomness*:
    - Random walks --> see [HW-random-walker.md](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-random-walker.md)
  - *Dynamical Systems*:
    - Chaotic Systems --> see [HW - Lorenz Attractor](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-lorenz-attractor.md)
    - Periodic functions --> see [HW - Sine Wave](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-sine-wave.md)
    - Phyllotaxis --> see [HW - Algorithmic Botany](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-algorithmic-botany.md)
    - Perlin Noise --> RESOURCES: Coding Train [Coding Challenge #136.1: Polar Perlin Noise Loops](https://www.youtube.com/watch?v=ZI1dmHv3MeM) & [Noisejs](https://github.com/josephg/noisejs)
  - *Emergence*:
    - Conway's *Game of Life* --> see [HW - Life](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-canvas-life.md)
    - Reaction Diffusion --> RESOURCE: Coding Train [Coding Challenge #13: Reaction Diffusion Algorithm in p5.js](https://www.youtube.com/watch?v=BV9ny785UNc&t=1431s)
  - or ??? (getting permission in advance is required) - here are some ideas:
    - Generative Art - here's a great blog post to give you some ideas --> https://www.artnome.com/news/2018/8/8/why-love-generative-art
    - Particle systems/falling sand app: https://github.com/pineapplemachine/websand
    - https://medium.com/better-programming/heres-what-i-learned-from-30-days-of-creative-coding-a-codevember-retrospective-8c05a8497d24
    - [Intro to Creative Coding](https://github.com/mattdesl/workshop-p5-intro/blob/master/README.md)
    - Shiffman, of course: https://www.youtube.com/user/shiffman/featured
- *Impact:*
  - This app is an *interactive sandbox*, similar to a physical sandbox where the user can experiment, create and destroy with no given objective
  - The app must do something that would be meaningful to the user, allowing them to explore the chosen theme in a compelling way
  - The creator of this app should take this assignment seriously ("engage"!) and do their **best work**
  - Here are some examples of the reverse (e.g. these are *counter examples* to be avoided):
    - not implementing specific requirements in the [rubric](#rubric) below
    - barely meeting "the minimum" on many elements of the rubric - for example:
      - writing *exactly* 3 utility functions
      - creating *exactly* 3 controls
      - using *exactly* 3 semantic HTML elements
      - having *exactly* 5 CSS style rules 
      - and so on, rather than letting the amount of these to be driven by what the app requires to work well and look good
    - copying/pasting CSS styles and layout from the demos and exercises, rather than creating their own
    - minimal modification/extension of the in-class code that was provided
    
<a id="media"/>

## III. Media
- Procedural drawing via the [CanvasRenderingContext2D](https://developer.mozilla.org/en-US/docs/Web/API/CanvasRenderingContext2D) that we have been utilizing in class is required. (Processing, Pixi.js, WebGL *et al* are NOT allowed):
  - canvas methods must be used for rectangles, arcs and lines
  - `ctx.save()` and `ctx.restore()` must be used
  - avoid using canvas convenience methods such `ctx.fillRect()` and `ctx.strokeRect()`
- HTML:
  - use semantic HTML where possible - `<header>`, `<footer>`, `<main>`, `<section>` (use at *least* 3 of these)
- CSS:
  - use an external CSS style sheet with at least 5 rules ("mobile friendly" CSS would be nice, but is not required)
  - an embedded font (ex. Google Fonts) is required
- Images:
  - if you end up using images, be sure that they are saved in a web-friendly format (JPEG, PNG or GIF) and *optimized* for web delivery. This means that their resolution (pixel dimensions) and file size are no larger than necessary.

<a id="code"/>

## IV. Code

### IV-A. File Naming Conventions
- The app file name is **index.html**
- Most of the app's code is in a file named **index.js**, which is linked from **index.html**, and located in an **src** folder
  - Most of the rest of the app's code is in your "User-created JS library" (see below)
- HTML/CSS/Image file names are [kebab-cased](https://wiki.c2.com/?KebabCase) - meaning all lower case letters -  NO spaces are allowed in file names, and dashes separate words - ex. NOT **myStyles.css** or **my styles.css**, INSTEAD USE **my-styles.css**:
- JS file names can be camel-cased in some cases. Here's an example of an exception to previous rule: 
  - *if a JS file contains a class named something like `FastCar`, you should forget about kebab-casing and instead name the file **FastCar.js***

### IV-B. Coding standards
- `"use strict";` at the top of every JS file
- `let` and `const` only. `var` is NOT allowed
- For DOM traversal, use only `document.querySelector()` and `document.querySelectorAll()`
-  NOT allowed: `document.getElementById()`, `document.getElementsByTagName()`, `document.getElementByClassName()` etc
- [**D.R.Y.**](https://en.wikipedia.org/wiki/Don%27t_repeat_yourself) - "Don't Repeat Yourself" - avoid redundancy - multiple blocks of similar code should be factored out into functions
- Avoid ["magic numbers"](https://en.wikipedia.org/wiki/Magic_number_(programming)#Unnamed_numerical_constants) and instead declare these values as variables or constants
- "inline" event handlers - ex. `<button onclick="doStuff();">My Button</button>` are NOT allowed

### IV-C. User-created JS library
- we did this in class - see "Screen Saver With Controls-5" and "Screen Saver With Controls-6" linked at the bottom of [week-02A-notes.md](../weekly/week-02A-notes.md)
- the file - named `abcLIB.js` - where `abc` are your initials - will:
  - contain some or all of utility functions that we created in class (such as `getRandomColor()`, `getRandomInt()`, `drawRectangle()` etc ...)
  - contain at least 3 (and probably more) useful utility functions that were **created by you**
  - these functions are contained in an IIFE (as was shown in the videos)
  - these functions will be exported to a global object named `abcLIB` - where `abc` are your initials (as was shown in the videos)
  - as "utility" functions these must be "pure functions" - see these notes --> [pure-function-notes.md](https://github.com/tonethar/IGME-330-Master/blob/master/notes/pure-function-notes.md)
- [IIFE-review.md](https://github.com/tonethar/IGME-330-Master/blob/master/notes/IIFE-review.md) will give you a good idea of how your project is supposed to be architected
  
### IV-D. Third-party libraries
- NOT allowed without advance approval
  
<a id="user-experience"/>

## V. User Experience
- Usability:
  - the purpose of the app and how to use it should be obvious
  - users should be able to figure out how to use the app with minimal instruction
  - the app must run without errors
- Text Content:
  - title the app - in a &lt;title> element (this helps with bookmarking and search engines)
  - title the app - in an &lt;h1></h1> element, probably using an embedded font
  - a description of what theme the project is exploring
  - instructions on how to use the app
  - if needed, use the `title` attribute of HTML elements to provide tooltips to the user
- Controls:
  - *At least* 3 distinct DOM controls that have a **meaningful effect on the experience** by allowing the user to adjust various parameters of the experience, in at least 2 of the following categories:
    - buttons (pause and play buttons DO NOT count towards this requirement)
    - sliders
    - pulldowns
    - radio buttons
    - checkboxes
  - where appropriate, HTML controls should have labels with `for` attributes to make UI element selection easier
  - Mouse interaction would be a nice plus, but is not required

<a id="examples"/>

## VI. Examples

### Spiral Generator (Procedural flower petal generation - *phylotaxis*)

![image](_images/spiral-generator.gif)

### Conway's Game of Life

![image](_images/life-example.gif)

<a id="rubric"/>

## VII. Rubric
  
  Your project will be graded on the following criteria:

| Criteria | Weight | Your Score |
| -------- | ------ | ---------- |
| **A. [Overall Theme/Impact](#theme)** | **50** | |
|    1. Does the app have an coherent and identifiable theme? | |
|    2. Does the app work as intended and it is reasonably engaging (both visually and otherwise)? | |
|    3. Does the app functionality and programming go beyond what we did in class? | |
|    4. Is the app at least *approaching/approximating* "portfolio quality" that you would not hesitate to show a potential employer? | |
|    **Overall:** Excellent/Outstanding/"Wow" (A+ = 50/50), Very Good (A = 45/50), Good (35-40/50), Fair (25-35/50), Poor (15-25/50), Unacceptable (0-15/50) ||
| &nbsp; | &nbsp; |
| **B. [User Experience](#user-experience)** | **20** | |
|    1. The purpose of the app and how to use it are obvious | |
|    2. Users should be able to figure out how to use the app with minimal instruction. The app runs without errors | |
|    3. Has required text content | |
|    4. Has required controls. Widgets are well labeled and follow interface conventions | |
|    5. Runs without errors | |
|    6. Visual design is pleasing (or at a minimum, "not ugly") | |
|    - *Missing controls* | *(-5 each)* |
|    - *Errors* | *(-? depending on severity)* |
|    **Overall:** You should aim to score 20/20 in this category ||
| &nbsp; | &nbsp; |
| **C. [Media](#media)**  | **15** | |
|    - *CSS does not pass validation* | *(-5)* |
|    - *HTML does not pass validation* | *(-5)* |
|    - *Missing required semantic HTML elements* | *(-5)* |
|    - *Majority of CSS is not in an external stylesheet* | *(-5)* |
|    - *Missing an embedded font* | *(-5)* | |
|    - *Images not properly optimized* | *(-5)* | |
|    - *Did not use `canvas.save()` or `canvas.restore()`* | *(-5)* | |
|    - *Did not draw rectangles, arcs, and lines* | *(-10)* | |
|    - *Did not use canvas API* | *0 grade on project* | |
|    **Overall:** You should aim to score 15/15 in this category ||
| &nbsp; | &nbsp; |
| **D. [Code](#code)**  | **15** | |
|    - *File Naming standards NOT followed (per incident)* | *(-1 to -5)* |
|    - *Code standards NOT followed (per incident)* | *(-1 to -5)* |
|    - *Inline event handlers used* | *(-5)* |
|    - *Missing index.js* | *(-10)* | |
|    - *Missing/improperly implemented ES5-style/IIFE Library* | *(-15)* | |
|    **Overall:** You should aim to score 15/15 in this category ||
| &nbsp; | &nbsp; |
| **Total Points Possible** | **100** | |
| &nbsp; | &nbsp; |
| **Other Deductions** | **&darr; Don't lose points for any of these! &darr;** | |
| *Deduction if required prototype is not submitted to dropbox on time* | *(-10)* | |
| *Deduction if final and complete documentation is not submitted to dropbox on time* | *(-10)* | |
| *-15% late penalty 0-24 hours after due date, -15% 24-48 hours and so on, means a maximum grad of 85% on any project that is submitted late* | *(-??)* | |

<a id="submission"/>

## VIII. Documentation & Submission
- Documentation is required:
  - *It's a good idea to document things as you are working on the project. Consider setting up a google doc right away so that you can posts links and other information there as you are working*
  - Elucidate how you met the 4 categories of requirements, and be specific about any extras you did - i.e. what code you wrote, where you went "above and beyond", and so on
  - Discuss what went right and what went wrong. List what features you would have liked to add to the project if you'd had more time/energy
  - Declare any non-course resources (libraries, sounds, images, tutorials, sample code) you utilized, in both your code comments, and in the final documentation of the project. Note: You don't have to document that you used the code we gave you in class
  - Grade the overall project and justify it. Use a grade of 0-100%.
- See dropbox for deliverables and due dates
