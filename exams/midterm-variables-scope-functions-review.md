# Variables and scope and functions *Review*

- See review questions below!
- Be sure to study for the exam by reviewing the resources that we suggested --> [midterm-exam-review.md](./midterm-exam-review.md)

<hr>

I. [Declaring variables with `var`, `let` & `const`](#variable-scope) - 15 questions

II. [Immutabilty](#immutabilty) - 6 questions 

III. [Writing JavaScript Functions](#javaScript-functions) -  2 questions

IV. [Interview-Style Question](#interview-question) - 1 question

V. [Answer Sheet](#answer-sheet)

<hr><hr>

## I. Variable Scope

### I-A. Declaring variables with `var`

- "The scope of a variable declared with `var` is its current execution context, which is either the enclosing function or, for variables declared outside any function, global. If you re-declare a JavaScript variable, it will not lose its value." - https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/var
- PS: When a function is declared with the `function` keyword, it follows the same scope rules
- "Because `var` variable declarations (and declarations in general) are processed before any code is executed, declaring a variable *anywhere* in the code is equivalent to declaring it at the top. This also means that a variable can appear to be used before it's declared. This behavior is called "hoisting", as it appears that the variable declaration is moved to the top of the function or global code."

### I-B. Declaring variables with `let` & `const`

- `"let` allows you to declare variables that are limited to a scope of a block statement, or expression on which it is used, unlike the `var` keyword, which defines a variable globally, or locally to an entire function regardless of block scope. The other difference between `var` and `let` is that the latter is initialized to a value only when a parser evaluates it..." - https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/let
- P.S. `const` has the same rules of scope as `let`
- P.P.S. If `let` is used to declare a variable *outside* of a function, method, or class, it ends up in what is called *script scope*, which is a "global-like" scope where it will be visible in other JavaScript files
- "Redeclaring the same variable (with `let`) within the same function or block scope raises a SyntaxError"


### I-C. Declaring variables inside of ES6 Modules

JavaScript code written inside of an ES6 Module is *private* (not visible from outside the module) by *default*. This includes variables & functions declared with `let`, `var`, and `const`, as well as functions declared with the `function` keyword

<hr>

<a id="variable-scope"/>

### I-D. Questions on Variable Scope

- For questions #1 - #9, what will be logged out? 
- If there is an error, write "ERROR" next to the line of code that produces it
- After you have answered all of the questions, test yourself in the debugger to see if you were right
- Assume that all of following code is running in [*strict mode*](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Strict_mode)

1. 

```js
<script>
  function init(){
    var myNum = 0;
    let myNum2 = 0;
  }
   init();
   console.log(myNum);
   console.log(myNum2);
</script>
```

<hr>

2. 

```js
<script>
  init();
  
  function init(){
    if(true){
      var myNum = 0;
    }
    console.log(myNum);
  }
</script>
```

<hr>

3.

```js
<script>
  init();
  
  function init(){
    if(true){
      let myNum = 0;
    }
    console.log(myNum);
  }
</script>
```

<hr>

4.

```js
<script>
  init();
  
  var myNum = 0;

  function init(){
    console.log(myNum);
  }
</script>
```

<hr>

5. 

```js
<script>
  init();
  let myNum = 0;

  function init(){
    console.log(myNum);
  }
</script>
```

<hr>

6. 

```js
<script>
  function init(){
    if(true){
      for(var i=0;i<5;i++){
      //
      }
    }
   console.log(i);
  }
  
  init();
  
</script>
```

<hr>

7. 

```js
<script>
  function init(){
    if(true){
      for(let i=0;i<5;i++){
      //
      }
    }
   console.log(i);
  }
  
  init();
  
</script>
```

<hr>

8. 

```js
<script>
init();

function init(){
  console.log("Hi there!");
}
</script>
```

<hr>

9. 

```js
<script>
init();

let init = () => {
  console.log("Hi there!");
}
</script>
```

<hr>

10. What is the *scope* of the `init` function below?

```js
<script>
let init = () => {
  console.log("Hi there!");
}

</script>
```

A) block

B) function/local

C) global

D) script

E) module

<hr>


