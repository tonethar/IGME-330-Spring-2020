# Project 2 - *Audio Visualizer*

[I. Overview](#overview)

  - [Mission](#mission)
  - [Resources](#resources)

[II. Impact](#theme)

[III. Media](#media)

[IV. Code](#code)

[V. User Experience](#user-experience)

[VI. Examples](#examples)

[VII. Rubric](#rubric)

[VIII. Documentation & Submission](#submission)

<a id="overview"/>

## I. Overview

<a id="mission"></a> 

1) Your mission:
  - First, get a partner, and post both of your names to the discussion thread in mycourses. If you like, give your team a name. A partner is optional, you may work solo if you wish
    - *Both* partners shall contribute *both* JavaScript code AND HTML/CSS to the project. This is NOT a project where team members are allowed to specialize into "Art Director" and "Software Developer" roles! Both team members shall be "Artist/Coders" (doing both) for this project
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
    
2) Course Resources:
    - [HW - Audio Visualizer - Part I](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-AV-2195-1.md)
    - [HW - Audio Visualizer - Part II](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-AV-2195-2.md)
    - [HW - Audio Visualizer - Part III](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-AV-2195-3.md)
    - [Web Audio Demo - 1](https://github.com/tonethar/IGME-330-Master/blob/master/notes/demo-web-audio-1.md)
    - [Web Audio Demo - 2](https://github.com/tonethar/IGME-330-Master/blob/master/notes/demo-web-audio-2.md)
    - [Canvas Image Data Demo](https://github.com/tonethar/IGME-330-Master/blob/master/notes/demo-canvas-image-data.md)
    - [Week 5A - Tuning up our Audio Visualizers](https://github.com/tonethar/IGME-330-Spring-2019/blob/master/weekly/week-05A-notes.md)
  


<a id="theme"/>

## II. Impact
1) The creator of this app should take this assignment seriously ("engage"!) and do their **best work**
2) Does the app functionality and programming go beyond what we did in class?
    - Is there an analogous relationship between the sound data and what people are seeing on the screen?
    - Is this project "portfolio quality" that you would not hesitate to show a potential employer?
3) READ --> [*What makes for an effective audio visualization?*](https://github.com/tonethar/IGME-330-Spring-2019/blob/master/weekly/week-05A-notes.md#effective-audio-visualizer)
4) **Impact**
    - Here are some examples of the reverse (e.g. these are *counter examples* to be avoided):
      - not implementing specific requirements in the [rubric](#rubric) below
      - barely meeting "the minimum" on many elements of the rubric  
      - copying/pasting CSS styles and layout from the demos and exercises, rather than creating their own
      - minimal modification/extension of the in-class code that was provided
      - and so on, rather than letting the amount of these to be driven by what the app requires to work well and look good
   
<a id="media"/>

## III. Media
1) Audio data (frequency and waveform) must be sampled and used to draw graphics on the canvas via the [CanvasRenderingContext2D](https://developer.mozilla.org/en-US/docs/Web/API/CanvasRenderingContext2D) that we have been utilizing in class is required. (Processing, Pixi.js, WebGL *et al* are NOT allowed):
    - canvas methods MUST be utilized for drawing either quadratic or cubic bezier curves
    - it is expected that you will also be drawing one or more of the following: rectangles, arcs, lines, text and/or images
    - you MUST utilize at least one canvas gradient (a linear OR radial gradient is fine)
    - use drawing context state variables where appropriate such as `.strokeStyle`, `.fillStyle`, `.lineWidth`, `.lineCap`, `.lineJoin`, `.globalAlpha` etc ...
    - `ctx.save()` and `ctx.restore()` MUST be used
    -  Recall that if your functions manipulate any drawing state variables, it's a good idea to `ctx.save()` the drawing state at the top of the function, and `ctx.restore()` the state at the bottom of the function
    - avoid using canvas convenience methods such `ctx.fillRect()` and `ctx.strokeRect()`
2) Bitmap data:
    - image data fetched with `ctx.getImageData()` will be manipulated with "Photoshopish" effects and then displayed to the user in some way using `ctx.putImageData()`
    - the user will be able to control or toggle the effects on and off. 
3) HTML:
    - use semantic HTML where possible - `<header>`, `<footer>`, `<main>`, `<section>` (use at *least* 3 of these)
4) CSS:
    - use an external CSS style sheet with at least 5 rules ("mobile friendly" CSS would be nice, but is not required)
    - an embedded font (ex. Google Fonts) is required
5) Images:
    - if you end up using static images, be sure that they are saved in a web-friendly format (JPEG, PNG or GIF) and *optimized* for web delivery. This means that their resolution (pixel dimensions) and file size are no larger than necessary.

<a id="code"/>

## IV. Code

### IV-A. File Naming Conventions and Organization
1) The ES6 module pattern shall be used. We covered this here --> [ES-6 Module Pattern](https://github.com/tonethar/IGME-330-Master/blob/master/notes/ES-6-module-pattern-2195.md)
2) The app file name is **index.html**:
    - this file will contain only HTML. All CSS & JS will be located in other files
3) All of the JS code files are contained in a **src** directory
4) All CSS files will be located in a folder named **styles**
5) All of the JavaScript files will utilize the ES6 module pattern, and will thus produce a public interface by having `import` and/or `export` keywords
6) There is a file named **loader.js** that is linked to from the index page. The `type` of this link is `"module"` : 
    - **loader.js** will `import` an `init()` function from **main.js** (see below)
    - NO OTHER JavaScript files will be linked from the index page, EXCEPT possibly 3rd-party libraries (if approved), or a library of your own creation (example: **abcLIB.js** from Project 1)
7) Most of the app's code is in a file named **main.js**
8) The location of most of the rest of the app's code is up to you - for example you could have **utils.js**, **canvas-utils.js**, **classes.js**, **visualizer.js** and so on
9) HTML/CSS/Image file names are [kebab-cased](https://wiki.c2.com/?KebabCase) - meaning all lower case letters -  NO spaces are allowed in file names, and dashes separate words - ex. NOT **myStyles.css** or **my styles.css**, INSTEAD USE **my-styles.css**:
10) JS file names can be camel-cased in some cases. Here's an example of an exception to the previous rule: 
    - *if a JS file contains a class named something like `FastCar`, you should forget about kebab-casing and instead name the file **FastCar.js***

