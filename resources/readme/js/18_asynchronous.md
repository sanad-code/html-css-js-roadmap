# Welcome 🙋‍♂️ to Asynchronous JS 🏆

🙏 Please credit me if you use this or share it with others. 🙏

### [🔙 Back To JS Readme](./js.md)

### [🔙 Back To Main Readme](../../../README.md)

## Asynchronous JavaScript

In this section we will talk about the following:

1. Callbacks
2. Promises
3. Async/Await
4. Event Loop, Task Queue and Call Stack
5. setTimeout, setInterval and clearTimeout
6. AJAX and Fetch API

### 1. Callbacks

A callback is a function that is passed as an argument to another function and is executed after its parent function has completed. 

The callback function is used to notify the parent function that a certain task has been completed. It is mostly used in asynchronous programming. As JavaScript is a single-threaded language, it can only do one thing at a time.

```js
const myCallback = function(){
  console.log('I am a callback')
}

const myFunction = function(callback){
  console.log('I am a function')
  callback()
}

myFunction(myCallback)
```

Callbacks introduce a problem called "Callback Hell" or "Pyramid of Doom" when multiple callbacks are nested within each other. This makes the code difficult to read and maintain.

```js
const myCallback = function(){
  console.log('I am a callback')
}

const myFunction = function(callback){
  console.log('I am a function')
  callback()
}

myFunction(function(){
  console.log('I am a callback')
  myFunction(function(){
    console.log('I am a callback')
    myFunction(function(){
      console.log('I am a callback')
    })
  })
})
```

### 2. Promises

Promises are a way to handle asynchronous operations in JavaScript. A promise is an object that represents the eventual completion or failure of an asynchronous operation and its resulting value.

A promise can be in one of three states:

1. Pending: Initial state, neither fulfilled nor rejected.
2. Fulfilled: The operation completed successfully.
3. Rejected: The operation failed.

```js
const myPromise = new Promise((resolve, reject) => {
  setTimeout(() => {
    resolve('Promise resolved')
  }, 2000)
})

myPromise.then((value) => {
  console.log(value)
})
```

Notes: 
    - A promise can only be resolved once.
    - A promise can be chained using the `then` method.
    - A promise can be rejected using the `reject` method.
    - A promise can be caught using the `catch` method.
    - A promise can be settled using the `finally` method.
    - A promise can be created using the `Promise.resolve` and `Promise.reject` methods.
    - A promise can be all or any using the `Promise.all` and `Promise.any` methods.

```js
const myPromise = new Promise((resolve, reject) => {
  setTimeout(() => {
    resolve('Promise resolved')
  }, 2000)
})

myPromise
  .then((value) => {
    console.log(value)
    return 'New Promise'
  })
  .then((value) => {
    console.log(value)
    return Promise.resolve('Another Promise')
  })
  .then((value) => {
    console.log(value)
    return Promise.reject('Rejected Promise')
  })
  .catch((error) => {
    console.log(error)
  })
  .finally(() => {
    console.log('Promise settled')
  })
```

Don't nest promises, use chaining instead.

This is bad way to write promises:

```js
const myPromise = new Promise((resolve, reject) => {
  setTimeout(() => {
    resolve('Promise resolved')
  }, 2000)
})

myPromise.then((value) => {
  console.log(value)
  myPromise.then((value) => {
    console.log(value)
    myPromise.then((value) => {
      console.log(value)
    })
  })
})
```

### 3. Async/Await

Async/Await is a modern way to handle asynchronous operations in JavaScript. The `async` keyword is used to define an asynchronous function, and the `await` keyword is used to wait for a promise to be resolved.

```js
const myPromise = new Promise((resolve, reject) => {
  setTimeout(() => {
    resolve('Promise resolved')
  }, 2000)
})

const myFunction = async () => {
  console.log('Before promise')
  const value = await myPromise
  console.log(value)
  console.log('After promise')
}

myFunction()
```

Notes:
    - An async function always returns a promise.
    - The `await` keyword can only be used inside an async function.
    - The `await` keyword pauses the execution of the async function until the promise is resolved.
    - The `await` keyword can be used with any promise, not just promises created using the `new Promise` constructor.
    - The `await` keyword can be used with the `Promise.all` and `Promise.any` methods.
    - async/await dosen't work with setTimeout, setInterval, and event listeners.

```js
const myPromise = new Promise((resolve, reject) => {
  setTimeout(() => {
    resolve('Promise resolved')
  }, 2000)
})

const myFunction = async () => {
  console.log('Before promise')
  const value = await myPromise
  console.log(value)
  console.log('After promise')
}

myFunction()
```

