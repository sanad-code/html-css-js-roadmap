# Welcome 🙋‍♂️ to JS Objects 🏆

🙏 Please credit me if you use this or share it with others. 🙏

### [🔙 Back To JS Readme](./js.md)

### [🔙 Back To Main Readme](../../../README.md)

## Objects in JavaScript

Objects are used to store collections of data and more complex entities. An object is a collection of properties, and a property is an association between a name (or key) and a value. A property's value can be a function, in which case the property is known as a method.

### Creating Objects

There are two ways to create objects in JavaScript:

1. Using the object literal syntax `{}`.
2. Using the `new Object()` syntax.

```javascript
// Using object literal syntax
let person = {
  name: "John",
  age: 30,
  city: "New York"
};

// Using new Object() syntax
let person = new Object();
person.name = "John";
person.age = 30;
person.city = "New York";
```

### Accessing Object Properties

You can access object properties using dot notation or bracket notation.

Bracket notation is useful when the property name is dynamic or when it contains special characters.

```javascript
let person = {
  name: "John",
  age: 30,
  city: "New York"
};

console.log(person.name); // John

console.log(person["name"]); // John
```

### Adding and Modifying Properties

You can add new properties to an object or modify existing properties using dot notation or bracket notation.

```javascript
let person = {
  name: "John",
  age: 30,
  city: "New York"
};

person.name = "Jane";
person["age"] = 25;
```

### Deleting Properties

You can delete properties from an object using the `delete` operator.

```javascript
let person = {
  name: "John",
  age: 30,
  city: "New York"
};

delete person.age;
```

### Object Methods

Objects can also contain methods. Methods are functions that are stored as object properties.

```javascript
let person = {
  name: "John",
  age: 30,
  city: "New York",
  greet: function() {
    console.log("Hello, my name is " + this.name);
  }
};

// Review the this scope readme for more information on the this keyword
person.greet(); // Hello, my name is John
```

### Object Constructors

You can create objects using constructor functions. Constructor functions are used to create multiple instances of an object.

```javascript
function Person(name, age, city) {
  this.name = name;
  this.age = age;
  this.city = city;
}

let person1 = new Person("John", 30, "New York");
let person2 = new Person("Jane", 25, "Los Angeles");
```

### Object Prototypes

JavaScript objects have a prototype. The prototype is also an object. All JavaScript objects inherit their properties and methods from their prototype.

```javascript
function Person(name, age, city) {
  this.name = name;
  this.age = age;
  this.city = city;
}

// This is better than adding the greet method to each instance of the Person object
Person.prototype.greet = function() {
  console.log("Hello, my name is " + this.name);
};

let person1 = new Person("John", 30, "New York");
let person2 = new Person("Jane", 25, "Los Angeles");
person1.greet(); // Hello, my name is John
person2.greet(); // Hello, my name is Jane
```

#### Concatenating Objects

You can concatenate objects using the `Object.assign()` method or the spread operator (`...`).

The created object is shallow-copied, meaning that nested objects are not copied.

```javascript
let obj1 = { a: 1, b: 2 };
let obj2 = { b: 3, c: 4 };
let obj3 = Object.assign(obj1, obj2);

console.log(obj3); // { a: 1, b: 3, c: 4 }

let obj4 = { ...obj1, ...obj2 };
```

#### Accessing Nested Objects

You can access nested objects using dot notation or bracket notation.

```javascript
let person = {
  name: "John",
  age: 30,
  address: {
    street: "123 Main St",
    city: "New York"
  }
};

console.log(person.address.street); // 123 Main St
console.log(person["address"]["city"]); // New York
```

#### Accessing keys and values

You can access the keys and values of an object using the `Object.keys()` and `Object.values()` methods.

You can access the entries of an object using the `Object.entries()` method.

```javascript
let person = {
  name: "John",
  age: 30,
  city: "New York"
};

console.log(Object.keys(person)); // ["name", "age", "city"]
console.log(Object.values(person)); // ["John", 30, "New York"]
console.log(Object.entries(person)); // [["name", "John"], ["age", 30], ["city", "New York"]]

for (let key in person) {
  console.log(key, person[key]); // name John, age 30, city New York
}

// Error: person is not iterable
// for (let key of person) {
//   console.log(key);
// }

for (let [key, value] of Object.entries(person)) {
  console.log(key, value);
}

for (let key of Object.keys(person)) {
  console.log(key, person[key]); // name John, age 30, city New York
}

```

#### length of an object

You can get the length of an object using the `Object.keys().length` method.

We can't use the `length` property directly on an object because it is not an array.

```javascript
let person = {
  name: "John",
  age: 30,
  city: "New York"
};

console.log(Object.keys(person).length); // 3
```

#### HasOwnProperty

You can check if an object has a specific property using the `hasOwnProperty()` method. The method returns `true` if the object has the property, otherwise it returns `false`.

If the property is inherited from the prototype chain, the method returns `false`.

To check if the property is in object or prototype chain, use the `in` operator.

```javascript
let person = {
  name: "John",
  age: 30,
  city: "New York"
};

console.log(person.hasOwnProperty("name")); // true

console.log("name" in person); // true
```

### [ ⏭ Next: Destructuring ](./13_destructuring.md)

### [🔙 Back To JS Readme](./js.md)

### [🔙 Back To Main Readme](../../../README.md)

🙏 Please credit me if you use this or share it with others. 🙏

