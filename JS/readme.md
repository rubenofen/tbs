# JS

JavaScript is a programming language that is commonly used to create interactive effects within web browsers. It is a high-level, dynamic, and interpreted language that is supported by all modern web browsers. JavaScript is used to create dynamic web pages, add interactivity to existing web pages, and develop web applications.

## Table of Contents

- [Variables](#variables)
- [Data Types](#data-types)
- [Operators](#operators)
- [Conditionals](#conditionals)
- [Loops](#loops)
- [Functions](#functions)
- [Arrays](#arrays)
- [Objects](#objects)
- [DOM](#dom)
- [Resources](#resources)

## Variables

Variables are used to store information to be referenced and manipulated in a computer program. They also provide a way of labeling data with a descriptive name, so our programs can be understood more clearly by the reader and ourselves. It is helpful to think of variables as containers that hold information. Their sole purpose is to label and store data in memory. This data can then be used throughout your program.

### Declaration

variables are declared with the `var`, `let`, or `const` keyword. The `var` keyword is used in pre-ES6 versions of JS. `let` and `const` were introduced in ES6 and are block-scoped. `let` is used for variables that can be reassigned, while `const` is used for variables that cannot be reassigned.

```js
var myName = "John";
let myAge = 30;
const myBirthday = "01/01/1990";
```

### Assignment

Variables are assigned with the `=` operator. The variable to the left of the `=` is the name of the variable, while the value to the right of the `=` is the value stored in the variable.

```js
let myName = "John";
```

### Initialization

Variables can be declared and assigned in the same step. This is called initialization.

```js
let myName = "John";
```

### Reassignment

Variables can be reassigned after they are declared and assigned.

```js
let myName = "John";
myName = "Jane";
```

### Scope

Variables have either function or block scope. Variables declared with the `var` keyword are function-scoped, while variables declared with the `let` or `const` keyword are block-scoped.

```js
function myFunction() {
  var myName = "John";
  let myAge = 30;
  const myBirthday = "01/01/1990";
}
```

### Hoisting

Variables declared with the `var` keyword are hoisted to the top of the function or global scope. Variables declared with the `let` or `const` keyword are not hoisted.

```js
console.log(myName); // undefined
let myName = "John";

console.log(myAge); // ReferenceError: myAge is not defined
let myAge = 30;
```

## Data Types

Data types are the classifications we give to the different kinds of data that we use in programming. In JavaScript, there are seven fundamental data types: `number`, `string`, `boolean`, `null`, `undefined`, `symbol`, and `object`.

### Number

The `number` data type is used to represent positive or negative numbers with or without decimal places, or numbers written using exponential notation.

```js
let myAge = 30;
let pi = 3.14;
let gravity = -9.81;
let million = 1e6;
```

### String

The `string` data type is used to represent textual data. Strings are created with single or double quotes surrounding one or more characters.

```js
let myName = "John";
let myCity = "New York";
```

### Boolean

The `boolean` data type is used to represent logical values. It can only have two possible values: `true` or `false`.

```js
let isTall = true;
let isMale = false;
```

### Null

The `null` data type is used to represent a non-existent or invalid value.

```js
let myName = null;
```

### Undefined

The `undefined` data type is used to represent a declared letiable that has not been assigned a value.

```js
let myName;
```

### Symbol

The `symbol` data type is used to represent a unique identifier.

```js
let mySymbol = Symbol();
```

### Object

The `object` data type is used to represent a collection of related data.

```js
const myObject = {
  name: "John",
  age: 30,
};
```

## Operators

Operators are used to perform operations on variables and values. JavaScript has the following types of operators: assignment, arithmetic, comparison, logical, bitwise, and more.

### Assignment

The assignment operator (`=`) assigns a value to a letiable.

```js
let myName = "John";
```

### Arithmetic

Arithmetic operators perform arithmetic on numbers.

```js
let x = 10;
let y = 5;

console.log(x + y); // 15
console.log(x - y); // 5
console.log(x * y); // 50
console.log(x / y); // 2
console.log(x++); // 10
console.log(x--); // 11
console.log(++x); // 11
console.log(--x); // 10

let x = 10;
let y = 5;

console.log(x % y); // 0
console.log(x ** y); // 100000
```

### Comparison

Comparison operators compare two values and return a boolean value.

```js
let x = 10;
let y = 5;

console.log(x == y); // false
console.log(x === y); // false
console.log(x != y); // true
console.log(x !== y); // true
console.log(x > y); // true
console.log(x < y); // false
console.log(x >= y); // true
console.log(x <= y); // false
```

### Logical

Logical operators are used to determine the logic between variables or values.

```js
let x = 10;
let y = 5;

console.log(x > 5 && y < 10); // true
console.log(x > 5 || y < 10); // true
console.log(!(x > 5 && y < 10)); // false
```

### Bitwise

Bitwise operators perform bitwise operations on numbers.

```js
let x = 10;
let y = 5;

console.log(x & y); // 0
console.log(x | y); // 15
console.log(x ^ y); // 15
console.log(~x); // -11
console.log(x << y); // 320
console.log(x >> y); // 0
console.log(x >>> y); // 0
```

## Conditionals

Conditional statements are used to perform different actions based on different conditions. In JavaScript, we have the following conditional statements: `if`, `else`, `else if`, `switch`, and `ternary`.

### If

The `if` statement executes a statement if a specified condition is truthy. If the condition is falsy, another statement can be executed using the `else` statement.

```js
let myAge = 30;

if (myAge >= 18) {
  console.log("You are an adult.");
} else {
  console.log("You are a minor.");
}
```

### Else If

The `else if` statement executes a statement if a specified condition is truthy. If the condition is falsy, another statement can be executed using the `else` statement. The `else if` statement is used to specify a new condition if the first condition is falsy.

```js
let myAge = 30;

if (myAge < 18) {
  console.log("You are a minor.");
} else if (myAge >= 18 && myAge < 65) {
  console.log("You are an adult.");
} else {
  console.log("You are a senior citizen.");
}
```

### Switch

The `switch` statement evaluates an expression and executes a statement based on the value of the expression. The `break` keyword is used to terminate a case in the `switch` statement. If the `break` keyword is omitted, the next case in the `switch` statement will be executed.

```js
let myAge = 30;

switch (myAge) {
  case 18:
    console.log("You are an adult.");
    break;
  case 65:
    console.log("You are a senior citizen.");
    break;
  default:
    console.log("You are a minor.");
}
```

### Ternary

The ternary operator (`?:`) assigns a value to a letiable based on a condition. It is the only JavaScript operator that takes three operands. The operands are separated by a question mark (`?`) and a colon (`:`).

```js
let myAge = 30;
let isAdult = myAge >= 18 ? true : false;
```

## Loops

Loops are used to execute the same block of code a specified number of times or while a specified condition is true. In JavaScript, we have the following types of loops: `for`, `for...in`, `for...of`, `while`, and `do...while`.

### For

The `for` loop repeats a block of code a specified number of times.

```js
for (let i = 0; i < 10; i++) {
  console.log(i);
}
```

### For...in

The `for...in` loop iterates over the properties of an object.

```js
const myObject = {
  name: "John",
  age: 30,
};

for (let key in myObject) {
  console.log(key + ": " + myObject[key]);
}
```

### For...of

The `for...of` loop iterates over the values of an iterable object.

```js
const myArray = [1, 2, 3];

for (let value of myArray) {
  console.log(value);
}
```

### While

The `while` loop executes a block of code while a specified condition is true.

```js
let i = 0;

while (i < 10) {
  console.log(i);
  i++;
}
```

### Do...While

The `do...while` loop executes a block of code while a specified condition is true. The block of code is executed once before the condition is checked.

```js
let i = 0;

do {
  console.log(i);
  i++;
} while (i < 10);
```

## Functions

Functions are used to perform actions. They let us reuse code without having to repeat ourselves. In JavaScript, we have the following types of functions: named functions, anonymous functions, and arrow functions.

### Named

Named functions are declared with the `function` keyword followed by the name of the function.

```js
function myFunction() {
  console.log("Hello World!");
}
```

### Anonymous

Anonymous functions are declared without a name.

```js
cosnt myFunction = function () {
  console.log("Hello World!");
};
```

### Arrow

Arrow functions are a shorter syntax for writing function expressions. They are declared with the `=>` syntax.

```js
const myFunction = () => {
  console.log("Hello World!");
};
```

## Arrays

Arrays are used to store multiple values in a single letiable. In JavaScript, arrays can store different data types and are zero-indexed. JavaScript arrays are also dynamic, so they can be resized.

### Declaration

Arrays are declared with square brackets (`[]`).

```js
const myArray = [];
```

### Initialization

Arrays can be initialized when they are declared.

```js
const myArray = [1, 2, 3];
```

### Accessing Elements

Array elements are accessed with bracket notation (`[]`) and their index.

```js
const myArray = [1, 2, 3];

console.log(myArray[0]); // 1
console.log(myArray[1]); // 2
console.log(myArray[2]); // 3
```

### Modifying Elements

Array elements are modified with bracket notation (`[]`) and their index.

```js
const myArray = [1, 2, 3];

myArray[0] = 4;
myArray[1] = 5;
myArray[2] = 6;

console.log(myArray); // [4, 5, 6]
```

### Length

The length of an array is accessed with the `length` property.

```js
const myArray = [1, 2, 3];

console.log(myArray.length); // 3
```

### Iterating

Arrays can be iterated using a `for` loop.

```js
const myArray = [1, 2, 3];

for (let i = 0; i < myArray.length; i++) {
  console.log(myArray[i]);
}
```

### Methods

Arrays have many useful methods that can be used to modify their contents.

```js
const myArray = [1, 2, 3];

myArray.push(4); // [1, 2, 3, 4]
myArray.pop(); // [1, 2, 3]
myArray.shift(); // [2, 3]
myArray.unshift(1); // [1, 2, 3]
myArray.splice(1, 1); // [1, 3]
myArray.concat([4, 5]); // [1, 2, 3, 4, 5]
myArray.slice(1, 2); // [2]
myArray.reverse(); // [3, 2, 1]
myArray.sort(); // [1, 2, 3]
```

## Objects

Objects are used to store multiple values in a single letiable. In JavaScript, objects can store different data types and are accessed using keys. JavaScript objects are also dynamic, so they can be resized.

### Declaration

Objects are declared with curly braces (`{}`).

```js
const myObject = {};
```

### Initialization

Objects can be initialized when they are declared.

```js
const myObject = {
  name: "John",
  age: 30,
};
```

### Accessing Properties

Object properties could be accessed with bracket notation (`[]`) and their key.

```js
const myObject = {
  name: "John",
  age: 30,
};

console.log(myObject["name"]); // John
console.log(myObject["age"]); // 30
```

Object properties could also be accessed with dot notation (`.`) and their key.

```js
const myObject = {
  name: "John",
  age: 30,
};

console.log(myObject.name); // John
console.log(myObject.age); // 30
```

### Modifying Properties

Object properties could be modified with bracket notation (`[]`) and their key.

```js
const myObject = {
  name: "John",
  age: 30,
};

myObject["name"] = "Jane";
myObject["age"] = 25;

console.log(myObject); // { name: 'Jane', age: 25 }
```

Object properties could also be modified with dot notation (`.`) and their key.

```js
const myObject = {
  name: "John",
  age: 30,
};

myObject.name = "Jane";
myObject.age = 25;

console.log(myObject); // { name: 'Jane', age: 25 }
```

### Methods

Objects have many useful methods that can be used to modify their contents.

```js
const myObject = {
  name: "John",
  age: 30,
};

Object.keys(myObject); // [ 'name', 'age' ]
Object.values(myObject); // [ 'John', 30 ]
Object.entries(myObject); // [ [ 'name', 'John' ], [ 'age', 30 ] ]
```

## DOM

The Document Object Model (DOM) is a programming interface for HTML documents. It represents the page so that programs can change the document structure, style, and content. The DOM represents the document as nodes and objects. That way, programming languages can connect to the page.

### Selecting Elements

Elements can be selected using the `querySelector()` and `querySelectorAll()` methods.

```js
document.querySelector("h1");
document.querySelectorAll("p");
```

### Modifying Elements

Elements can be modified using the `innerHTML` and `textContent` properties.

```js
document.querySelector("h1").innerHTML = "Hello World!";
document.querySelectorAll("p").textContent = "Hello World!";
```

### Modifying Styles

Styles can be modified using the `style` property.

```js
document.querySelector("h1").style.color = "red";
document.querySelectorAll("p").style.backgroundColor = "yellow";
```

### Modifying Attributes

Attributes can be modified using the `setAttribute()` method.

```js
document.querySelector("h1").setAttribute("class", "heading");
document.querySelectorAll("p").setAttribute("class", "paragraph");
```

### Adding Classes

Classes can be added using the `classList.add()` method.

```js
document.querySelector("h1").classList.add("heading");
document.querySelectorAll("p").classList.add("paragraph");
```

### Removing Classes

Classes can be removed using the `classList.remove()` method.

```js
document.querySelector("h1").classList.remove("heading");
document.querySelectorAll("p").classList.remove("paragraph");
```

### Toggling Classes

Classes can be toggled using the `classList.toggle()` method.

```js
document.querySelector("h1").classList.toggle("heading");
document.querySelectorAll("p").classList.toggle("paragraph");
```

### Adding Event Listeners

Event listeners can be added using the `addEventListener()` method.

```js
document.querySelector("h1").addEventListener("click", function () {
  console.log("Hello World!");
});
document.querySelectorAll("p").addEventListener("click", function () {
  console.log("Hello World!");
});
```

### Removing Event Listeners

Event listeners can be removed using the `removeEventListener()` method.

```js
document.querySelector("h1").removeEventListener("click", function () {
  console.log("Hello World!");
});
document.querySelectorAll("p").removeEventListener("click", function () {
  console.log("Hello World!");
});
```

### Creating Elements

Elements can be created using the `createElement()` method.

```js
document.createElement("h1");
document.createElement("p");
```

### Appending Elements

Elements can be appended using the `appendChild()` method.

```js
document.querySelector("h1").appendChild("h1");
document.querySelectorAll("p").appendChild("p");
```

### Removing Elements

Elements can be removed using the `removeChild()` method.

```js
document.querySelector("div").removeChild("h1");
document.querySelectorAll("p").removeChild("span");
```

### Replacing Elements

Elements can be replaced using the `replaceChild()` method.

```js
document.querySelector("div").replaceChild("h1");
document.querySelectorAll("p").replaceChild("span");
```

## Resources

- [Public apis](https://apipheny.io/free-api/#apis-without-key)
- [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
- [W3Schools](https://www.w3schools.com/js/default.asp)
- [JavaScript.info](https://javascript.info/)
- [You dont know JS](https://github.com/getify/You-Dont-Know-JS)
