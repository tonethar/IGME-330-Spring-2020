# DOM *Review*

- For the review questions below, assume that all of the code is running in [*strict mode*](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Strict_mode)
- In the short answer questions below, you may not use `document.getElementsByTagname()` or `document.getElementById()` etc. Instead, use one of the 2 methods we have been using in class 
- Be sure to study for the exam by reviewing the resources that we suggested --> [midterm-exam-review.md](./midterm-exam-review.md)

<hr><hr>

1. Given a page that has a &lt;button> with an `id="button1"`, write JS code to attach a click event to the button. When the button is clicked, the function should print "I was clicked" to the console.

<hr>

2. Given a page that has a &lt;select> element with the `id="dropdown1"`, write JS code to attach a change event to this select. When the chosen dropdown item of the select is changed, your function should print the current value of the dropdown to the console.

<hr>

3. Given a page with a &lt;p> element of `id="score"`, utilize JavaScript to change the visible text of the paragraph to "Score: 100"

<hr>

4. Write code that loops through the `colors` array and:
    - Creates an *unordered* list of the contents of the array
    - Adds this list to a &lt;section> of `id="content"` 
    
    `let colors=["Red", "Green", "Blue"];`
    
<hr>

5. The following code throws the error **`Uncaught TypeError: Cannot set property 'innerHTML' of null.`** Why does this error occur and how do you fix it?

```html
<!DOCTYPE html>
<html>
<head>
<title>Example 1</title>
<script>
	function init(){
		let myH1 = document.querySelector("#main");
		myH1.innerHTML="Welcome to my favorite music page";
	}
	
	init();

</script>
</head>
<body>
	<h1 id="main">This is my header</h1>
</body>
</html>
```
