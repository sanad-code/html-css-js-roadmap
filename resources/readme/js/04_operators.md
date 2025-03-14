# Welcome 🙋‍♂️ to JS Operators 🏆

🙏 Please credit me if you use this or share it with others. 🙏

### [🔙 Back To JS Readme](./js.md)

### [🔙 Back To Main Readme](../../../README.md)

## Operators

Operators are used to perform operations on variables and values. JavaScript has the following types of operators:

- Arithmetic operators
- Assignment operators
- Comparison operators
- Logical operators
- Bitwise operators
- String operators
- Conditional (ternary) operator
- Relational operators
- Spread operator
- Comma operator
- Unary operators


### Arithmetic Operators

Arithmetic operators are used to perform arithmetic operations on numbers.

**In mathematics  1 + 2 = 3, the 1 and 2 are called operands and + is called operator.**

| Operator | Description | Example | Result | Notes |
| --- | --- | --- | --- | --- |
| `+` | Addition | `10 + 5` | `15` | |
| `-` | Subtraction | `10 - 5` | `5` | |
| `*` | Multiplication | `10 * 5` | `50` | |
| `/` | Division | `10 / 5` | `2` | |
| `/` | Division | `10 / 3` | `3.3333333333333335` | |
| `%` | Modulus (Remainder) | `10 % 3` | `1` | |
| `%` | Modulus (Remainder) | `10.1 % 3` | `1.1` | Note this is remainder and can be float |
| `%` | Modulus (Remainder) | `-10 % 3` | `-1` | Note it give negative number  |
| `**` | Exponentiation | `2 ** 3` | `8` | `2 * 2 * 2` |
| `++` | Increment | `let x = 10; console.log(x++);` | `10` | x++ returns the value of x before incrementing this is called post-increment |
| `++` | Increment | `let x = 10; let y = 5; let z = x++ + y; console.log(z); console.log(x);` | `15` `11` | x++ returns the value of x before incrementing this is called post-increment | 
| `++` | Increment | `let x = 10; console.log(++x);` | `11` | ++x returns the value of x after incrementing this is called pre-increment |
| `--` | Decrement | `let x = 10; console.log(x--);` | `10` | x-- returns the value of x before decrementing this is called post-decrement |
| `--` | Decrement | `let x = 10; console.log(--x);` | `9` | --x returns the value of x after decrementing this is called pre-decrement |
| `-` | Unary Negation | `let x = 10; console.log(-x);` | `-10` | Unary means **only one operand** |
| `+` | Unary Plus | `let x = 10; console.log(+x);` | `10` | Unary means **only one operand** |

### Assignment Operators

Assignment operators are used to assign values to variables.

| Operator | Example | Same As |
| --- | --- | --- |
| `=` | `x = 10` | `x = 10` |
| `+=` | `x += 5` | `x = x + 5` |
| `-=` | `x -= 5` | `x = x - 5` |
| `*=` | `x *= 5` | `x = x * 5` |
| `/=` | `x /= 5` | `x = x / 5` |
| `%=` | `x %= 5` | `x = x % 5` |
| `**=` | `x **= 5` | `x = x ** 5` |

### Comparison Operators

Comparison operators are used to compare two values. Values must be of the same type to avoid coercion (we will talk later about coercion). The result of a comparison is a boolean value.

| Operator | Description | Example | Result | Notes |
| --- | --- | --- | --- | --- |
| `==` | Equal | `10 == 5` | `false` | Equal use double == , assignment use only one |
| `!=` | Not Equal | `10 != 5` | `true` | |
| `===` | Strict Equal | `10 === 5` | `false` | Strict Equal use triple ===, this will tell js engine to not to do coercion, which simply means type of data matter, it is recommeded to use === equality over == equality |
| `!==` | Strict Not Equal | `10 !== 5` | `true` | |
| `>` | Greater Than | `10 > 5` | `true` | |
| `<` | Less Than | `10 < 5` | `false` | |
| `>=` | Greater Than or Equal | `10 >= 5` | `true` | |
| `<=` | Less Than or Equal | `10 <= 5` | `false` | |
| `??` | Nullish Coalescing | `let x = null; let y = x ?? 5; console.log(y);` | `5` | Nullish Coalescing operator (??) is a logical operator that returns its right-hand side operand when its left-hand side operand is null or undefined, and otherwise returns its left-hand side operand. |