11. What is the *scope* of the `init` function below?

```js
<script>
  function init(){
    console.log("Hi there!");
  }
</script>
```

A) block

B) function/local

C) global

D) script

E) module

<hr>

12. What is the *scope* of the `pi` function below?

```js
<script>
  function init(){
    console.log("pi is approximately " + pi());
		
    function pi(){
      return 3.1415;
    }
  }
</script>
```

A) block

B) function/local

C) global

D) script

E) module

<hr>

13. What is the *scope* of the `pi` function below?

```js
<script>
  function init(){
    const pi = () => {
      return 3.1415;
    }
  }
</script>
```

A) block

B) function/local

C) global

D) script

E) module

<hr>

14. What is the *scope* of `myNum`, `myNum2` & `init` below?

```js
<script type="module">
  var myNum;
  let myNum2;
  
  function init(){
    myNum = 0;
    myNum2 = 0;
  }
</script>
```

15. What is the *scope* of `myNum`, `myNum2`, `myNum3` & `myNum4` below?

```js
<script type="module">
  var myNum = 10;
  let myNum2 = 20;
  window["myNum3"] = 30;
  window.myNum4 = 40;
</script>
```

<hr><hr>

<a id="immutabilty"/>

## II. Immutability

- "The `const` declaration creates a read-only reference to a value. It does not mean the value it holds is immutable, just that the variable identifier cannot be reassigned. For instance, in the case where the content is an object, this means the object's contents (e.g., its properties) can be altered." - https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/const

- After you have answered all of the questions, test yourself in the debugger to see if you were right
- Assume that all of the following code is running in [*strict mode*](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Strict_mode)

<hr>

1. What will be logged when this code runs?

```js
const y = 1;
y++;
console.log(y);
```

A) This will produce a runtime error

B) 1

C) 2

D) undefined

<hr>

2. What will be logged when this code runs?

```js
const x = {};
x.species = "Orc";
console.log(x.species);
```

A) This will produce a runtime error

B) "Orc"

C) undefined

<hr>

3. What will be logged when this code runs?

```js
const x = {};
x = {"species":"Orc"};
x.species = "Goblin";
console.log(x.species);
```

A) This will produce a runtime error

B) "Orc"

C) "Goblin"

D) undefined

<hr>

- Read about what `Object.seal()` and `Object.freeze()` do there:
  - https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/seal
  - https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/freeze

<hr>

4. What will be logged when this code runs?

```js
const x = Object.seal({species: "Orc"});
x.species = "Goblin";
console.log(x.species);
```

A) This will produce a runtime error

B) "Orc"

C) "Goblin"

D) undefined

<hr>

5. What will be logged when this code runs?

```js
const x = Object.seal({species: "Orc"});
x.hitpoints = 10;
console.log(x.species);
```

A) This will produce a runtime error

B) "Orc"

C) "Goblin"

D) undefined

<hr>

6. What will be logged when this code runs?

```js
const x = Object.freeze({species: "Orc"});
x.species = "Goblin";
console.log(x.species);
```

A) This will produce a runtime error

B) "Orc"

C) "Goblin"

D) undefined



<hr><hr>

<a id="javascript-functions"/>

## III. Writing JavaScript Functions

1) Declare a JavaScript function named `doubleIt` that accepts a number as an argument. This function will double the number and return the result.


2) Now re-write the `doubleIt` function as an ES6 arrow function.


<hr><hr>

<a id="interview-question"/>

## IV. Interview-Style Question

- Be sure you practice the interview question at the end of [sample-midterm-exam.md](./sample-midterm-exam.md)

<hr><hr>

<a id="answer-sheet"/>

## V. Answer Sheet

- Test yourself!  Answer the questions without using your neighbor or the Internet
- Then check your answers by trying the code out in a browser

```text
**I. Variable Scope**

1) 
2) 
3)
4)
5)
6)
7)
8)
9)
10)
11)
12)
13)
14)
15)

**II. Immutability**

1)
2)
3)
4)
5)
6)

**III. Writing JavaScript Functions**

1)
2)

**Interview-Style Question**

1)
```

<hr><hr>



