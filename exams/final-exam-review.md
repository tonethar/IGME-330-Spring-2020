# Final Exam Review

## I. When is it?
- The final written exam:
  - It will be given in class during our final regular, meeting week 14

## II. What's on it? How do I study?
- Everything that was covered for the entire semester is fair game, so be sure to review the course material from prior to the midterm --> [Midterm Exam Review](../exams/midterm-exam-review.md)
- Review questions covered since midterm exam:
  - [week-12A-notes.md#review](../weekly/week-12A-notes.md#review)
  - [week-12B-notes.md#review](../weekly/week-12B-notes.md#review)
- Review course notes and lecture videos, they are linked in mycourses

## III. More review questions

### III-A. Unstructured Text

- See **Text** notes #1-#5 starting here --> [Text 1 - Loading plain text](https://github.com/tonethar/IGME-330-Master/blob/master/notes/text-5.md)
- See **Text** "wrap up" here --> [week-10B-notes.md#review](../weekly/week-10B-notes.md#review)

1) Give examples of *constrained writing* techniques

2) What do the following JavaScript methods do?
  - `array.join()`
  - `string.replace()`
  - `string.split()`
  - `string.trim()`
  
3) Give an example of a regular expression *Metacharacter* - https://help.relativity.com/9.3/Content/Relativity/Regular_expressions/Regular_expression_metacharacters.htm

4) What are *stop words*?

5) What is a *grammar*?

6) What is the difference between a *terminal symbol* and a *non-terminal symbol*?

7) What happens when we `.expand()` a grammar?

8) Give an example of a PENN part-of-speech tag (these tags are returned by the RiTa `pos()` method)


### III-B. ES6 Classes & Modules

1) Let's suppose we have a web service that returns "pet of the day" data in a JSON format. Properties of the JSON include the `species`, `description`, and `url` of the pet:
  - create an ES6 class named `CutePet` that contains these 3 values as properties
  - the class will have a constructor to initialize these values
  - BONUS: create JS setters and getters for this class, and write validation code in the setters that guarantees that these 3 properties will always have a default value
  
  
2) Turn the following code into an ES6 module by making just the `doubleIt()` function "public" and visible from the outside of the file. `SECRET` should be "private" to the file.

```js
// this code is in a file named mylib.js

const SECRET = 42;

function doubleIt(num){
  return num * 2;
}
```

### III-C. Node.js & npm

1) Which JavaScript *engine* does **Node.js** use?

2) Does **Node.js** run on the *client-side*, *server-side*, or *both*?

3) Why doesn't **Node.js** have a `window` object and *DOM manipulation*  methods?

4) Write the line of code that imports a package named `cowsay`

5) What does `npm` allow us to download and manage?

6) What is contained in a *package.json* file?

7) What is *transpiling*?

8) What does the **webpack** package do?


### III-D. Web Services

- Also see the other web service review questions linked above (12A)

```js
let json = {
  "statusCode": 200, 
  "results": [{"firstName": "Jimmy"},{"firstName": "Johnny"}, {"firstName": "Jilly"}]
 };
 ```

1) Write code that logs out the value of `statusCode` above

2) Write code that loops though all of the `results` above and logs out the value of all the `firstName` properties

3) What is the name of the format of the following data? (ANSWER: *JSONP - which stands for "JSON with padding" - note the callback function. This won't be on the exam*)

```js
dataLoaded({
  "statusCode": 200, 
  "results": [{"firstName": "Jimmy"},{"firstName": "Johnny"}, {"firstName": "Jilly"}]};
});
```

4) Give the HTTP response header than "turns on" CORS so that a web browser can access a web service directly

5) Explain what a *proxy server* does

6) Write code that will access the &lt;city> value below. Assume that this XML is a parseable `DOMDocument` that is stored in a variable named `xmlDOM`:

```js
let xmlString = `
<locations>
  <place>
    <title>
      RIT
    </title>
    <location>
      <street>
        Jefferson Road
      </street>
      <city>
        Henrietta
      </city>
    </location>
  </place>
</locations>
`;

let domParser = new DOMParser();
let xmlDOM = domParser.parseFromString(xmlString, "application/xml");
```


### III-E. Firebase

1)  Which method of a firebase reference adds a new JSON object to that reference AND auto-assigns a new key?

2)  Which method of a firebase reference replaces a JSON object and allows the developer to assign the object’s key?

3)  Which method of a firebase reference is used to "listen" for the change in a value?



### III-F. Vue.js

- See **Vue** Notes #1-#4 starting here --> [Vue Part I - Introduction to Vue.js](https://github.com/tonethar/IGME-330-Master/blob/master/notes/vue-1.md)
- See the "ReVue" Vue.js review questions (12B) linked above
- Sample Question:

**Re-write the HTML below so that when the button is clicked, the `sayHello()` method will be called, and the paragraph is updated to display the value of `message`. You will not need to modify the JavaScript.**

```html
<div id="root">
	<button>Click Me!</button>
	<p></p>











</div>

<script>
const app = new Vue({
	el: "#root",
	data: {
		message: "???"
	},
	methods: {
		sayHello(){
			this.message="Hi!";
		}
	}

});

</script>
```


