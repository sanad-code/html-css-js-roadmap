# Welcome 🙋‍♂️ to JS Arrays 🏆

🙏 Please credit me if you use this or share it with others. 🙏

### [🔙 Back To JS Readme](./js.md)

### [🔙 Back To Main Readme](../../../README.md)

## Arrays in JavaScript

Arrays are a special type of object that holds a list of values. You can store any type of value in an array, and you can store different types of values in the same array.

### Creating Arrays

You can create an array by enclosing a list of values in square brackets `[]`, separated by commas.

```javascript
let fruits = ['Apple', 'Banana', 'Cherry'];
let mix = [1, 'two', true, null];
```

### Accessing Array Elements

You can access an element in an array using its index. The index of the first element is `0`, the index of the second element is `1`, and so on.

```javascript
let fruits = ['Apple', 'Banana', 'Cherry'];
console.log(fruits[0]); // Apple
console.log(fruits[1]); // Banana
console.log(fruits[2]); // Cherry
```

### Modifying Array Elements

You can modify an element in an array by assigning a new value to the element using its index.

```javascript
let fruits = ['Apple', 'Banana', 'Cherry'];
fruits[1] = 'Orange';
console.log(fruits); // ['Apple', 'Orange', 'Cherry']
```

### Array Methods

JavaScript provides a number of methods for working with arrays. Here are some of the most commonly used methods:

#### `push()`

The `push()` method adds one or more elements to the end of an array and returns the new length of the array.

```javascript
let fruits = ['Apple', 'Banana', 'Cherry'];
fruits.push('Orange');
console.log(fruits); // ['Apple', 'Banana', 'Cherry', 'Orange']

fruits.push('Grapes', 'Kiwi');
console.log(fruits); // ['Apple', 'Banana', 'Cherry', 'Orange', 'Grapes', 'Kiwi']
```

#### `pop()`

The `pop()` method removes the last element from an array and returns that element.

```javascript
let fruits = ['Apple', 'Banana', 'Cherry'];
let lastFruit = fruits.pop();
console.log(lastFruit); // Cherry
console.log(fruits); // ['Apple', 'Banana']
```

#### `shift()`

The `shift()` method removes the first element from an array and returns that element.

```javascript
let fruits = ['Apple', 'Banana', 'Cherry'];
let firstFruit = fruits.shift();
console.log(firstFruit); // Apple
console.log(fruits); // ['Banana', 'Cherry']
```

#### `unshift()`

The `unshift()` method adds one or more elements to the beginning of an array and returns the new length of the array.

```javascript
let fruits = ['Apple', 'Banana', 'Cherry'];
fruits.unshift('Orange');
console.log(fruits); // ['Orange', 'Apple', 'Banana', 'Cherry']

fruits.unshift('Grapes', 'Kiwi');
console.log(fruits); // ['Grapes', 'Kiwi', 'Orange', 'Apple', 'Banana', 'Cherry']
```

#### `concat()`

The `concat()` method is used to merge two or more arrays. This method does not change the existing arrays, but instead returns a new array.

```javascript
let fruits1 = ['Apple', 'Banana', 'Cherry'];
let fruits2 = ['Orange', 'Grapes', 'Kiwi'];
let allFruits = fruits1.concat(fruits2);
console.log(allFruits); // ['Apple', 'Banana', 'Cherry', 'Orange', 'Grapes', 'Kiwi']

// We can use the spread operator to merge arrays
let allFruits2 = [...fruits1, ...fruits2];
console.log(allFruits2); // ['Apple', 'Banana', 'Cherry', 'Orange', 'Grapes', 'Kiwi']
```

#### `slice()`

The `slice()` method returns a shallow copy of a portion of an array into a new array object selected from `begin` to `end` (`end` not included). The original array will not be modified.

Shallow copy means that the elements of the new array are references to the elements of the original array. If the elements of the original array are objects, the elements of the new array will reference the same objects.

```javascript
let fruits = ['Apple', 'Banana', 'Cherry', 'Orange', 'Grapes', 'Kiwi'];
let selectedFruits = fruits.slice(1, 4);
console.log(selectedFruits); // ['Banana', 'Cherry', 'Orange']
console.log(fruits); // ['Apple', 'Banana', 'Cherry', 'Orange', 'Grapes', 'Kiwi']
```

#### `splice()`

The `splice()` method changes the contents of an array by removing or replacing existing elements and/or adding new elements in place.

