# Welcome 🙋‍♂️ to JS Convertion and Coercion 🏆

🙏 Please credit me if you use this or share it with others. 🙏

### [🔙 Back To JS Readme](./js.md)

### [🔙 Back To Main Readme](../../../README.md)

## Convertion and Coercion

Convertion and Coercion are two different things in JavaScript. Convertion is when you explicitly convert a value from one type to another (Also known as type casting). Coercion is when JavaScript automatically converts a value from one type to another.

🚨 Try to avoid coercion as it may lead to unexpected results, confusion, and bugs in your code. 🚨 

### Convertion

Convertion is when you explicitly convert a value from one type to another. You can convert a value from one type to another using the following methods:

1. `Number()`: Converts a value to a number.
2. `String()`: Converts a value to a string.
3. `Boolean()`: Converts a value to a boolean.
4. `parseInt()`: Converts a value to an integer.
5. `parseFloat()`: Converts a value to a floating-point number.
6. `toString()`: Converts a value to a string.
7. `toFixed()`: Converts a value to a string with a specified number of decimal places.
8. `toPrecision()`:  It returns a string representing the number with a specific number of significant digits.
9. `toExponential()`: Converts a value to a string in exponential notation.
10. `JSON.stringify()`: Converts a value to a JSON string.
11. `JSON.parse()`: Converts a JSON string to a JavaScript object.
12. `Array.from()`: Converts an array-like object to an array.
13. `Object.assign()`: Converts an object to another object.
14. `Object.keys()`: Converts an object to an array of keys.
15. `Object.values()`: Converts an object to an array of values.
16. `Object.entries()`: Converts an object to an array of key-value pairs.
17. `Object.fromEntries()`: Converts an array of key-value pairs to an object.

```javascript
let num = "123";
let str = 123;
let bool = 0;

console.log(Number(num)); // 123
console.log(String(str)); // "123"
console.log(Boolean(bool)); // false
console.log(parseInt("123.45")); // 123
console.log(parseFloat("123.45")); // 123.45
console.log(num.toString()); // "123"
console.log((123.45).toFixed(1)); // "123.5"
console.log((3.14159).toPrecision(4)); // "3.142"
console.log((123.45).toExponential(2)); // "1.23e+2"
console.log(JSON.stringify({ id: 1, name: "msanad"})); // "{"id":1,"name":"msanad"}"
console.log(JSON.parse('{"id":1,"name":"msanad"}')); // { id: 1, name: 'msanad' }
console.log(Array.from({ 0: "a", 1: "b", 2: "c", length: 3 })); // ["a", "b", "c"]
console.log(Object.assign({ id: 1 }, { name: "msanad" })); // { id: 1, name: 'msanad' }
console.log(Object.keys({ id: 1, name: "msanad" })); // ["id", "name"]
console.log(Object.values({ id: 1, name: "msanad" })); // [1, "msanad"]
console.log(Object.entries({ id: 1, name: "msanad" })); // [["id", 1], ["name", "msanad"]]
console.log(Object.fromEntries([["id", 1], ["name", "msanad"]])); // { id: 1, name: 'msanad' }
```

### Coercion

Coercion is when JavaScript automatically converts a value from one type to another. Coercion can be implicit or explicit.

1. Implicit Coercion: JavaScript automatically converts a value from one type to another.
2. Explicit Coercion: You can explicitly convert a value from one type to another.

```javascript
let num = 123;
let str = "123";
let bool = 0;

console.log(num + str); // "123123", in this case, JavaScript converts the number to a string and concatenates the two strings
console.log(num + bool); // 123, in this case, JavaScript converts the boolean to a number and adds the two numbers
console.log(str - num); // 0, in this case, JavaScript converts the string to a number and subtracts the two numbers
console.log(bool + str); // "0123", in this case, JavaScript converts the boolean to a string and concatenates the two strings
```


### [ ⏭ Next: Truthy & Falsy Values](./07_truthy_falsy_values.md)

### [🔙 Back To JS Readme](./js.md)

### [🔙 Back To Main Readme](../../../README.md)

🙏 Please credit me if you use this or share it with others. 🙏
