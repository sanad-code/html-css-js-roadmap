# Welcome 🙋‍♂️ to JS Destructuring 🏆

🙏 Please credit me if you use this or share it with others. 🙏

### [🔙 Back To JS Readme](./js.md)

### [🔙 Back To Main Readme](../../../README.md)

## Destructuring in JavaScript

Destructuring is a JavaScript expression that makes it possible to unpack values from arrays, or properties from objects, into distinct variables.

### Array Destructuring

```javascript
let [a, b] = [1, 2];
console.log(a); // 1
console.log(b); // 2
```

### Object Destructuring

```javascript
let {name, age} = {name: "John", age: 30};
console.log(name); // John
```

### Nested Destructuring

```javascript
let {name, age, address: {city}} = {name: "John", age: 30, address: {city: "New York"}};
console.log(city); // New York
```

### Swapping Variables

```javascript
let a = 1;
let b = 2;
[a, b] = [b, a];
console.log(a); // 2
console.log(b); // 1
```

### Ignoring Values

```javascript
let [a, , b] = [1, 2, 3];
console.log(a); // 1
console.log(b); // 3
```

### Default Values

You can provide default values for variables that are not found in the array or object.

```javascript
let [a, b, c = 3] = [1, 2];
console.log(c); // 3
```

### Rest Syntax

The rest syntax `...` allows you to collect the remaining elements of an array or object into a new array or object.

```javascript
let [a, ...b] = [1, 2, 3, 4];
console.log(b); // [2, 3, 4]

let {name, ...rest} = {name: "John", age: 30, city: "New York"};
console.log(rest); // {age: 30, city: "New York"}
```

### Spread Syntax

The spread syntax `...` allows you to spread the elements of an array or object into another array or object.

```javascript
let arr1 = [1, 2];
let arr2 = [3, 4];
let arr3 = [...arr1, ...arr2];
console.log(arr3); // [1, 2, 3, 4]

let obj1 = {name: "John"};
let obj2 = {age: 30};
let obj3 = {...obj1, ...obj2};

console.log(obj3); // {name: "John", age: 30}

//If there are nested references, the spread operator only copies the reference, not the value.
let obj4 = {name: "John", address: {city: "New York"}};
let obj5 = {...obj4};
obj5.address.city = "Los Angeles";
console.log(obj4.address.city); // Los Angeles

//To create a deep copy, you can use JSON.parse(JSON.stringify(obj))
let obj6 = JSON.parse(JSON.stringify(obj4));
obj6.address.city = "Chicago";
console.log(obj4.address.city); // Los Angeles
```

### [ ⏭ Next: Functions](./14_functions.md)

### [🔙 Back To JS Readme](./js.md)

### [🔙 Back To Main Readme](../../../README.md)

🙏 Please credit me if you use this or share it with others. 🙏
