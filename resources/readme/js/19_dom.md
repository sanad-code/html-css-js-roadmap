# Welcome 🙋‍♂️ to JS DOM 🏆

🙏 Please credit me if you use this or share it with others. 🙏

### [🔙 Back To JS Readme](./js.md)

### [🔙 Back To Main Readme](../../../README.md)

## DOM Document Object Model

The following topics will be covered in this section:

- document object
- Selecting html nodes from JS.
- Changing the nodes styles from JS.
- Changing the node text from JS.
- Changing the innerHtml of a node from JS.
- Use JS to add or remove elements.
- Add event listeners to html nodes.

### The Document Object

The Document Object Model (DOM) is a programming interface for web documents. It represents the structure of an HTML document as a tree of nodes. The DOM provides a way for programs to interact with the structure and content of a web page.

The `document` object is the root of the DOM tree. It represents the entire HTML document and provides methods and properties for working with the document.

### Selecting HTML Nodes

You can select HTML nodes using the `document` object and various methods provided by the DOM API. Here are some common methods for selecting nodes:

- `getElementById()`: Selects an element by its ID.
- `getElementsByClassName()`: Selects elements by their class name.
- `getElementsByTagName()`: Selects elements by their tag name.
- `querySelector()`: Selects the first element that matches a CSS selector.
- `querySelectorAll()`: Selects all elements that match a CSS selector.

```javascript
// Select an element by its ID
let element = document.getElementById("myElement");

// Select elements by their class name
let elements = document.getElementsByClassName("myClass");

// Select elements by their tag name
let elements = document.getElementsByTagName("div");

// Select the first element that matches a CSS selector
let element = document.querySelector(".myClass");

// Select all elements that match a CSS selector
let elements = document.querySelectorAll(".myClass");
```

### Changing Node Styles

You can change the styles of HTML nodes using the `style` property of the node. The `style` property is an object that contains the CSS properties of the node.

Note: The CSS property names in JavaScript are written in camelCase, e.g., `backgroundColor` instead of `background-color`.

```javascript
// Change the background color of an element
element.style.backgroundColor = "red";

// Change the font size of an element
element.style.fontSize = "16px";
```

### Changing Node Text

You can change the text content of HTML nodes using the `textContent` property of the node. The `textContent` property sets or returns the text content of the node and its descendants.

```javascript
// Change the text content of an element
element.textContent = "Hello, World!";
```

### Changing InnerHTML

You can change the inner HTML of HTML nodes using the `innerHTML` property of the node. The `innerHTML` property sets or returns the HTML content of the node and its descendants.

```javascript
// Change the inner HTML of an element
element.innerHTML = "<strong>Hello, World!</strong>";
```

### Adding and Removing Elements

You can add or remove elements from the DOM using the following methods:

- `appendChild()`: Adds a new child node to an element.
- `removeChild()`: Removes a child node from an element.
- `createElement()`: Creates a new element node.
- `createTextNode()`: Creates a new text node.
- `insertBefore()`: Inserts a new node before an existing node.
- `replaceChild()`: Replaces an existing node with a new node.
- `cloneNode()`: Clones a node.
- `remove()`: Removes an element from the DOM.
- `insertAdjacentHTML()`: Inserts HTML into the DOM at a specified position.
- `insertAdjacentElement()`: Inserts an element into the DOM at a specified position.
- `insertAdjacentText()`: Inserts text into the DOM at a specified position.
- `before()`: Inserts an element before another element.
- `after()`: Inserts an element after another element.
- `prepend()`: Inserts an element at the beginning of another element.
- `append()`: Inserts an element at the end of another element.
  

```javascript
// Create a new element
let newElement = document.createElement("div");
newElement.textContent = "Hello, World!";
newElement.style.color = "red";

// Add the new element to the document
document.body.appendChild(newElement);

// Remove an element from the document
document.body.removeChild(newElement);
```

### Adding Event Listeners

You can add event listeners to HTML nodes using the `addEventListener()` method. Event listeners are used to handle events such as clicks, keypresses, and mouse movements.

```javascript
// Add an event listener to an element
element.addEventListener("click", () => {
  console.log("Element clicked");
});
```

### Example

```html
<!DOCTYPE html>
<html>
<head>
  <title>DOM Example</title>
</head>
<body>
  <div id="myDiv">Hello, World!</div>
  <button id="myButton">Click Me</button>

  <script>
    // Select the div element
    let div = document.getElementById("myDiv");

    // Change the text content of the div element
    div.textContent = "Hello, JavaScript!";

    // Select the button element
    let button = document.getElementById("myButton");

    // Add an event listener to the button element
    button.addEventListener("click", () => {
      console.log("Button clicked");
    });
  </script>
</body>
</html>
```

Note: Adding same event listener to multiple elements is not a good practice. Instead, you can use event delegation to handle events on multiple elements.

The idea of event delegation is to add a single event listener to a parent element and use the `event.target` property to determine which child element triggered the event.

The event propagation model in the DOM consists of three phases: capturing, target, and bubbling. By default, event listeners are added in the bubbling phase. You can use the `addEventListener()` method with the `useCapture` parameter set to `true` to add event listeners in the capturing phase.

```javascript
// Add an event listener in the capturing phase
element.addEventListener("click", () => {
  console.log("Element clicked");
}, true);
```

Example

```html
<!DOCTYPE html>
<html>
<head>
  <title>Event Delegation Example</title>
</head>
<body>
  <ul id="myList">
    <li>Item 1</li>
    <li>Item 2</li>
    <li>Item 3</li>
  </ul>

  <script>
    // Select the ul element
    let ul = document.getElementById("myList");

    // Add an event listener to the ul element
    ul.addEventListener("click", (event) => {
      if (event.target.tagName === "LI") {
        console.log("Item clicked:", event.target.textContent);
      }
    });
  </script>
</body>
</html>
```

### [ ⏭ Next: OOP](./20_oop.md)

### [🔙 Back To JS Readme](./js.md)

### [🔙 Back To Main Readme](../../../README.md)

🙏 Please credit me if you use this or share it with others. 🙏

