---
sidebar_position: 1
---

# JavaScript Intro

JavaScript is a versatile programming language primarly used in web applications. Before we build an app, let's understand the basics.

## What is a Programming Language?

A programming language is a way for humans to describe algorithms to a computer in a human-readable way. Notably, programming languages can be used to do perform calculations, store data, and control data flow. Programming languages are compiled (translated) to binary or interpreted (executed) within another program.

JavaScript is an interpreted language, meaning it needs a runtime environment to be executed. For our practice, we're going to run JavaScript in a web browser by including our code in an HTML file. So, create an `index.html` file somewhere and open it in your browser to begin.

## Project Setup

There are two options for your project setup.

### Option 1: replit.com

Assuming you already have an account, create an [HTML, CSS, JS project on replit.com](https://replit.com/new/html). Once the project is running, open the `script.js` file. You will not need to modify the HTML file.

```javascript title="script.js"
// Code goes here
```

### Option 2: Local Development

Create a text file called `index.html` on your computer. Open the file in a text editor and a browser.

Start by adding a `<script>` element to your HTML. We will add our JavaScript code between the opening and closing tags.

```html title="index.html"
<script>
  // Code goes here
</script>
```

## Outputting to the Console

The line that reads `// Code goes here` is a **comment**. Comments are inline documentation as to how your code works, they are not instructions to be executed by the computer. You will encounter comments throughout this tutorial and should use them document your own code. Commenting is a good habit and will increase the readability and understandability of your code (but don't comment every line).

We will be outputting our data and results to the `console`, which can be accessed in the Developer Tools of your browser. <kbd>F12</kbd> and <kbd>Ctrl+Shift+I</kbd> are common shortcuts to open the console.

Log data to the console by using `console.log(data)`, where `data` is replaced with whatever you want to output.

```js
// Any text data you want to use must be wrapped in quotes.
console.log("Hello!");
// You can do standard math operations and output the result.
console.log(2 * 4);
```

Console Output:

```
Hello!
8
```

## Variables: Storing Data

Now that we can output data, it's time to store, reuse, and manipulate data to build more complex programs. A **variable** is a label for stored data. Data could be text, numbers, or more complex objects like HTML elements. There are two ways to store data using variables.

### Variables with `let`

To make a variable, start the statement (line of code) with the keyword `let`, followed by a variable name. Then **assign** a value to the variable by using the assignment operator (`=`).

```javascript
let myName = "David";
```

Now whenever you **reference** the variable `myName` anywhere in the code, the value `"David"` will be used.

```javascript
console.log(myName);
```

```
David
```

#### Mutability

Variables declared with `let` are **mutable**, meaning that the value stored can be changed later. In other words, you can assign a new value to the variable as many times as you'd like. The most recently assigned item will be the one stored.

```javascript title="Using let to declare variables"
// Only write `let` when you declare (create) the variable.
let myName = "David";
console.log(myName);
// Do not include `let` for new assignments.
myName = "Jeff";
console.log(myName);
myName = "Fred";
console.log(myName);
```

```
David
Jeff
Fred
```

### Variables with `const`

#### Immutability

If you do not want or need the variable to be reassigned, use `const` to declare it. This is an **immutable** (unchangeable) way to store data.

```javascript title="Cannot reassign constant"
const pi = 3.1415927;
// TypeError: Assignment to constant variable.
pi = 3;
```

#### Modifying objects declared with `const`: Arrays

Storing more complex data is usually done with `const`. For example, let's say we have a list of names we want to store. We can use an [Array object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array) to store these names together. We can then modify our list as much as we want as long as we don't use the assignment operator again.

```javascript title="const example"
const names = ["Alice", "Bob", "Charlie"];
// This adds the name "David" to the end of the array
names.push("David");
// You can reassign individual items in the array
names[0] = "Ada";
// You just can't do this (TypeError)
names = ["New", "Names"];
// Output: ["Ada", "Bob", "Charlie", "David"]
console.log(names);
```

> Opinion: As a rule of thumb, use `const` for everything unless you need to reassign later.

## Functions: Storing Instructions

A **function** is a label for a group of instructions. We've already used a function or two in this lesson, notably `console.log()`. A function has a name, ends with `()`, and can take in 0 or more **parameters** (inputs) within those parentheses.

```javascript
zeroParameters()
oneParameter(p1)
twoParameters(p1, p2)
...
```

### Defining Functions

Here is an example that defines a function that adds two numbers together and prints them.

```javascript title="Defining add function"
function add(x, y) {
  const sum = x + y;
  console.log(sum);
}
```

Once you have defined the function, you can **call** (use) it as many times as you'd like. Each time you call the function, the instructions defined between the `{}` are executed.

```javascript title="Calling add function"
add(2, 2);
add(3, 4);
add(-1, -2);
```

```
4
7
-3
```

### Outputting From Functions: `return`

We previously established that you can input data into functions with parameters. To output data that you can use later, use `return` at the end of your function. In the visual explanation below, a function can take in inputs (parameters), do some processing, and return an output.

<img alt="Function Diagram" src="https://upload.wikimedia.org/wikipedia/commons/thumb/3/3b/Function_machine2.svg/1200px-Function_machine2.svg.png" width="250"/>

```javascript
function add(x, y) {
  const sum = x + y;
  console.log(sum);
  return sum;
}

let result = add(2, 2);
result = add(result, -4);
console.log("The final result is:", result);
```

```
4
0
The final result is: 0
```

## Practice Task: Calculator

Make a calculator that has four functions: add, subtract, multiply, and divide. The functions will each have two parameters and will return the result (sum, difference, product, and quotient). You do not need to `console.log` within your functions.

If your program works with these test cases, you are good to go.

```javascript
// Result: 6
console.log(add(12, -6));
// Result: 6
console.log(subtract(12, 6));
// Result: 0
console.log(multiply(1, 0));
// Result: Infinity
console.log(divide(1, 0));
// Result: 12
console.log(add(multiply(3, 3), divide(6, 2)));
```