```javascript
let fruits = ['Apple', 'Banana', 'Cherry', 'Orange', 'Grapes', 'Kiwi'];
let removedFruits = fruits.splice(2, 2, 'Mango', 'Pineapple'); // Remove 2 elements starting from index 2 and add 'Mango' and 'Pineapple'
console.log(removedFruits); // ['Cherry', 'Orange']
console.log(fruits); // ['Apple', 'Banana', 'Mango', 'Pineapple', 'Grapes', 'Kiwi']

let fruits2 = ['Apple', 'Banana', 'Cherry', 'Orange', 'Grapes', 'Kiwi'];
let addedFruits = fruits2.splice(2, 0, 'Mango', 'Pineapple'); // Add 'Mango' and 'Pineapple' starting from index 2
console.log(addedFruits); // []
console.log(fruits2); // ['Apple', 'Banana', 'Mango', 'Pineapple', 'Cherry', 'Orange', 'Grapes', 'Kiwi']

let fruits3 = ['Apple', 'Banana', 'Cherry', 'Orange', 'Grapes', 'Kiwi'];
let removedAndAddedFruits = fruits3.splice(2, 3, 'Mango', 'Pineapple'); // Remove 3 elements starting from index 2 and add 'Mango' and 'Pineapple'
console.log(removedAndAddedFruits); // ['Cherry', 'Orange', 'Grapes']
```

#### `reverse()`

The `reverse()` method reverses the elements of an array in place.

```javascript
let fruits = ['Apple', 'Banana', 'Cherry', 'Orange', 'Grapes', 'Kiwi'];
fruits.reverse();
console.log(fruits); // ['Kiwi', 'Grapes', 'Orange', 'Cherry', 'Banana', 'Apple']

// We can reverse strings as well
let str = 'Hello, World!';
let reversedStr = str.split('').reverse().join('');
```

#### `sort()`

The `sort()` method sorts the elements of an array in place and returns the sorted array. The default sort order is ascending.

The idea of sorting is to compare two elements and determine their relative positions. The `sort()` method uses the `compareFunction` to compare two elements. The `compareFunction` should return a negative value if the first element should come before the second element, a positive value if the first element should come after the second element, and zero if the two elements are equal.

Swapping the elements is done by comparing the elements and swapping them if the first element should come after the second element.

```javascript
let fruits = ['Apple', 'Banana', 'Cherry', 'Orange', 'Grapes', 'Kiwi'];
fruits.sort();
console.log(fruits); // ['Apple', 'Banana', 'Cherry', 'Grapes', 'Kiwi', 'Orange']

// To sort numbers in ascending order
let numbers = [3, 1, 4, 1, 5, 9, 2, 6, 5, 3, 5];
numbers.sort((a, b) => a - b);
console.log(numbers); // [1, 1, 2, 3, 3, 4, 5, 5, 5, 6, 9]

// To sort numbers in descending order
numbers.sort((a, b) => b - a);
console.log(numbers); // [9, 6, 5, 5, 5, 4, 3, 3, 2, 1, 1]
```

#### `indexOf()` , `lastIndexOf()`

The `indexOf()` method returns the first index at which a given element can be found in the array, or `-1` if it is not present.

The `lastIndexOf()` method returns the last index at which a given element can be found in the array, or `-1` if it is not present.

```javascript
let fruits = ['Apple', 'Banana', 'Cherry', 'Orange', 'Grapes', 'Kiwi'];
console.log(fruits.indexOf('Cherry')); // 2
console.log(fruits.indexOf('Mango')); // -1

console.log(fruits.lastIndexOf('Banana')); // 1
```

#### `includes()`

The `includes()` method determines whether an array includes a certain element, returning `true` or `false` as appropriate.

```javascript
let fruits = ['Apple', 'Banana', 'Cherry', 'Orange', 'Grapes', 'Kiwi'];
console.log(fruits.includes('Cherry')); // true
console.log(fruits.includes('Mango')); // false
```

#### `find()`, `findIndex()`

The `find()` method returns the first element in an array that satisfies a provided testing function. Otherwise, it returns `undefined`.

The `findIndex()` method returns the index of the first element in an array that satisfies a provided testing function. Otherwise, it returns `-1`.

```javascript
let numbers = [3, 1, 4, 1, 5, 9, 2, 6, 5, 3, 5];
let evenNumber = numbers.find(num => num % 2 === 0);
console.log(evenNumber); // 4

let evenNumberIndex = numbers.findIndex(num => num % 2 === 0);
console.log(evenNumberIndex); // 2
```

#### `filter()`

The `filter()` method creates a new array with all elements that pass the test implemented by the provided function.

