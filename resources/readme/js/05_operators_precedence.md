# Welcome 🙋‍♂️ to JS Operator Precedence 🏆

🙏 Please credit me if you use this or share it with others. 🙏

### [🔙 Back To JS Readme](./js.md)

### [🔙 Back To Main Readme](../../../README.md)

## Operator Precedence

Operator precedence is a rule that defines the order in which operators are evaluated when an expression is executed. Operators with higher precedence are evaluated first.

Also the associativity of an operator is the order in which the operator is evaluated when there are multiple operators of the same precedence. The associativity of an operator is either left-to-right or right-to-left.

To check the precedence of an operator, you can refer to the [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Operator_precedence#table).

```javascript
// * and / have higher precedence than + and - so they are evaluated first
// they are evaluated from left to right means 3 * 4 is evaluated first then 12 * 6 is evaluated
// finally 2 + 72 is evaluated
let result = 2 + 3 * 4 * 6; // 74
```

### [ ⏭ Next: Conversion & Coercion](./06_convertion_coercion.md)

### [🔙 Back To JS Readme](./js.md)

### [🔙 Back To Main Readme](../../../README.md)

🙏 Please credit me if you use this or share it with others. 🙏