### 4. Event Loop, Task Queue and Call Stack

The Event Loop is a mechanism that allows JavaScript to perform non-blocking I/O operations. It is responsible for handling asynchronous operations in JavaScript.

The Event Loop consists of the following components:

1. Call Stack: A data structure that stores function calls.
2. Task Queue: A data structure that stores tasks to be executed. Tasks first runs in the background and then are added to task queue.

The Event Loop works as follows:

1. The Event Loop continuously checks the Call Stack and Task Queue.
2. If the Call Stack is empty, the Event Loop checks the Task Queue.
3. If there are tasks in the Task Queue, the Event Loop adds them to the Call Stack.
4. The tasks are executed in the Call Stack.

```js
console.log('Start')

setTimeout(() => {
  console.log('Timeout')
}, 0)

console.log('End')

//This will output: Start, End, Timeout
```

### 5. setTimeout, setInterval and clearTimeout

The `setTimeout` function is used to execute a function after a specified delay. The `setInterval` function is used to execute a function repeatedly at a specified interval. The `clearTimeout` function is used to cancel a timeout.

```js
const timeout = setTimeout(() => {
  console.log('Timeout')
}, 2000)

clearTimeout(timeout)
```

```js
const interval = setInterval(() => {
  console.log('Interval')
}, 2000)

clearInterval(interval)
```

### 6. AJAX and Fetch API

AJAX (Asynchronous JavaScript and XML) is a technique used to send and receive data from a server without reloading the page. The Fetch API is a modern replacement for AJAX that provides a more powerful and flexible way to make HTTP requests.

```js
const xhr = new XMLHttpRequest()
xhr.open('GET', 'https://jsonplaceholder.typicode.com/posts')
xhr.onload = () => {
  if (xhr.status === 200) {
    console.log(JSON.parse(xhr.responseText))
  } else {
    console.log('Error')
  }
}
xhr.send()
```

```js
fetch('https://jsonplaceholder.typicode.com/posts')
  .then(response => {
    if (response.ok) {
      return response.json()
    } else {
      throw new Error('Error')
    }
  })
  .then(data => {
    console.log(data)
  })
  .catch(error => {
    console.log(error)
  })
```

### Handling multiple promises

#### Promise.all

The `Promise.all` method is used to wait for all promises to be resolved. It returns a single promise that resolves when all promises are resolved.

```js
const promise1 = new Promise((resolve, reject) => {
  setTimeout(() => {
    resolve('Promise 1 resolved')
  }, 2000)
})

const promise2 = new Promise((resolve, reject) => {
  setTimeout(() => {
    resolve('Promise 2 resolved')
  }, 2000)
})

Promise.all([promise1, promise2])
  .then(values => {
    console.log(values)
  })
```

#### Promise.any

The `Promise.any` method is used to wait for any promise to be resolved. It returns a single promise that resolves when any promise is resolved.

```js
const promise1 = new Promise((resolve, reject) => {
  setTimeout(() => {
    resolve('Promise 1 resolved')
  }, 2000)
})

const promise2 = new Promise((resolve, reject) => {
  setTimeout(() => {
    resolve('Promise 2 resolved')
  }, 2000)
})

Promise.any([promise1, promise2])
  .then(value => {
    console.log(value)
  })
```

#### Promise.race

The `Promise.race` method is used to wait for the first promise to be resolved. It returns a single promise that resolves when the first promise is resolved.

```js
const promise1 = new Promise((resolve, reject) => {
  setTimeout(() => {
    resolve('Promise 1 resolved')
  }, 2000)
})

const promise2 = new Promise((resolve, reject) => {
  setTimeout(() => {
    resolve('Promise 2 resolved')
  }, 2000)
})

Promise.race([promise1, promise2])
  .then(value => {
    console.log(value)
  })
```

#### Promise.resolve

The `Promise.resolve` method is used to create a resolved promise.

```js
const promise = Promise.resolve('Resolved promise')

promise.then(value => {
  console.log(value)
})
```

#### Promise.reject

The `Promise.reject` method is used to create a rejected promise.

```js

const promise = Promise.reject('Rejected promise')

promise.catch(error => {
  console.log(error)
})
```


### [ ⏭ Next: DOM](./19_dom.md)

### [🔙 Back To JS Readme](./js.md)

### [🔙 Back To Main Readme](../../../README.md)

🙏 Please credit me if you use this or share it with others. 🙏

