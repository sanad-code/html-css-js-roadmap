# Welcome 🙋‍♂️ to JS Introduction 🏆

🙏 Please credit me if you use this or share it with others. 🙏

### [🔙 Back To JS Readme](./js.md)

### [🔙 Back To Main Readme](../../../README.md)

## Comments

Comments are lines that are ignored by the JavaScript engine. They are used to write notes in the code. Comments are useful for explaining what the code does, and why it does it.

```javascript
// This is a single line comment

/*
This is a multi-line comment
This is a multi-line comment
This is a multi-line comment
*/
```

## JS Console

The console is a panel that displays important messages, like errors, for developers. Much of the work the browser does is also displayed in the console. You can view logged information by opening the console.

You can also use the console to interact with JavaScript on the page. The console is part of the browser's developer tools, and is primarily used for debugging.

```javascript
console.log("Hello, World!");

console.error("This is an error message");

console.warn("This is a warning message");

console.clear(); // Clear the console

console.table({ id: 1, name: "msanad", gender: "male" }); // Display data in tabular format

//Start console group, this will group all the console logs between group and groupEnd with proper indentation
console.group("Group 1");
console.log("Hello, World!");
console.warn("Hello, World!");
console.groupEnd();
```

### [ ⏭ Next: Variables](./02_variables.md)

### [🔙 Back To JS Readme](./js.md)

### [🔙 Back To Main Readme](../../../README.md)

🙏 Please credit me if you use this or share it with others. 🙏