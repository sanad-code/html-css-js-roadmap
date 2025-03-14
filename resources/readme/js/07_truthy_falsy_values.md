# Welcome 🙋‍♂️ to JS Truthy and Falsy Values 🏆

🙏 Please credit me if you use this or share it with others. 🙏

### [🔙 Back To JS Readme](./js.md)

### [🔙 Back To Main Readme](../../../README.md)

## Truthy and Falsy Values

### Falsy Values in JavaScript

In JavaScript, a falsy value is a value that translates to false when evaluated in a Boolean context. Falsy values are:

1. `false`
2. `0`,`-0`, `0.0` (all forms of zero)
3. `0n` (BigInt)
4. `""` (empty string)
5. `null`
6. `undefined`
7. `NaN` (Not a Number)
8.  `document.all` The only false object in JavaScript

### Truthy Values in JavaScript

Any value that is not falsy is truthy.


```javascript
console.log(Boolean(false)); // false
console.log(Boolean(0)); // false
console.log(Boolean(-0)); // false
console.log(Boolean(0n)); // false
console.log(Boolean("")); // false
console.log(Boolean('')); // false
console.log(Boolean(null)); // false
console.log(Boolean(undefined)); // false
console.log(Boolean(NaN)); // false
console.log(Boolean(document.all)); // false
console.log(Boolean(true)); // true
console.log(Boolean(1)); // true
console.log(Boolean(-1)); // true
console.log(Boolean(0.1)); // true
console.log(Boolean("0")); // true
console.log(Boolean("false")); // true
console.log(Boolean([])); // true
console.log(Boolean({})); // true
console.log(Boolean(function(){})); // true
console.log(Boolean(new Date())); // true
console.log(Boolean(/test/)); // true
console.log(Boolean(new Error())); // true
```

### [ ⏭ Next: Strings](./08_strings.md)

### [🔙 Back To JS Readme](./js.md)

### [🔙 Back To Main Readme](../../../README.md)

🙏 Please credit me if you use this or share it with others. 🙏

