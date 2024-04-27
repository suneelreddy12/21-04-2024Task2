# Difference between Document and Window Objects in JavaScript

## Document Object: (blueprint of web pages)

- The Document object represents the entire HTML content of a web page, including its structure, elements, and text content. It serves as an in-memory representation of the document loaded in the browser window or tab.

### Accessing Elements:
- One of the primary functions of the Document object is to provide methods for accessing and manipulating elements within the document. we can use methods like getElementById, getElementsByClassName, and querySelector to select elements based on various criteria such as ID, class, or CSS selector.

### Modifying Content:
The Document object allows us to dynamically modify the content of the web page. This includes updating text content, attributes, and styles of existing elements, as well as adding or removing elements from the document.

### Handling Events:
The Document object provides methods for registering event listeners and handling user interactions within the document. we can attach event handlers to elements or the document itself to respond to user actions such as clicks, keypresses, or form submissions.

// Example: Adding a click event listener to an element
element.addEventListener('click', function() {
    console.log('Element clicked!');
});

### Traversal and Manipulation:
In addition to selecting elements by their IDs or classes, we can traverse the document tree and manipulate elements based on their relationships with other elements. This allows for more complex interactions and dynamic updates to the document structure.

// Example: Appending a new element to an existing one
let newElement = document.createElement('div');
element.appendChild(newElement);

### Basic HTML Document

<!-- HTML code snippet -->
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <script src = 'sample.js' defer></script>
</head>
<body>
    <h1>hello</h1>
</body>
</html>

- Example of how to access content field

```javascript
// JavaScript code snippet
// Accessing the <head> element
let headElement = document.head;
// Accessing all <meta> elements within the <head> element
let metaTags = headElement.getElementsByTagName('meta');
// Looping through the <meta> elements to find the one with name="viewport"
for (let i = 0; i < metaTags.length; i++) {
    if (metaTags[i].getAttribute('name') === 'viewport') {
        // Retrieving the content attribute value of the <meta> tag
        let viewportContent = metaTags[i].getAttribute('content');
        // Logging the content attribute value to the console
        console.log(viewportContent); // Output: "width=device-width, initial-scale=1.0"
        // Exit the loop since we found the desired <meta> tag
        break;
    }
}
```

- Example of how to access text from h1 tag

```javascript
// JavaScript code snippet
// Accessing the <body> element
let bodyElement = document.body;
// Accessing the first child node of the <body> element, which is the <h1> element
let h1Element = bodyElement.firstChild;
// Retrieving the text content of the <h1> element
let helloText = h1Element.textContent;
// Logging the text content to the console
console.log(helloText); // Output: "hello"
```

## Window Object:

