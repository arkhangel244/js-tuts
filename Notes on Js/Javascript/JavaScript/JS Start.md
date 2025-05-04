JS is added to a website via a script, a script is a set of instructions to automate a process. JavaScript in browser works like a script i.e. it automates the work we want the browser to render. In order to import a js script to a HTML there are a few ways:

#### Import as Script

```
<script src="Location to script"></script>
```

This is a simple way we save our js code in a .js file and then we import it in the HTML pages we need directly from the source. We need to add this in the head part of our HTML code. Though there are ways of how to import scripts because, when scripts are long it introduces unwanted behaviour to our codes. We will look into it later on how it's done.

#### Directly in the HTML

```
<script>
// This is a single-line comment
console.log("Hello, World!"); // Output to the console
</script>
```

This is another way to import js into the HTML files. This is a really bad way to keep code in HTML but just for a few lines of code this is okay.

## Basic Commands

Let's look into a few basic snippets of code to be used in our tutorial a lot. 
- **window** object - The window object represents an open window in a browser.If a document contain frames (iframe tags), the browser creates one window object for the HTML document, and one additional window object for each frame.
	- ==Properties==
	- document - Returns the Document object for the window.
	- history - Returns the History object for the window.
	- localStorage - Allows to save key/value pairs in a web browser. Stores the data with no expiration date.
	- ==Methods== 
	- alert() - Displays an alert box with a message and an OK button.
	- close() - Closes the current window
- **console** object - this provides access to browser debugging window. It is a property of the windows object.
	- ==Methods==
	-  log()  - Outputs a message to the console.
	-  assert() - Writes an error message to the console if a assertion is false.
	-  error () - Outputs an error message to the console.

We will look into this later in details, but for now we will use console object and alert for basic debugging and message printing.

Now coming back to JavaScript we need to look into how a script behaves on a web-page.  Scripts usually triggers events which changes the aspect of the web-page or helps detect information related to the web-page. For a browser js, the changes happen in a window i.e. Window is the base object over which changes can be made over the course of a session. 

###  ==Window Object Model==

![[js_window_model.webp]]
It’s the global object that represents the open window in the browser.
- All predefined methods like: _alert(“hello”)_ are attached to the global window object.
`alert("hello");     ===     window.alert("hello");`

- All new global variables and methods are also attached to the global window object.

```
var name = "John";  
console.log(name); //John  
console.log(window.name); //John
```

- BOM (Browser Object Model) data can be accessed using _window_ object.

> BOM (Browser Object Model): it contains the data about the browser rather than the document to be rendered.

# Window object Properties:

- **window.document**: it returns a reference to the document that the window contains
- **window.innerWidth**: it returns the width of the content area of the browser window.
- **window.innerHeight**: it returns the height of the content area of the browser window.
- **window.event**: it returns the **_event_** that is currently being handled by the javascript code’s context, or **_undefined_** if no event is currently being handled.
- **window.history**: it returns a reference to the history object.
- **window.name**: it sets/gets the name of the window.

and there’re much more properties you can use.(check [MDN](https://developer.mozilla.org/en-US/docs/Web/API/Window))

# Window object Methods:

- **window.alert()**: it display the default alert dialog.
- **window.confirm()**: it displays a dialog with a message that the user needs to respond to.
- **window.open()**: it opens a new window.
- **window.scroll()**: it scrolls the window _to a particular place_ in the document.
- **window.find()**: it searches for a given string in a window.
- **window.print()**: it opens the _print dialog_ to print the current document.

**window.document()** will contain most the things we would need to render the page we need. We can focus on elements in the document() select it, change its properties,move it etc.

### Variables

Variables are containers for storing data. Javascript automatically detects data-type of the variable we only need to know of the type of the variable it is, i.e. if it's a variable that will be changed later or will it be a constant variable. The two keywords used for the deceleration of variables are 
- ==let== - used to declare variables that changes through-out the scope of the program
- ==const== - used to declare const variables i.e won't change through the scope.

> N.B. const should be used a lot in js w.r.t other programming languages.

Variables should be declared before using the let and const keywords before using it in the program.  
```
let x = 5; 
const pi = 3.14;
```

### Operators

Javascript operators are used to perform different types of mathematical and logical computations.

The **Assignment Operator** **=** assigns values
The **Addition Operator** **+** adds values
The **Comparison Operator** **>** compares values
##### Types of JavaScript Operators

There are different types of JavaScript operators:
- Arithmetic Operators
- Assignment Operators
- Comparison Operators
- String Operators
- Logical Operators
- Bitwise Operators
- Ternary Operators
- Type Operators

### Strings and Dates

String and  Dates are datatypes that exhibit weird behaviour in Javascript in general though all the behaviours can't be described in a few paragraphs as it would just come working with JavaScript. 

In JavaScript, **strings** are sequences of characters used to represent text. They can be created using single, double, or backtick quotes and offer various built-in methods for manipulation, such as `.length`, `.toUpperCase()`, and `.slice()`.

```
let str = "Hello, World!";
console.log(str.length);         // 13
console.log(str.toUpperCase());  // "HELLO, WORLD!"
console.log(str[7]);             // "W"
console.log("10" + 5);           // "105" (quirk: + triggers string concatenation)
console.log("5" - 2);            // 3    (quirk: - triggers numeric conversion)

```

#### String Templates in JavaScript

**String templates**, also known as **template literals**, allow you to embed expressions directly into strings using back-ticks (`` ` ``) and the `${}` syntax. They make string construction more readable and flexible compared to traditional concatenation.
```
`string text ${expression} string text`
let name = "Alice";
let age = 25;

// Basic interpolation
let greeting = `Hello, ${name}!`;
// "Hello, Alice!"

// Multi-line string
let bio = `Name: ${name}
Age: ${age}`;
// "Name: Alice\nAge: 25"

// Expressions inside
let summary = `${name} will be ${age + 1} next year.`;
// "Alice will be 26 next year."

```
#### Date
The **Date** object in JavaScript represents a single point in time and provides methods to work with dates and times. You can create a date using `new Date()`, retrieve components like the year or month, and perform operations such as formatting or comparing dates.

```
let now = new Date();
console.log(now);                        // Current date and time
let specific = new Date("2024-12-25");
console.log(specific.getFullYear());     // 2024
console.log(specific.getMonth());    // 11 (Months are 0-indexed: Jan = 0)
let invalid = new Date("not-a-date");
console.log(invalid.toString());         // "Invalid Date"
```


























