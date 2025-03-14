# Welcome 🙋‍♂️ to JS Numbers 🏆

🙏 Please credit me if you use this or share it with others. 🙏

### [🔙 Back To JS Readme](./js.md)

### [🔙 Back To Main Readme](../../../README.md)

## Numbers in JavaScript

In JavaScript, numbers are represented using the `Number` data type. JavaScript uses the 64-bit floating-point format (IEEE 754) to represent numbers. This format allows JavaScript to represent both integers and floating-point numbers.

### Creating Numbers

You can create numbers in JavaScript using numeric literals or the `Number` object.

```javascript
let num1 = 42; // integer
let num2 = 3.14; // floating-point number
let num3 = Number("42"); // using the Number object
```

### Arithmetic Operations

Check the operators section in the [Operators](./04_operators.md) section.

### Special Numbers

JavaScript has two special numeric values: `Infinity` and `NaN`.

- `Infinity`: Represents positive infinity. It is displayed when a number exceeds the upper limit of the floating-point numbers.
- `-Infinity`: Represents negative infinity. It is displayed when a number exceeds the lower limit of the floating-point numbers.
- `NaN`: Stands for "Not a Number." It is displayed when a mathematical operation is performed on a non-numeric value.

```javascript
console.log(1 / 0); // Infinity
console.log(-1 / 0); // -Infinity
console.log("abc" / 2); // NaN
```

### Number Methods

JavaScript provides a number of methods for working with numbers. Here are some of the most commonly used number methods:

#### `toString()`

The `toString()` method converts a number to a string.

```javascript
let num = 42;
console.log(num.toString()); // "42"
```

#### `toFixed()`

The `toFixed()` method formats a number using fixed-point notation.

```javascript
let num = 3.14159;
console.log(num.toFixed(2)); // "3.14"

num = 3.14659;
console.log(num.toFixed(2)); // "3.15"
```

#### `toPrecision()`

The `toPrecision()` method formats a number to a specified length.

```javascript
let num = 3.14159;
console.log(num.toPrecision(3)); // "3.14"

num = 3.14659;
console.log(num.toPrecision(3)); // "3.15"
```

The difference between `toFixed()` and `toPrecision()` is that `toFixed()` formats a number to a fixed number of decimal places, while `toPrecision()` formats a number to a specified length.

example:

```javascript
let num = 3.14159;
console.log(num.toFixed(2)); // "3.14"

num = 3.14659;
console.log(num.toPrecision(3)); // "3.15"
num = 3.14159;
console.log(num.toPrecision(3)); // "3.14"
```

#### `parseInt()` and `parseFloat()`

The `parseInt()` method parses a string and returns an integer. The `parseFloat()` method parses a string and returns a floating-point number.

```javascript
let num = parseInt("42");
console.log(num); // 42

num = parseFloat("3.14");
console.log(num); // 3.14
```

#### `isNaN()`

The `isNaN()` method checks if a value is `NaN`.

```javascript
console.log(isNaN(42)); // false
console.log(isNaN("42")); // false
console.log(isNaN("abc")); // true
```

#### `isFinite()`

The `isFinite()` method checks if a value is a finite number.

```javascript
console.log(isFinite(42)); // true
console.log(isFinite(Infinity)); // false
```

#### `Number()`

The `Number()` method converts a value to a number.

```javascript
let num = Number("42");
console.log(num); // 42
```

#### `Math` Object

The `Math` object provides a number of mathematical constants and functions.

```javascript
console.log(Math.PI); // 3.141592653589793
console.log(Math.E); // 2.718281828459045
console.log(Math.sqrt(16)); // 4
console.log(Math.abs(-42)); // 42
console.log(Math.round(3.14)); // 3
console.log(Math.round(3.5)); // 4
console.log(Math.floor(3.9)); // 3
console.log(Math.ceil(3.1)); // 4
console.log(Math.min(1, 2, 3)); // 1
console.log(Math.max(1, 2, 3)); // 3
console.log(Math.random()); // random number between 0 and 1
```

### Number Properties

JavaScript provides a number of properties for working with numbers. Here are some of the most commonly used number properties:

#### `MAX_VALUE` and `MIN_VALUE`

The `MAX_VALUE` property returns the largest representable number in JavaScript. The `MIN_VALUE` property returns the smallest representable number in JavaScript.

```javascript
console.log(Number.MAX_VALUE); // 1.7976931348623157e+308
console.log(Number.MIN_VALUE); // 5e-324
```

#### `POSITIVE_INFINITY` and `NEGATIVE_INFINITY`

The `POSITIVE_INFINITY` property represents positive infinity. The `NEGATIVE_INFINITY` property represents negative infinity.

```javascript
console.log(Number.POSITIVE_INFINITY); // Infinity
console.log(Number.NEGATIVE_INFINITY); // -Infinity
```

#### `NaN`

The `NaN` property represents "Not a Number."

```javascript
console.log(Number.NaN); // NaN
```

#### Length of a Number

To get the length you need to convert the number to a string and then get the length of the string.

```javascript
let num = 12345;
console.log(num.toString().length); // 5
```

### Format Numbers

JavaScript does not have a built-in number format function. However, you can create your own number format function using the `Number` object methods.

```javascript
function formatNumber(num) {
  return num.toString().replace(/\B(?=(\d{3})+(?!\d))/g, ",");
}

let num = 1234567890;
console.log(formatNumber(num)); // "1,234,567,890"
```

You can also use the local string method to format numbers.

```javascript
let num = 1234567890;
console.log(num.toLocaleString()); // "1,234,567,890"
```

### Using _ in Numbers

You can use the `_` character as a separator in numbers to make them more readable.

```javascript
let num = 1_000_000;
console.log(num); // 1000000
```

### [ ⏭ Next: Dates in JS](./10_date.md)

### [🔙 Back To JS Readme](./js.md)

### [🔙 Back To Main Readme](../../../README.md)

🙏 Please credit me if you use this or share it with others. 🙏

