# Objects & Classes *Review*

- For the review questions below, assume that all of the code is running in *strict mode*
- Be sure to study for the exam by reviewing the resources that we suggested --> [midterm-exam-review.md](./midterm-exam-review.md)

<hr>

I. [Object Literals](#object-literals) - 6 questions

II. [Classes](#classes) - 3 questions

III. [Answer Sheet](#answer-sheet)

<hr><hr>

<a id="object-literals"/>

## I. Object Literals

1. What will be logged when this code runs?

```js
let car = {color: "red"};
car.cylinders = 10;
console.log(car.cylinders);
```

A) This will produce a runtime error

B) 10

C) undefined

<hr>

2. What will be logged when this code runs?

```js
let car = {color: "red"};
car["cylinders"] = 10;
console.log(car.cylinders);
```

A) This will produce a runtime error

B) 10

C) undefined

<hr>


3. What will be logged when this code runs?

```js
let car = {color: "red"};
console.log(car.cylinders);
```

A) This will produce a runtime error

B) 0

C) undefined

<hr>

4. What will be logged when this code runs?

```js
class Car{
	constructor(color){
		this.car = color;
	}
}

let car = new Car("red");
car.cylinders = 10;
console.log(car.cylinders);
```

A) This will produce a runtime error

B) 0

C) undefined

<hr>

5. What will be logged when this code runs?

```js
class Car{
	constructor(color){
		this.car = color;
	}
	
	repaint(newColor){
		let oldColor = this.color;
		this.color = newColor; 
	}
}

let car = new Car("red");
car.repaint("green");
console.log(car.oldColor);
```

A) This will produce a runtime error

B) "red"

C) "green"

D) undefined



<hr>

6. Create a JS [*object literal*](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Working_with_Objects) named `monster`:
    - give it a `species` property with a value of "orc"
    - give it a `hitpoints` property with a value of 10
    - give it a method named `slay()` - this method sets `hitpoints` to 0 when it is called

<hr><hr>

<a id="classes"/>

## II. Classes

1. Create an ES6 class named `Person`

    - give it a constructor that takes `age` and `name` as values
    - initialize those values as  `age` and `name` properties
    - implement a `reincarnate()` method that sets the `age` property to `0`

2. Create a new instance of `Person` called `p1`, with an `age` of 18, and `name` of `Ace Coder`

3. Write a class named `WarriorKing` that subclasses `Person`:

    - give it a constructor that takes `age` and `name` and `nemesis` as values
    - initialize the `age` and `name` properties by  calling the super class
    - create a property named `nemesis` using the passed in value

<hr><hr>

<a id="answer-sheet"/>

## III. Answer Sheet

- Test yourself!  Answer the questions without using your neighbor or the Internet
- Then check your answers by trying the code out in a browser

```text
**I. Object Literals**

1)
2)
3)
4)
5)
6)

**II. Classes**

1)
2)
3)
```

<hr><hr>



