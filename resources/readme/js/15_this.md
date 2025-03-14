# Welcome 🙋‍♂️ to JS This 🏆

🙏 Please credit me if you use this or share it with others. 🙏

### [🔙 Back To JS Readme](./js.md)

### [🔙 Back To Main Readme](../../../README.md)

## This in JavaScript Explained

## Purpose of this

Reues functions with different context

## This keyword rules

- Implicit Binding [Left]
- Explicit Binding [right]
- new Binding
- window Binding

## How to figure out the value of this ? 

Always ask your self where the function is invoked!

In this example we don't know yet what is the value of this because the functions are not invoked

```js
let a = 3;
let b = 4;

const functionA= function(){
  console.log(this.a)
}


const objectA = {
  a : 1,
  b : 2,
  c : function(){
    console.log(this.a)
  }
}
```

This is exactly same as asking you what is the result of this function without passing the parameter yet

```js
const multiplyBy2 = function(number){
  console.log(number * 2)
}
```

We can't know what is the result until we get actual invokation

```js
multiplyBy2(4) // result is 8
```

## Implicit Binding

When a function is invoked look to the **Left** of the function if there is an object then this will be the **this**

```js
const objectA = {
  a : 1,
  b : 2,
  c : function(){
    console.log(this.a)
  }
}

objectA.c() // result will be 1, because when c function is invoked the left of the function is objectA which will act as this, since we are calling this.a then the value will be 1
```

We can utilize this concept by creating function Mixins or decoration

```js
const sayHi = function(obj){
    obj.greet = function(){
        console.log(`Hello ${this.name}`)
    }
}

const a = {name:'Moataz'}

const b = {name:'Sanad'}

sayHi(a)
sayHi(b)

a.greet(); // Hello Moataz
b.greet(); // Hello Sanad

```

What about more complex object ?

```js
const obj = {
  name:'Moataz',
  sayName : function(){
    console.log(this.name)
  },
  manager:{
    name : 'Mohamed',
    sayName : function(){
      console.log(this.name)
    }
  }
}

obj.sayName(); // Moataz
obj.manager.sayName(); // Mohamed
```

## Explicit Binding Call, Apply, Bind

### call(this,args[0],args[1],....)

calling call method on any function will 

- Invoke the function immediatly
- Set this scope
- Pass parameters as , separated

```js
const sayHi = function(){
    console.log(this.name)
}

objA = {a:1,name:'Moataz'}
objB = {b:1,name:'Sanad'}

sayHi.call(objA); //Moataz
sayHi.call(objB); //Sanad
```

### apply(this,argsAsArray)

calling apply method on any function will 

- Invoke the function immediatly
- Set this scope
- Pass parameters as and array, this is useful when you don't know how many parameters you will pass

```js
const sayHi = function(){
    console.log(this.name)
}

objA = {a:1,name:'Moataz'}
objB = {b:1,name:'Sanad'}

sayHi.apply(objA); //Moataz
sayHi.apply(objB); //Sanad
```

### bind(this,args[0],args[1],....)

calling apply method on any function will 

- Return a new function with this scope is set
- Pass parameters to function as , separated

```js
const sayHi = function(name){
    console.log(this.name)
}

objA = {a:1,name:'Moataz'}
objB = {b:1,name:'Sanad'}

const hiA = sayHi.bind(objA)
const hiB = sayHi.bind(objB)

console.log("Doing some logic")
hiA()
hiB()

```

## new Binding

When you use new Keyward js implicitly creates this as empty object {} at the begining of the function and finally it returns this newly created object

```js
const Person = function(name,age){
  //this={}
  this.age = age;
  this.name = name;
  //return this
}

let moataz = new Person('Moataz',36)
console.log(moataz)
```

## window Binding

If you invoke a function and nothing to its left or nothing on the right (call,apply,bind) and no "new" keyword then this will be window scope.

```js
const sayHi = function(){
    console.log(this)
}

sayHi() // window
```

## Arrow Functions

Arrow functions do not have their own this. The value of this inside an arrow function is always inherited from the enclosing scope.

```js
const obj = {
  name: "John",
  greet: function() {
    console.log(this.name);
  },
  greetArrow: () => {
    console.log(this.name);
  },
  greetNested: function() {
    const nested = () => {
      console.log(this.name);
    };
    nested();
  }
};

obj.greet(); // John, this is the greeting function this scope

obj.greetArrow(); // undefined, this is the global scope this

obj.greetNested(); // John, this is the greetNested function this scope
```

### [ ⏭ Next: Logical Control](./16_logical_control.md)

### [🔙 Back To JS Readme](./js.md)

### [🔙 Back To Main Readme](../../../README.md)

🙏 Please credit me if you use this or share it with others. 🙏

