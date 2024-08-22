# JavaScript Documentation for Backend Development

## Table of Contents
1. [Introduction to JavaScript](#introduction-to-javascript)
2. [Variables and Data Types](#variables-and-data-types)
3. [Operators](#operators)
4. [Control Flow](#control-flow)
5. [Loops and Iterations](#loops-and-iterations)
6. [Functions](#functions)
7. [Asynchronous JavaScript](#asynchronous-javascript)
8. [Objects and Classes](#objects-and-classes)
9. [Modules](#modules)
10. [Event Loop](#event-loop)
11. [Memory Management](#memory-management)

---

## Introduction to JavaScript

### What is JavaScript?
JavaScript is a versatile, high-level programming language widely used for web development. Initially designed for front-end tasks, it has evolved to handle backend development through environments like Node.js.

### Running JavaScript
JavaScript can be executed in:
- **Browser**: Runs within the browser’s JavaScript engine (e.g., Chrome's V8).
- **Node.js**: Allows JavaScript to run on servers using a non-blocking, event-driven architecture.

#### Example:
```javascript
console.log("Hello, World!");
```

#### Output:
```
Hello, World!
```

---

## Variables and Data Types

### Variable Declarations
JavaScript offers three ways to declare variables:
- **`var`**: Function-scoped.
- **`let`**: Block-scoped.
- **`const`**: Block-scoped and immutable.

#### Example:
```javascript
let name = "Haji";
const age = 25;
var city = "Hyderabad";

console.log(name, age, city);
```

#### Output:
```
Haji 25 Hyderabad
```

### Data Types
JavaScript includes several primitive types:
- `String`
- `Number`
- `BigInt`
- `Boolean`
- `Null`
- `Undefined`
- `Symbol`

#### Example:
```javascript
let str = "Hello";
let num = 100;
let isLoggedIn = false;

console.log(typeof str, typeof num, typeof isLoggedIn);
```

#### Output:
```
string number boolean
```

---

## Operators

JavaScript provides a variety of operators that allow you to perform different operations on values and variables.

### Arithmetic Operators
These operators are used for mathematical calculations.

- `+`: Addition
- `-`: Subtraction
- `*`: Multiplication
- `/`: Division
- `%`: Modulus (remainder)
- `++`: Increment
- `--`: Decrement

#### Example:
```javascript
let a = 5;
let b = 10;

console.log(a + b); // 15
console.log(a * b); // 50
console.log(b % a); // 0
```

### Assignment Operators
These operators assign values to variables.

- `=`: Assigns the value on the right to the variable on the left.
- `+=`: Adds the right value to the left variable and assigns the result.
- `-=`: Subtracts the right value from the left variable and assigns the result.
- `*=`: Multiplies the left variable by the right value and assigns the result.
- `/=`: Divides the left variable by the right value and assigns the result.
- `%=`: Applies modulus on the left variable by the right value and assigns the result.

#### Example:
```javascript
let x = 5;

x += 3;  // x = x + 3; x is now 8
x *= 2;  // x = x * 2; x is now 16
```

### Comparison Operators
These operators compare two values and return a boolean (`true` or `false`).

- `==`: Equal to
- `===`: Strict equal to (checks both value and type)
- `!=`: Not equal to
- `!==`: Strict not equal to (checks both value and type)
- `>`: Greater than
- `<`: Less than
- `>=`: Greater than or equal to
- `<=`: Less than or equal to

#### Example:
```javascript
let a = 10;
let b = '10';

console.log(a == b);  // true (value is the same)
console.log(a === b); // false (type is different)
console.log(a > 5);   // true
console.log(a <= 10); // true
```

### Logical Operators
Logical operators are used to combine multiple conditions.

- `&&`: Logical AND
- `||`: Logical OR
- `!`: Logical NOT

#### Example:
```javascript
let isAdult = true;
let hasID = false;

console.log(isAdult && hasID); // false (both conditions must be true)
console.log(isAdult || hasID); // true (only one condition needs to be true)
console.log(!isAdult);         // false (negates the value)
```

### Bitwise Operators
These operators perform bit-level operations on binary numbers.

- `&`: AND
- `|`: OR
- `^`: XOR (exclusive OR)
- `~`: NOT
- `<<`: Left shift
- `>>`: Right shift
- `>>>`: Zero-fill right shift

#### Example:
```javascript
let a = 5; // 0101 in binary
let b = 3; // 0011 in binary

console.log(a & b);  // 1 (0001 in binary)
console.log(a | b);  // 7 (0111 in binary)
console.log(a ^ b);  // 6 (0110 in binary)
```

### String Operators
In addition to arithmetic operations, the `+` operator is also used to concatenate strings.

- `+`: Concatenates two strings

#### Example:
```javascript
let firstName = "Haji";
let lastName = "Saklain";

console.log(firstName + " " + lastName); // Haji Saklain
```

### Ternary Operator
This is a shorthand for the `if...else` statement.

- `condition ? exprIfTrue : exprIfFalse`

#### Example:
```javascript
let age = 20;
let canVote = (age >= 18) ? "Yes" : "No";

console.log(canVote); // Yes
```

### typeof Operator
This operator returns the data type of a variable.

#### Example:
```javascript
let x = 42;
let y = "Hello";

console.log(typeof x); // number
console.log(typeof y); // string
```

---

## Control Flow

### Conditional Statements
JavaScript uses `if...else` and `switch` to control the flow of code execution.

#### If...else Example:
```javascript
let num = 5;
if (num > 0) {
    console.log("Positive");
} else {
    console.log("Negative");
}
```

#### Output:
```
Positive
```

### Switch Statement
Switch statements enable checking multiple conditions.

#### Example:
```javascript
let color = "red";
switch (color) {
    case "blue":
        console.log("Blue");
        break;
    case "red":
        console.log("Red");
        break;
    default:
        console.log("Unknown color");
}
```

#### Output:
```
Red
```

---

## Loops and Iterations

### For Loop
For loops enable repetitive execution of code blocks.

#### Example:
```javascript
for (let i = 0; i < 5; i++) {
    console.log(i);
}
```

#### Output:
```
0
1
2
3
4
```

### While Loop
While loops continue execution as long as the condition is true.

#### Example:
```javascript
let i = 0;
while (i < 3) {
    console.log(i);
    i++;
}
```

#### Output:
```
0
1
2
```

---

## Functions

### Function Declaration
Functions are reusable blocks of code that perform specific tasks.

#### Example:
```javascript
function greet(name) {
    return "Hello, " + name;
}
console.log(greet("Saklain"));
```

#### Output:
```
Hello, Saklain
```

### Arrow Functions
Arrow functions provide a concise syntax for defining functions.

#### Example:
```javascript
const greet = (name) => "Hello, " + name;
console.log(greet("Haji"));
```

#### Output:
```
Hello, Haji
```

### IIFE (Immediately Invoked Function Expression)
An IIFE runs immediately upon definition.

#### Example:
```javascript
(function() {
    console.log("IIFE executed");
})();
```

#### Output:
```
IIFE executed
```

---

## Asynchronous JavaScript

### Callbacks
A callback is a function passed as an argument to another function, to be executed after a specific event or task.

#### Example:
```javascript
function fetchData(callback) {
    setTimeout(() => {
        callback("Data received");
    }, 1000);
}

fetchData((message) => console.log(message));
```

#### Output:
```
Data received
```

### Promises
Promises simplify asynchronous tasks and prevent callback hell.

#### Example:
```javascript
const fetchData = new Promise((resolve, reject) => {
    setTimeout(() => {
        resolve("Data fetched");
    }, 1000);
});

fetchData.then((message) => console.log(message));
```

#### Output:
```
Data fetched
```

### async/await
`async/await` allows asynchronous code

 to be written more like synchronous code.

#### Example:
```javascript
async function fetchData() {
    let response = await new Promise((resolve) => {
        setTimeout(() => resolve("Data fetched"), 1000);
    });
    console.log(response);
}

fetchData();
```

#### Output:
```
Data fetched
```

---

## Objects and Classes

### Objects
Objects are collections of key-value pairs.

#### Example:
```javascript
let person = {
    name: "Haji",
    age: 25,
    city: "Karachi"
};

console.log(person.name); // Haji
```

### Classes
Classes provide a blueprint for creating objects.

#### Example:
```javascript
class Person {
    constructor(name, age) {
        this.name = name;
        this.age = age;
    }

    greet() {
        return `Hello, ${this.name}`;
    }
}

let person = new Person("Saklain", 30);
console.log(person.greet()); // Hello, Saklain
```

---

## Modules

### Import/Export
JavaScript modules allow splitting code into reusable files.

#### Export Example:
```javascript
// math.js
export function add(a, b) {
    return a + b;
}
```

#### Import Example:
```javascript
// main.js
import { add } from './math.js';

console.log(add(2, 3)); // 5
```

---

## Event Loop

### Event Loop
The event loop is a mechanism that handles asynchronous operations in JavaScript.

#### Example:
```javascript
console.log("Start");

setTimeout(() => {
    console.log("Timeout");
}, 0);

console.log("End");
```

#### Output:
```
Start
End
Timeout
```

---

## Memory Management

### Garbage Collection
JavaScript automatically allocates and deallocates memory through garbage collection.

#### Example:
```javascript
function createObject() {
    let obj = { name: "Haji" };
    return obj;
}

let newObj = createObject();
console.log(newObj); // { name: "Haji" }
```

