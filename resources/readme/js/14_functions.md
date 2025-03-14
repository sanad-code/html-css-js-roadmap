# Welcome 🙋‍♂️ to JS Functions 🏆

🙏 Please credit me if you use this or share it with others. 🙏

### [🔙 Back To JS Readme](./js.md)

### [🔙 Back To Main Readme](../../../README.md)

## Functions in JavaScript

Functions are blocks of code that can be defined and called at a later time. Functions are used to perform a specific task or to calculate a value.

### Creating Functions

You can create a function using the `function` keyword followed by the function name, a list of parameters enclosed in parentheses, and the function body enclosed in curly braces.

```javascript
// Function declaration
function greet(name) {
  return `Hello, ${name}!`;
}

console.log(greet("John")); // Hello, John!
```

### Function Expressions

You can also create a function using a function expression. A function expression can be stored in a variable.

```javascript
// Function expression
let greet = function(name) {
  return `Hello, ${name}!`;
};

console.log(greet("John")); // Hello, John!
```

### Arrow Functions

Arrow functions are a more concise way to write functions. Arrow functions do not have their own `this` value. Check this guide for more information on [this in JS](./15_this.md). 

```javascript
// Arrow function
let greet = (name) => `Hello, ${name}!`;

console.log(greet("John")); // Hello, John!
```

Notes: 

- Arrow functions are not hoisted, which means they cannot be called before they are defined.
- Arrow functions do not have their own `this` value. They inherit the `this` value from the surrounding code.
- Arrow functions do not have their own `arguments` object. You can use the rest syntax instead.
- If arrow function has only one parameter, you can omit the parentheses around the parameter list. `let greet = name => `Hello, ${name}!`;`
- If arrow function is a single expression, you can omit the curly braces and the `return` keyword. `let greet = name => `Hello, ${name}!`;` This will automatically return the value of the expression.
- If arrow function has no parameters, you must include an empty pair of parentheses. `let greet = () => "Hello, World!";`
- If arrow function has multiple parameters, you must include a pair of parentheses. `let sum = (a, b) => a + b;`
- If arrow function returns an object literal, you must wrap the object literal in parentheses. `let getPerson = (name, age) => ({name, age});`

### Hoisting in JavaScript

Hoisting is a JavaScript mechanism where variables and function declarations are moved to the top of their containing scope during the compilation phase. This means that you can use a variable or function before it has been declared.

```javascript
console.log(a); // undefined
var a = 10;

console.log(b); // ReferenceError: Cannot access 'b' before initialization
let b = 20;
```

Function declarations are hoisted, but function expressions are not hoisted.

```javascript
greet("John"); // Hello, John!

function greet(name) {
  return `Hello, ${name}!`;
}
```

### Currying in JavaScript

Currying is a technique in functional programming where a function with multiple arguments is converted into a sequence of functions, each with a single argument. Currying allows you to create reusable functions with partial application.

```javascript
function add(a) {
  return function(b) {
    return a + b;
  };
}

let add5 = add(5);
console.log(add5(10)); // 15

console.log(add(5)(10)); // 15
```

### Closure in JavaScript

A closure is a function that has access to its own scope, the outer function's scope, and the global scope. Closures are used to create private variables and functions.

```javascript
function counter() {
  let count = 0;

  return function() {
    return ++count;
  };
}

let increment = counter();
console.log(increment()); // 1
console.log(increment()); // 2
console.log(increment()); // 3
```

### Arguments Object

The `arguments` object is an array-like object that contains all the arguments passed to a function. The `arguments` object is not available in arrow functions.

```javascript
function sum() {
  let total = 0;

  for (let i = 0; i < arguments.length; i++) {
    total += arguments[i];
  }

  return total;
}

console.log(sum(1, 2, 3, 4, 5)); // 15
```

### Default Parameters

You can provide default values for function parameters. If a parameter is not provided, the default value is used.

```javascript
function greet(name = "World") {
  return `Hello, ${name}!`;
}

console.log(greet("John")); // Hello, John!
console.log(greet()); // Hello, World!
```

### Rest Syntax

The rest syntax `...` allows you to collect the remaining arguments into an array.

```javascript
function sum(a, b, ...rest) {
  let total = a + b;

  for (let i = 0; i < rest.length; i++) {
    total += rest[i];
  }

  return total;
}

console.log(sum(1, 2, 3, 4, 5)); // 15
```

### Immediately Invoked Function Expression (IIFE)

An Immediately Invoked Function Expression (IIFE) is a function that is executed immediately after it is defined. IIFEs are used to create a new scope and to avoid polluting the global scope.

```javascript
(function() {
  console.log("Hello, World!");
})();

(function(name) {
  console.log(`Hello, ${name}!`);
})("John");

let sum = (function(a, b) {
  return a + b;
})(5, 10);
```

### Function Methods

Functions are objects in JavaScript, which means they have properties and methods. Here are some of the most commonly used function methods:

- `call()`: calls a function with a specified `this` value and arguments provided individually.
- `apply()`: calls a function with a specified `this` value and arguments provided as an array.
- `bind()`: creates a new function that, when called, has its `this` keyword set to the provided value.
- Check the [this in JS](./15_this.md) section for more information on `call()`, `apply()`, and `bind()`.
- `toString()`: returns a string representing the source code of the function.
- `length`: returns the number of arguments expected by the function.

### [ ⏭ Next: This in JS](./15_this.md)

### [🔙 Back To JS Readme](./js.md)

### [🔙 Back To Main Readme](../../../README.md)

🙏 Please credit me if you use this or share it with others. 🙏

