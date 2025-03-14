# Welcome 🙋‍♂️ to JS Strings 🏆

🙏 Please credit me if you use this or share it with others. 🙏

### [🔙 Back To JS Readme](./js.md)

### [🔙 Back To Main Readme](../../../README.md)

## Strings in JavaScript

Strings are used to store text. Strings must be enclosed in quotes. You can use single or double quotes to create a string.

`IMPORTANT: Strings are immutable in JavaScript. This means that once a string is created, it cannot be changed. 🚨🔥`

```javascript
let str1 = "Hello, World!";
let str2 = 'Hello, World!';
```
### String concatenation

You can concatenate strings using the `+` operator.

`IMPORTANT: Using the + operator to concatenate strings is not recommended. It is better to use template literals or the concat() method. 🚨🔥`

```javascript
let str1 = "Hello,";
let str2 = "World!";
let str3 = str1 + " " + str2; // Hello, World!
```

### Template literals

Template literals are enclosed in backticks (` `) and can contain placeholders `${expression}`. The expressions in the placeholders are evaluated and the result is concatenated with the rest of the string.

`IMPORTANT: Template literals are the recommended way to concatenate strings in JavaScript. 🏆`

```javascript
let str1 = "Hello,";
let str2 = "World!";
let str3 = `${str1} ${str2}`; // Hello, World!
```

### String methods & properties

JavaScript provides a number of methods for working with strings. Here are some of the most commonly used string methods:

#### `length` this is property not a method

The `length` property returns the length of a string.

```javascript
let str = "Hello, World!";
console.log(str.length); // 13
```

#### `toUpperCase()` and `toLowerCase()`

The `toUpperCase()` method converts a string to uppercase. The `toLowerCase()` method converts a string to lowercase.

```javascript
let str = "Hello, World!";
console.log(str.toUpperCase()); // HELLO, WORLD!
console.log(str.toLowerCase()); // hello, world!
```

#### `charAt()` and `charCodeAt()`

The `charAt()` method returns the character at a specified index in a string. The `charCodeAt()` method returns the Unicode value of the character at a specified index in a string.

```javascript
let str = "Hello, World!";
console.log(str.charAt(0)); // H
console.log(str.charCodeAt(0)); // 72

// Don't every try to change the value of a string using charAt() method, strings are immutable
str.charAt(0) = "h"; // TypeError: Cannot assign to read only property '0' of string 'Hello, World!'
```

#### `indexOf()` and `lastIndexOf()`

- The `indexOf()` method returns the index of the **first occurrence** of a specified value in a string. 
- The `lastIndexOf()` method returns the index of the **last occurrence** of a specified value in a string.

```javascript
let str = "Hello, World!";
console.log(str.indexOf("o")); // 4
console.log(str.lastIndexOf("o")); // 8
```

#### `includes()`, `startsWith()`, and `endsWith()`

- The `includes()` method returns `true` if a string contains a specified value, otherwise it returns `false`.
- The `startsWith()` method returns `true` if a string starts with a specified value, otherwise it returns `false`. It is case-sensitive.
- The `endsWith()` method returns `true` if a string ends with a specified value, otherwise it returns `false`. It is case-sensitive.

```javascript
let str = "Hello, World!";
console.log(str.includes("o")); // true
console.log(str.startsWith("Hello")); // true
console.log(str.endsWith("World!")); // true
console.log(str.startsWith("h")); // false
```

#### `slice()`, `substring()`, and `substr()`

- The `slice()` method extracts a part of a string and returns the extracted part in a new string.
- The `substring()` method extracts a part of a string and returns the extracted part in a new string. It is similar to `slice()`, but it cannot accept negative indexes.
- The `substr()` method extracts a part of a string and returns the extracted part in a new string. It takes two arguments: the starting index and the length of the substring.

```javascript
let str = "Hello, World!";
let pdx = "0123456789012"; // positive index respective to the string
let ntr = "Hello, World!";
let ndx = "2109876543210"; // negative index respective to the string
console.log(str.slice(7)); // World! 7 is not included
console.log(str.slice(7, 12)); // World
console.log(str.substring(7)); // World!
console.log(str.substring(7, 12)); // World
console.log(str.substr(7)); // World!
console.log(str.substr(7, 5)); // World

// Negative indexes
console.log(str.slice(-6)); // World! -6 is not included
console.log(str.slice(-6, -1)); // World -1 is not included, -6 is included

console.log(str.substring(-6)); // Hello, World! -6 is treated as 0
console.log(str.substring(-6, -1)); // Hello, World! -6 is treated as 0, -1 is treated as 0

console.log(str.substr(-6)); // World! -6 is the starting index
console.log(str.substr(-6, 5)); // World -6 is the starting index, 5 is the length
```

#### `replace()` and `replaceAll()`

- The `replace()` method replaces a specified value with another value in a string. **It replaces only the first occurrence of the specified value**.
- The `replaceAll()` method replaces all occurrences of a specified value with another value in a string.

```javascript
let str = "Hello, World!";
console.log(str.replace("o", "0")); // Hell0, World!
console.log(str.replaceAll("o", "0")); // Hell0, W0rld!
```

#### `split()` and `join()`

- The `split()` method splits a string into an array of substrings based on a specified separator. If the separator is an empty string, the string is split into an array of characters.
- The `join()` method joins the elements of an array into a string, and returns the string.

```javascript
let str = "Hello, World!";
console.log(str.split(" ")); // ["Hello,", "World!"]
console.log(str.split("")); // ["H", "e", "l", "l", "o", ",", " ", "W", "o", "r", "l", "d", "!"]
console.log(str.split("o")); // ["Hell", ", W", "rld!"]
console.log(str.split("o").join("0")); // Hell0, W0rld!

let arr = ["Hello,", "World!"];
console.log(arr.join(" ")); // Hello, World!
```

#### `trim()`

The `trim()` method removes whitespace from both ends of a string.

```javascript
let str = "   Hello, World!   ";
console.log(str.trim()); // Hello, World!
```

#### `repeat()`

The `repeat()` method returns a new string with a specified number of copies of the string it was called on.

```javascript
let str = "Hello, World!";
console.log(str.repeat(3)); // Hello, World!Hello, World!Hello, World!

console.log("*".repeat(10)); // **********
console.log("*" * 10 ); // NaN
```

#### `valueOf()`, `toString()`

- The `valueOf()` method returns the primitive value of a string object.
- The `toString()` method returns a string representing the specified object.

```javascript
let str = new String("Hello, World!");
console.log(str.valueOf()); // Hello, World!
console.log(str.toString()); // Hello, World!
```

If you forget about string methods and you don't have internet access, you can use the following code to get all the string methods and properties.

```javascript
let str = "Hello, World!";
console.log(str.__proto__); // String {"", constructor: ƒ, anchor: ƒ, big: ƒ, blink: ƒ, …}
```

### [ ⏭ Next: Numbers in JS](./09_numbers.md)

### [🔙 Back To JS Readme](./js.md)

### [🔙 Back To Main Readme](../../../README.md)

🙏 Please credit me if you use this or share it with others. 🙏

