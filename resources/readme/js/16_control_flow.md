# Welcome 🙋‍♂️ to JS Logic Control 🏆

🙏 Please credit me if you use this or share it with others. 🙏

### [🔙 Back To JS Readme](./js.md)

### [🔙 Back To Main Readme](../../../README.md)

## JS Logic Control

### Conditional Statements

Conditional statements are used to perform different actions based on different conditions.

#### if Statement

Use the `if` statement to specify a block of JavaScript code to be executed if a condition is true.

```javascript
if (condition) {
  // block of code to be executed if the condition is true
} else if (anotherCondition) {
  // block of code to be executed if the condition is false and the anotherCondition is true
} else {
  // block of code to be executed if the condition is false
}
```

Notes:

- The condition is evaluated to `true` or `false`.
- The `else if` statement specifies a new condition if the first condition is false.
- The `else` statement specifies the code to run if the condition is false.
- You can have as many `else if` statements as you want.
- You can have only one `else` statement.
- You can omit the `else` statement if you do not need it.
- You can omit the `else if` statement if you do not need it.
- You can use && (AND), || (OR), and ! (NOT) operators to combine multiple conditions.
- You can nest `if` statements inside `if` statements.

```javascript
let age = 20;
let isCitizen = true;
let canVote = false;

if (age >= 18 && isCitizen) {
  if (canVote) {
    console.log('You are old enough to vote.');
  } else {
    console.log('You are old enough to vote, but you cannot vote.');
  }
}else {
  console.log('You are not old enough to vote.');
}
```

#### short-hand if

If the code is only one line, you can write it in one line using the short-hand if statement.

```javascript
if (condition) 
  console.log('This is a short-hand if statement');
```

#### ternary Operator

The ternary operator is the only JavaScript operator that takes three operands. This operator is frequently used as a shortcut for the `if` statement.

```javascript
let result = (condition) ? value1 : value2;
```

Notes:
- If the condition is true, the operator returns the value of `value1`; otherwise, it returns the value of `value2`.
- You can use the ternary operator as a short-hand if statement.
- You can use multiple ternary operators in one statement.
- You can use the ternary operator inside the template literals.

```javascript
let age = 20;
let message = `You are ${age >= 18 ? 'old enough' : 'not old enough'} to vote.`;
console.log(message); // You are old enough to vote.
```




#### switch Statement

Use the `switch` statement to select one of many code blocks to be executed.

```javascript
switch (expression) {
  case x:
    // code block
    break;
  case y:
    // code block
    break;
  default:
    // code block
}
```

Notes:

- The `break` keyword breaks out of the switch block.
- The `default` keyword specifies the code to run if there is no case match.
- If you omit the `break` keyword, the next case will be executed even if the evaluation does not match the case.

### [ ⏭ Next: Loops](./17_loops.md)

### [🔙 Back To JS Readme](./js.md)

### [🔙 Back To Main Readme](../../../README.md)

🙏 Please credit me if you use this or share it with others. 🙏