### Logical Operators

Logical operators are used to determine the logic between variables or values.

| Operator | Description | Example | Result | Notes |
| --- | --- | --- | --- | --- |
| `&&` | Logical AND | `true && true` | `true` | Both operands must be true to give true or otherwise it will be false |
| `||` | Logical OR | `true || false` | `true` | Both operands must be false to give false or otherwise it will be true |
| `!` | Logical NOT | `!true` | `false` | Logical NOT operator is used to reverse the logical state of its operand. If a condition is true, the Logical NOT operator makes it false. |
| `&&` | Short-circuiting | `let x = 10; let y = 5; let z = x > 5 && y > 5; console.log(z);` | `false` | Short-circuiting means that if the first operand is false, the second operand will not be evaluated. It is used as a performance optimization and as guard operator. |
| `||` | Short-circuiting | `let x = 10; let y = 5; let z = x > 5 || y > 5; console.log(z);` | `true` | Short-circuiting means that if the first operand is true, the second operand will not be evaluated. It is used as a performance optimization and as guard operator. |

### Bitwise Operators

Bitwise operators are used to perform bitwise operations on numbers. Bitwise operators treat their operands as a sequence of bits (zeros and ones), rather than as decimal, hexadecimal, or octal numbers. For example, the decimal number nine has a binary representation of 1001. Bitwise operators perform their operations on such binary representations, but they return standard JavaScript numerical values. The operands of all bitwise operators are converted to signed 32-bit integers in two's complement format. Bitwise operators perform the following operations:

| Operator | Description | Example | Result | Notes |
| --- | --- | --- | --- | --- |
| `&` | AND | `5 & 1` | `1` |  5 in binary is 101, 1 in binary is 001, 101 & 001 = 001 which is 1, we perform the && operation on each bit |
| `|` | OR | `5 | 1` | `5` | 5 in binary is 101, 1 in binary is 001, 101 | 001 = 101 which is 5, we perform the || operation on each bit |
| `^` | XOR | `5 ^ 1` | `4` | 5 in binary is 101, 1 in binary is 001, 101 ^ 001 = 100 which is 4, we perform the XOR operation on each bit, XOR means exclusive OR which means if both bits are same it will be 0 otherwise 1 |
| `~` | NOT | `~5` | `-6` | 5 in binary is 101, ~5 = -6, we perform the NOT operation on each bit |
| `<<` | Left Shift | `5 << 1` | `10` | 5 in binary is 101, 5 << 1 = 1010 which is 10, we shift the bits to the left by 1, **You can observe that the number is doubled, multplied by 2** |
| `>>` | Right Shift | `5 >> 1` | `2` | 5 in binary is 101, 5 >> 1 = 10 which is 2, we shift the bits to the right by 1, **You can observe that the number is halved, divided by 2** |
| `>>>` | Zero-fill Right Shift | `5 >>> 1` | `2` | 5 in binary is 101, 5 >>> 1 = 10 which is 2, we shift the bits to the right by 1, **You can observe that the number is halved, divided by 2** |
| `&=` | AND Assignment | `let x = 5; x &= 1; console.log(x);` | `1` | 5 in binary is 101, 1 in binary is 001, 101 & 001 = 001 which is 1, we perform the && operation on each bit and assign the result to x |
| `|=` | OR Assignment | `let x = 5; x |= 1; console.log(x);` | `5` | 5 in binary is 101, 1 in binary is 001, 101 | 001 = 101 which is 5, we perform the || operation on each bit and assign the result to x |
| `^=` | XOR Assignment | `let x = 5; x ^= 1; console.log(x);` | `4` | 5 in binary is 101, 1 in binary is 001, 101 ^ 001 = 100 which is 4, we perform the XOR operation on each bit and assign the result to x |
| `<<=` | Left Shift Assignment | `let x = 5; x <<= 1; console.log(x);` | `10` | 5 in binary is 101, 5 << 1 = 1010 which is 10, we shift the bits to the left by 1 and assign the result to x |
| `>>=` | Right Shift Assignment | `let x = 5; x >>= 1; console.log(x);` | `2` | 5 in binary is 101, 5 >> 1 = 10 which is 2, we shift the bits to the right by 1 and assign the result to x |
| `>>>=` | Zero-fill Right Shift Assignment | `let x = 5; x >>>= 1; console.log(x);` | `2` | 5 in binary is 101, 5 >>> 1 = 10 which is 2, we shift the bits to the right by 1 and assign the result to x |

