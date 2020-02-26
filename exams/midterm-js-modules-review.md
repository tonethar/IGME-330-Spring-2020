# JavaScript Modules *Review*

## I. IIFE Fun

<hr>

1) What does IIFE ("Iffy") stand for?

<hr>

2) What two things does an IIFE accomplish for you?

<hr>

3) Wrap the following code into an IIFE

```js

let name = "Jimmy";

function hello(){
  console.log(`Hello ${name}`);
}

hello();

```

<hr><hr>

## II. ES6 Module Fun

<hr>

1) **True or False.** With JavaScript ES Module syntax, there is exactly one module per file and one file per module

<hr>

2) **True or False.** One *disadvantage* of ES6 modules is that in general you will need to have a lot more &lt;script> tags in your HTML file

<hr>

3) How do you "tell" your HTML file that a particular JavaScript file is an ES6 Module (as opposed to being a regular JS file)? 

<hr>

4) **True or False.** JavaScript code written inside of an ES6 Module runs in *strict mode* by default

<hr>

5) **True or False.** JavaScript code written inside of an ES6 Module is *private* (not visible from outside the module) by default. This includes variables & functions declared with `let`, `var`, and `const`, as well as functions declared with the `function` keyword

<hr>

6) **True or False.** It is possible to create a *global* variable (i.e. visible on the `window` object) from within an ES6 Module

<hr>

7) *Modular programming* is the process of subdividing a computer program into separate sub-programs. Modules have the following characteristics:

    A) enforce logical boundaries between components and improve maintainability
  
    B) are implemented through interfaces (i.e. publicly available methods or properties)
  
    C) are designed in such a way as to minimize dependencies between different modules

    - **Describe how A above is reflected in ES6 Modules**
    - **Describe how B above is reflected in ES6 Module Syntax (*i.e. which keyword?*)**
    - **Describe how C above is reflected in ES6 Module Syntax (*i.e. which keyword?*)**

<hr>

8) Modify the code below to turn the following into an ES6 module (without using a &lt;script> tag):
  - `name` will remain "private", and NOT be visible outside of the module
  - the `hello` function will be "public", and WILL be visible outside of the module

```js

let name = "Jimmy";

function hello(){
  console.log(`Hello ${name}`);
}

```

<hr><hr>

##  II. Answer Sheet

- Test yourself!  Answer the questions without using your neighbor or the Internet
- Then check your answers by trying the code out in a browser

```text
**I. IIFE Fun**

1)

2)

3)

**II. ES6 Module Fun**

1)

2)

3)

4)

5)

6)

7)

8)
```
