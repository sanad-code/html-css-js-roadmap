# Welcome 🙋‍♂️ to JS Loops 🏆

🙏 Please credit me if you use this or share it with others. 🙏

### [🔙 Back To JS Readme](./js.md)

### [🔙 Back To Main Readme](../../../README.md)

## Loops in JavaScript

Loops are used to execute the same block of code a specified number of times or while a specified condition is true.

### for Loop

Use the `for` loop to execute a block of code a specified number of times.

```javascript
for (let i = 0; i < 5; i++) {
  console.log(i);
}
```

Notes:

- The `for` loop has three parts: initialization, condition, and increment/decrement.
- The initialization part is executed once at the beginning.
- The condition is evaluated before each iteration. If it is `true`, the loop continues. If it is `false`, the loop stops.
- The increment/decrement part is executed after each iteration.
- You can omit any of the three parts.
- You can have multiple statements in each part.
- You can have multiple conditions in the condition part.
- You can use the `break` statement to exit the loop.
- You can use the `continue` statement to skip the current iteration.
- You can nest loops inside loops.
- You can use the `for...in` loop to iterate over the properties of an object. You can also use it to get index values of an array.
- You can use the `for...of` loop to iterate over the values of an iterable object, strings and maps.


```javascript
//ommiting the initialization part
let i = 0;
for (; i < 5; i++) {
  console.log(i);
}

//ommiting the condition part
for (let i = 0; ; i++) {
  if (i >= 5) {
    break;
  }
  console.log(i);
}

//ommiting the increment part
for (let i = 0; i < 5;) {
  console.log(i);
  i++;
}

//ommiting all parts
for(;;) {
  console.log('infinite loop');
  break;
}

//multiple statements in each part
for (let i = 0, j = 5; i < 5; i++, j--) {
  console.log(i, j);
}

//multiple conditions in the condition part
for (let i = 0, j = 5; i < 5 && j > 0; i++, j--) {
  console.log(i, j);
}

//break statement
for (let i = 0; i < 5; i++) {
  if (i === 3) {
    break;
  }
  console.log(i);
}

//continue statement
for (let i = 0; i < 5; i++) {
  if (i === 3) {
    continue;
  }
  console.log(i);
}

//nested loops
for (let i = 0; i < 3; i++) {
  for (let j = 0; j < 3; j++) {
    console.log(i, j);
  }
}

//for...in loop
let obj = { a: 1, b: 2, c: 3 };
for (let key in obj) {
  console.log(key, obj[key]);
}

let arr = [1, 2, 3];
for (let index in arr) {
  console.log(index, arr[index]);
}

//for...of loop
let arr = [1, 2, 3];
for (let value of arr) {
  console.log(value);
}

let obj = { a: 1, b: 2, c: 3 };
for (let value of Object.values(obj)) {
  console.log(value);
}

let str = 'hello';
for (let char of str) {
  console.log(char);
}

let map = new Map([['a', 1], ['b', 2], ['c', 3]]);
for (let [key, value] of map) {
  console.log(key, value);
}
```

### while Loop

Use the `while` loop to execute a block of code while a specified condition is true. Use it when you do not know the number of iterations in advance.

```javascript
let i = 0;
while (i < 5) {
  console.log(i);
  i++;
}
```

Notes:
    - The condition is evaluated before each iteration. If it is `true`, the loop continues. If it is `false`, the loop stops.
    - You can use the `break` statement to exit the loop.
    - You can use the `continue` statement to skip the current iteration.
    - repeat the loop as long as a specified condition is true.
    - You can nest loops inside loops.
    - You can use the `while...true` loop to create an infinite loop.
    - You can use the `while...false` loop to create a loop that never executes.
    - You can use the `while...break` loop to create a loop that breaks immediately.
    - You can use the `while...continue` loop to create a loop that skips the current iteration.
    - You can use the `while...for...in` loop to iterate over the properties of an object.
    - You can use the `while...for...of` loop to iterate over the values of an iterable object.

```javascript
//break statement
let i = 0;
while (i < 5) {
  if (i === 3) {
    break;
  }
  console.log(i);
  i++;
}

//continue statement
let i = 0;
while (i < 5) {
  if (i === 3) {
    i++;
    continue;
  }
  console.log(i);
  i++;
}


//nested loops
let i = 0;
while (i < 3) {
  let j = 0;
  while (j < 3) {
    console.log(i, j);
    j++;
  }
  i++;
}

//infinite loop
while (true) {
  console.log('infinite loop');
  break;
}

//loop that never executes
while (false) {
  console.log('loop that never executes');
}

//loop that breaks immediately
while (true) {
  break;
}

//loop that skips the current iteration
let i = 0;
while (i < 5) {
  i++;
  continue;
  console.log(i);
}

//nested loop
let i = 0;
while (i < 3) {
  let j = 0;
  while (j < 3) {
    console.log(i, j);
    j++;
  }
  i++;
}

//for...in loop
let obj = { a: 1, b: 2, c: 3 };
let key;
while (key in obj) {
  console.log(key, obj[key]);
}

//for...of loop
let arr = [1, 2, 3];
let value;
while (value of arr) {
  console.log(value);
}
```

### do...while Loop

Use the `do...while` loop to execute a block of code at least once, and then repeat the loop as long as a specified condition is true.

```javascript
let i = 0;
do {
  console.log(i);
  i++;
} while (i < 5);
```

### Loop Control Statements

Use loop control statements to control the flow of loops.

- The `break` statement exits the loop.
- The `continue` statement skips the current iteration and continues with the next iteration.

### Foreach Method

Use the `forEach` method to execute a function once for each element in an array.

```javascript
let arr = [1, 2, 3];
arr.forEach(function(value, index, array) {
  console.log(value, index, array);
});
```


### [ ⏭ Next: Asynchronus JS](./18_asynchronous.md)

### [🔙 Back To JS Readme](./js.md)

### [🔙 Back To Main Readme](../../../README.md)

🙏 Please credit me if you use this or share it with others. 🙏