### IV-B. Coding standards
1) `"use strict";` is NO LONGER NEEDED in ES6 modules, so be sure to delete this line of code
2) `let` and `const` only:
    - `var` is NOT allowed
3) For DOM traversal, use only `document.querySelector()` and `document.querySelectorAll()`
    - NOT allowed: `document.getElementById()`, `document.getElementsByTagName()`, `document.getElementByClassName()` etc
4) [**D.R.Y.**](https://en.wikipedia.org/wiki/Don%27t_repeat_yourself) - "Don't Repeat Yourself" - avoid redundancy - multiple blocks of similar code should be factored out into functions
5) Avoid ["magic numbers"](https://en.wikipedia.org/wiki/Magic_number_(programming)#Unnamed_numerical_constants) and instead declare these values as variables or constants
6) "inline" event handlers - ex. `<button onclick="doStuff();">My Button</button>` are NOT allowed

### IV-C. Third-party libraries
1) CSS Framework libraries ARE allowed - some examples are here: https://fresh.codingphase.com/articles/5-popular-css-frameworks-to-use-in-2020
2) [dat.gui](https://workshop.chromeexperiments.com/examples/gui/#1--Basic-Usage) is allowed 
3) Other libraries are NOT allowed without advance approval (but please ask if you see something that you think would be helpful to your project!)
4) It is expected and required that the code in the assignment (other than from approved libraries) is written by you. If you do end up using a small amount of code you found on the web, you must document where you got it from.  Give credit and a link for all code (fragments or otherwise) that are not written you - do so both in the code comments AND in your documentation. Failing to give credit opens you to charges of **academic dishonesty**:
   - examples of acceptable use for this project:
     - copying and lightly modifying code for an emboss effect - https://www.i-programmer.info/programming/graphics-and-imaging/2078-canvas-bitmap-operations-bitblt-in-javascript.html?start=2
     - copying and lightly modifying code for a "hamburger" menu - https://www.google.com/search?q=vanilla+javascript+hamburger+menu
   - Cite the code source **both** in the source code itself as a comment, and in your final documentation
   - Be sure to make borrowed code "your own" as much as possible for example by simplifying or improving the clarity of the code,  using `let` or `const` instead of `var`, getting rid of inline event handlers (which are prohibited in this project) and so on
   - You do not need to cite code that you received from our in-class exercises, demos or HW
   - **If you have any doubt about what is acceptable to "borrow", ask the professor *in advance* of using it**
  
  