```javascript
let numbers = [3, 1, 4, 1, 5, 9, 2, 6, 5, 3, 5];
let evenNumbers = numbers.filter(num => num % 2 === 0);
console.log(evenNumbers); // [4, 2, 6]
```

#### `map()`

The `map()` method creates a new array populated with the results of calling a provided function on every element in the calling array.

```javascript
let numbers = [3, 1, 4, 1, 5, 9, 2, 6, 5, 3, 5];
let squaredNumbers = numbers.map(num => num ** 2);
console.log(squaredNumbers); // [9, 1, 16, 1, 25, 81, 4, 36, 25, 9, 25]
```

#### `reduce()`

The `reduce()` method applies a function against an accumulator and each element in the array (from left to right) to reduce it to a single value.

```javascript
let numbers = [3, 1, 4, 1, 5, 9, 2, 6, 5, 3, 5];
let sum = numbers.reduce((acc, num) => acc + num, 0);
console.log(sum); // 44
```

#### `forEach()`

The `forEach()` method executes a provided function once for each array element.

```javascript
let fruits = ['Apple', 'Banana', 'Cherry', 'Orange', 'Grapes', 'Kiwi'];
fruits.forEach(fruit => console.log(fruit));
```

#### `every()`, `some()`

The `every()` method tests whether all elements in the array pass the test implemented by the provided function. It returns a Boolean value.

The `some()` method tests whether at least one element in the array passes the test implemented by the provided function. It returns a Boolean value.

```javascript
let numbers = [3, 1, 4, 1, 5, 9, 2, 6, 5, 3, 5];
let allEven = numbers.every(num => num % 2 === 0);
console.log(allEven); // false
console.log(numbers.some(num => num % 2 === 0)); // true
```

#### `join()`

The `join()` method creates and returns a new string by concatenating all of the elements in an array, separated by commas or a specified separator string.

```javascript
let fruits = ['Apple', 'Banana', 'Cherry', 'Orange', 'Grapes', 'Kiwi'];
let fruitsString = fruits.join(', ');
console.log(fruitsString); // Apple, Banana, Cherry, Orange, Grapes, Kiwi
```

#### `toString()`

The `toString()` method returns a string representing the specified array and its elements.

```javascript
let fruits = ['Apple', 'Banana', 'Cherry', 'Orange', 'Grapes', 'Kiwi'];
console.log(fruits.toString()); // Apple,Banana,Cherry,Orange,Grapes,Kiwi

let numbers = [3, 1, 4, 1, 5, 9, 2, 6, 5, 3, 5];
console.log(numbers.toString()); // 3,1,4,1,5,9,2,6,5,3,5
```

#### `isArray()`

The `isArray()` method determines whether the passed value is an Array.

```javascript
let fruits = ['Apple', 'Banana', 'Cherry', 'Orange', 'Grapes', 'Kiwi'];
console.log(Array.isArray(fruits)); // true
```

#### Array From

The `Array.from()` method creates a new, shallow-copied Array instance from an array-like or iterable object.

```javascript
let str = 'Hello, World!';
let strArray = Array.from(str);
console.log(strArray); // ['H', 'e', 'l', 'l', 'o', ',', ' ', 'W', 'o', 'r', 'l', 'd', '!']

let set = new Set([1, 2, 3, 4, 5]);
let setArray = Array.from(set);
console.log(setArray); // [1, 2, 3, 4, 5]
```

#### Array Of

The `Array.of()` method creates a new Array instance with a variable number of arguments, regardless of the number or type of the arguments.

```javascript
let numbers = Array.of(1, 2, 3, 4, 5);
console.log(numbers); // [1, 2, 3, 4, 5]
```

#### Flatten an Array

You can flatten an array using the `flat()` method. The `flat()` method creates a new array with all sub-array elements concatenated into it recursively up to the specified depth.

```javascript
let numbers = [1, [2, 3], [4, [5, 6]]];
let flatNumbers = numbers.flat();
console.log(flatNumbers); // [1, 2, 3, 4, [5, 6]]
```

#### Multi-dimensional Arrays

You can create multi-dimensional arrays by nesting arrays inside arrays.

```javascript
let matrix = [
  [1, 2, 3],
  [4, 5, 6],
  [7, 8, 9]
];

console.log(matrix[0][0]); // 1
console.log(matrix[1][1]); // 5
console.log(matrix[2][2]); // 9
```


### [ ⏭ Next: Objects in JS](./12_objects.md)

### [🔙 Back To JS Readme](./js.md)

### [🔙 Back To Main Readme](../../../README.md)

🙏 Please credit me if you use this or share it with others. 🙏