### String Operators

String operators are used to concatenate strings.

| Operator | Description | Example | Result | Notes |
| --- | --- | --- | --- | --- |
| `+` | Concatenation | `'Hello, ' + 'World!'` | `'Hello, World!'` | |
| `+=` | Concatenation Assignment | `let x = 'Hello, '; x += 'World!'; console.log(x);` | `'Hello, World!'` | |

**It is better to avoid using the `+` operator to concatenate strings, instead use template literals.** 

```javascript
let firstName = "Moataz",
  lastName = "Sanad";
console.log(`Hello, ${firstName} ${lastName}`);
```

### Conditional (Ternary) Operator

The conditional operator assigns a value to a variable based on a condition. It is the only JavaScript operator that takes three operands. The operator can have one of two values based on a condition.

It is a shorthand for the `if` statement. But it has an advantage over the `if` statement, it can be **used inside expressions**.

```javascript
let age = 25;
let canDrink = age >= 21 ? "Yes" : "No";
console.log(canDrink); // Yes
```

### Relational Operators

Relational operators are used to determine the relationship between two variables or values.

| Operator | Description | Example | Result | Notes |
| --- | --- | --- | --- | --- |
| `in` | Property in Object | `'x' in {x: 10}` | `true` | The in operator returns true if the specified property is in the specified object. |
| `instanceof` | Instance of Object | `[] instanceof Array` | `true` | The instanceof operator returns true if the specified object is an instance of the specified object. |
| `instanceof` | Instance of Object | `[] instanceof Object` | `true` | The instanceof operator returns true if the specified object is an instance of the specified object. |
| `instanceof` | Instance of Object | `[] instanceof Function` | `false` | The instanceof operator returns true if the specified object is an instance of the specified object. |

### Spread Operator

The spread operator is used to expand an array or object into individual elements.

```javascript
let arr = [1, 2, 3];
let arr2 = [...arr, 4, 5, 6];
console.log(arr2); // [1, 2, 3, 4, 5, 6]
```

### Comma Operator

The comma operator evaluates each of its operands (from left to right) and returns the value of the last operand.

```javascript
let x = 1;
let y = 20;
x = (x++, 11 , y);
console.log(x); // 20 as the last operand is y
```

### Unary Operators

Unary operators are used to perform operations on a single operand.

| Operator | Description | Example | Result | Notes |
| --- | --- | --- | --- | --- |
| `+` | Unary Plus | `let x = 10; console.log(+x);` | `10` | Unary means **only one operand** |
| `-` | Unary Negation | `let x = 10; console.log(-x);` | `-10` | Unary means **only one operand** |
| `++` | Increment | `let x = 10; console.log(x++);` | `10` | x++ returns the value of x before incrementing this is called post-increment |
| `++` | Increment | `let x = 10; console.log(++x);` | `11` | ++x returns the value of x after incrementing this is called pre-increment |
| `--` | Decrement | `let x = 10; console.log(x--);` | `10` | x-- returns the value of x before decrementing this is called post-decrement |
| `--` | Decrement | `let x = 10; console.log(--x);` | `9` | --x returns the value of x after decrementing this is called pre-decrement |
| `!` | Logical NOT | `!true` | `false` | Logical NOT operator is used to reverse the logical state of its operand. If a condition is true, the Logical NOT operator makes it false. |
| `typeof` | Typeof | `typeof 10` | `number` | The typeof operator returns the type of a variable, object, function, or expression. |
| `void` | Void | `void(0)` | `undefined` | The void operator evaluates the given expression and then returns undefined. |

```javascript
let x = 1;
let y = void(x++);
console.log(x,y) // 2, undefined
```

### [ ⏭ Next: Operator Precedence](./05_operators_precedence.md)

### [🔙 Back To JS Readme](./js.md)

### [🔙 Back To Main Readme](../../../README.md)

🙏 Please credit me if you use this or share it with others. 🙏