<a id="user-experience"/>

## V. User Experience
1) Usability & Aesthetics:
    - the purpose of the app and how to use it should be obvious
    - users should be able to figure out how to use the app with minimal instruction
    - the app must run without errors
    - the app UI must NOT resemble the AV homework's UI - throw out the HW UI and start over
    - at a bare minimum, create a UI that respects the C.R.A.P. principles --> https://vwo.com/blog/crap-design-principles/
2) Text Content:
    - title the app - in a &lt;title> element (this helps with bookmarking and search engines)
    - title the app - in an &lt;h1></h1> element, probably using an embedded font
    - if needed, instructions on how to use the app
    - if needed, use the `title` attribute of HTML elements to provide tooltips to the user
3) Controls:
    - where appropriate, HTML controls should have labels with `for` attributes to make UI element selection easier
    - be sure that the default settings of these controls results in an app that starts up in a visually pleasing state
    - Required Controls:
      - the controls that we added in the Audio Visualizer exercises (play/pause button, volume slider and "Fullscreen" button)
      - a progress indicator - either in digital format such as `01:22` or as a graphical playhead or something non-standard
      - at least 2 additional sliders
      - at least 3 checkboxes
      - at least 1 radio button group
      - a way to choose between at least 3 distinct audio tracks (ideally, find your own tracks and don't reuse what we gave you) 
      - give the user the ability to view both the frequency AND the waveform data (not necessarily simultaneously)
      - add at least one additional audio effect node (besides the analyser and gain nodes that were given to you in the HW), and give the user the ability to manipulate it. Be sure that the effect is *aesthetically pleasing* and not merely tacked on to meet a requirement
     
4) Ideas for optional controls:
      - Make your entire UI minimalist by using dat.gui instead of standard DOM controls --> http://workshop.chromeexperiments.com/examples/gui/#1--Basic-Usage
      - Mouse control (clicking or moving the mouse changes how the visualizer looks)
      - Web Cam input changes how the visualizer looks:
        - The web cam demo links are here --> [Demo - Webcam Links](https://github.com/tonethar/IGME-330-Master/blob/master/notes/demo-webcam-links.md)
      - The user can load their own tracks using [HTML Drag and Drop API](https://developer.mozilla.org/en-US/docs/Web/API/HTML_Drag_and_Drop_API) or the [HTML `File` API](https://developer.mozilla.org/en-US/docs/Web/API/File)

<a id="examples"/>

## VI. Examples

- [Audio Visualizer Project Showcase Video (2181)](https://video.rit.edu/Watch/Si56JxGd) - projects are shown starting at 5:00
- Here are some examples from 2171 & 2175 (Originally, most of these ran best in Chrome, but because Chrome changed their autoplay security policy recently, it broke most of these examples, so try them in FireFox instead):
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

<a id="VI"></a>
  
### VI-A. Screenshots
  
![screenshot](./_images/av-1.jpg)
   
![screenshot](./_images/awesome.jpg)

![screenshot](./_images/disco.jpg)

![screenshot](./_images/glb-av.jpg)

![screenshot](./_images/life.jpg)

![screenshot](./_images/audio-pulse.jpg)

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
