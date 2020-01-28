# Week 6A - Wrap up Modules / Audio Visualizer Prototypes

## I. IIFE - "Immediately Invoked Function Expression"

- Last time we looked at ES6 modules as a way to create per-file privacy of variables, functions, and classes
- An older technique that works in any version of JavaScript is the [IIFE - "Immediately Invoke Function Expression"](https://developer.mozilla.org/en-US/docs/Glossary/IIFE) - pronounced "Iffy" - which wraps code inside of a function - therefore making it inaccessible (private) outside of this containing function.

- The base syntax of an IIFE looks like this:

```js
(function(){
    // code goes here - won't be visible in the containing scope
})();
```

- even with the wide availability of ES6 modules, there are still use cases for the IIFE
- let's go ahead and demo this technique (if we have not previously done so) on one of the AV homeworks

<hr>

<a id="review-questions"></a>
 
## II. Review Questions (ES6 Modules)

**Here are some review questions related to ES6 modules - you might see some of these on the midterm exam (which is on 7B)!**

1) **True or False.** With JavaScript ES Module syntax, there is exactly one module per file and one file per module

2) **True or False.** One *disadvantage* of ES6 modules is that in general you will need to have a lot more &lt;script> tags in your HTML file

3) How do you "tell" your HTML file that a particular JavaScript file is an ES6 Module (as opposed to being a regular JS file)? 

4) **True or False.** JavaScript code written inside of an ES6 Module runs in *strict mode* by default

5) **True or False.** JavaScript code written inside of an ES6 Module is *private* (not visible from outside the module) by default. This includes variables & functions declared with `let`, `var`, and `const`, as well as functions declared with the `function` keyword

6) **True or False.** It is possible to create a *global* variable (i.e. visible on the `window` object) from within an ES6 Module

7) *Modular programming* is the process of subdividing a computer program into separate sub-programs. Modules have the following characteristics:

    A) enforce logical boundaries between components and improve maintainability
  
    B) are implemented through interfaces (i.e. publicly available methods or properties)
  
    C) are designed in such a way as to minimize dependencies between different modules

- **Describe how A above is reflected in ES6 Modules**
- **Describe how B above is reflected in ES6 Module Syntax (*i.e. which keyword?*)**
- **Describe how C above is reflected in ES6 Module Syntax (*i.e. which keyword?*)**

<hr>

<a id="section3"></a>

## III. Writing maintainable code

- The Audio Visualizer HW code is "not scalable" demo code. It should be refactored when used in your Project 1's - let's look at some ideas of things we could do.

<hr>

### III-A. Refactor code into separate files

- Re-factor your code and put it into multiple files:
  - **loader.js**
  - **main.js**
  - **utils.js** - move `makeColor()` and `requestFullscreen()` here. Create a new helper function named `createAudioGraph()`?
  - **canvas-utils.js** - here are some helper function ideas - `showCircle()` and `showPixelEffects()`

<hr>

### III-B. Group related variables into Object literals

- The standard AV-2 HW has 15 variables scoped outside of any function definition - we could instead group them together:

```js
// main.js
let params = Object.seal({
	invert 			: false,
	tintRed 		: false, 
	noise 			: false, 
	lines 			: false,
	brightnessAmount 	: 0,
	maxRadius		: 200
});
```

**AND**

```js
// main.js
const Sounds = Object.freeze({
	sound_1: 'media/New Adventure Theme.mp3',
	sound_2: 'media/Peanuts Theme.mp3',
	sound_3: 'media/The Picard Song.mp3'
});
```

- Converting these freestanding variables to properties of an object declutters our code
- [`Object.seal()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/seal) and [`Object.freeze()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/freeze) also add compiler checks:
  - if we mistakenly add any properties to the `params` object (by misspelling a property name for example) we will get a runtime error
  - additionally, if we mistakenly modify any properties of the `Sound` object, we will get a runtime error

<hr>

### III-C. Create helper functions to reduce duplication of code and facilitate reuse

- AV-2 is duplicating a bunch of code when it draws the 3 sets of circles - how about refactoring this code into a helper function - something like this:

```js
// canvas-utils.js
function showCircle(ctx,x,y,radius,color){
  ctx.save();
  
  // draw a circle of the desired radius and color
  
  ctx.restore();
}
```

**AND**

```js
function showPixelEffects(imageData,params){
  let data = imageData.data;
  let length = data.length;
  let width = imageData.width;
	
  // do a bunch of stuff

  return imageData;
}
```


<hr>
  
### III-D. Create a helper function to reduce clutter

- We can group all of our audio related objects and nodes under one object:

```js
// utils.js
function createAudioGraph(audioElement,numSamples){
  // 1 - create new AudioContext
  let ctx = new (window.AudioContext || window.webkitAudioContext);
	
  // 2 - create a source node for our audio routing graph
  let sourceNode = ctx.createMediaElementSource(audioElement); 
	
  // do a bunch of stuff
	
  // 6 - create our object (with ES6 shorthand property notation)
  let audioGraph = {
    audioElement,
    ctx,
    sourceNode,
    bassNode,
    analyserNode
  };
	
  // 7 - freeze the object and send it back
  return Object.freeze(audioGraph);
}
```

<hr>

## IV. Project 1
- Project 1 due dates have been updated
- Look at [Project 2 - Audio Visualizer](../projects/project-2.md) prototypes
  - does your project prototype have at least the beginnings of "flair" and go beyond a *minimum effort*? 
    - https://www.youtube.com/watch?v=3vdcw415OcQ
  - does it go beyond what we did in the AV HW assignments?
  - does it represent your best work? 
  - is it a potential portfolio piece (in code and/or design) you could show employers?
  

<hr><hr>

| <-- Previous Unit | Home | Next Unit -->
| --- | --- | --- 
| [**week-05B-notes.md**](week-05B-notes.md)     |  [**IGME-330 Schedule**](../schedule.md) | [**week-06B-notes.md**](week-06B-notes.md)
