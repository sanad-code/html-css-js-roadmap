# Welcome 🙋‍♂️ to JS Variables 🏆

🙏 Please credit me if you use this or share it with others. 🙏

### [🔙 Back To JS Readme](./js.md)

### [🔙 Back To Main Readme](../../../README.md)

## Variables

Variables are containers for storing data values. In JavaScript, a variable is declared using the `var`, `let`, or `const` keyword.

### `var`

The `var` keyword is used to declare a variable. The variable can be reassigned and redeclared.

**The `var` scope is function-scoped.**

Function scope is an area within a function. Variables declared inside a function are only accessible to the code within the function.

**`var` is subjected to hoisting (We will talk later about hoisting). This means that you can use a variable before it is declared.**

```javascript
console.log(name); // undefined
var name = "msanad";
```

🚨 DONT ever use `var` keyword to declare a variable. It is an old way of declaring variables in JavaScript. Use `let` and `const` instead. 🚨

Only use it if you know what you are doing. 📢

```javascript
var name = "msanad";
console.log(name); // msanad
name = "Yassien"; // This is reassignment
console.log(name); // Yassien

var name = "Ahmed"; // This is redeclaration
console.log(name); // Ahmed
```

### `let`

The `let` keyword is used to declare a variable. The variable can be reassigned but not redeclared.

**The `let` scope is block-scoped.**

Block scope is an area within if, switch conditions or for and while loops. Variables declared inside a block scope are only accessible to the code within the curly braces `{}`.

**`let` is not subjected to hoisting.**

```javascript
console.log(name); // ReferenceError: Cannot access 'name' before initialization
let name = "msanad";
```

```javascript
let name = "msanad";
console.log(name); // msanad
name = "Yassien"; // This is reassignment
console.log(name); // Yassien
let name = "Ahmed"; // SyntaxError: Identifier 'name' has already been declared
```

### `const`

The `const` keyword is used to declare a variable. The variable cannot be reassigned or redeclared.

**Always favor using `const` over `let` if you are not going to reassign the variable.**

**The `const` scope is block-scoped.**

**`const` is not subjected to hoisting.**

```javascript
console.log(name); // ReferenceError: Cannot access 'name' before initialization
const name = "msanad";
```

```javascript
const name = "msanad";
console.log(name); // msanad
name = "Yassien"; // TypeError: Assignment to constant variable.
const name = "Ahmed"; // SyntaxError: Identifier 'name' has already been declared
```

🚨 **Important Note:** If you declare an object or an array using `const`, you can still modify the object or array. You just can't reassign the variable. 🚨

```javascript
const person = { name: "msanad", mobile: "123456789" };
console.log(person); // { name: 'msanad', mobile: '123456789' }
person.name = "Yassien"; // This is object modification not reassignment, this is allowed
console.log(person); // { name: 'Yassien', mobile: '123456789' }
person = { name: "Ahmed", mobile: "987654321" }; // TypeError: Assignment to constant variable. As this is reassignment
```

```javascript
const numbers = [1, 2, 3, 4, 5];
console.log(numbers); // [ 1, 2, 3, 4, 5 ]
numbers.push(6); // This is array modification not reassignment, this is allowed
console.log(numbers); // [ 1, 2, 3, 4, 5, 6 ]
numbers = [6, 7, 8, 9, 10]; // TypeError: Assignment to constant variable. As this is reassignment
```

## Variable Naming

- Variable names can only contain letters, numbers, `$`, and `_`.
- Variable names cannot start with a number.
- Variable names are case-sensitive.
- Variable names cannot be reserved keywords like `let`, `const`, `var`, `function`, `if`, `else`, `for`, `while`, `switch`, `case`, `break`, `continue`, `return`, `class`, `extends`, `super`, `static`, `new`, `this`, `null`, `undefined`, `true`, `false`, `typeof`, `instanceof`, `delete`, `try`, `catch`, `finally`, `throw`, `with`, `debugger`, `import`, `from`, `as`, `export`, `default`, `await`, `async`, `let`, `const`, `var`, `function`, `if`, `else`, `for`, `while`, `switch`, `case`, `break`, `continue`, `return`, `class`, `extends`, `super`, `static`, `new`, `this`, `null`, `undefined`, `true`, `false`, `typeof`, `instanceof`, `delete`, `try`, `catch`, `finally`, `throw`, `with`, `debugger`, `import`, `from`, `as`, `export`, `default`, `await`, `async`.
- Variable names should be descriptive and meaningful, avoid using single-letter variable names like `x`, `y`, `z`.
- Variable names should be in camelCase. Like `firstName`, `lastName`, `mobileNumber`, `emailAddress`.

```javascript
const firstName = "Moataz",
  lastName = "Sanad"; // You can declare multiple variables in one line using , (comma)
```

### [ ⏭ Next: Data Types](./03_data_types.md)

### [🔙 Back To JS Readme](./js.md)

### [🔙 Back To Main Readme](../../../README.md)

🙏 Please credit me if you use this or share it with others. 🙏
