# Difference between Document and Window Objects in JavaScript

## Document Object: (blueprint of web pages)

- The Document object represents the entire HTML content of a web page, including its structure, elements, and text content. It serves as an in-memory representation of the document loaded in the browser window or tab.

### Accessing Elements:
- One of the primary functions of the Document object is to provide methods for accessing and manipulating elements within the document. we can use methods like getElementById, getElementsByClassName, and querySelector to select elements based on various criteria such as ID, class, or CSS selector.

### Modifying Content:
The Document object allows us to dynamically modify the content of the web page. This includes updating text content, attributes, and styles of existing elements, as well as adding or removing elements from the document.

### Handling Events:
The Document object provides methods for registering event listeners and handling user interactions within the document. we can attach event handlers to elements or the document itself to respond to user actions such as clicks, keypresses, or form submissions.

```javascript
// JavaScript code snippet
// Example: Adding a click event listener to an element
element.addEventListener('click', function() {
    console.log('Element clicked!');
});
```

### Traversal and Manipulation:
In addition to selecting elements by their IDs or classes, we can traverse the document tree and manipulate elements based on their relationships with other elements. This allows for more complex interactions and dynamic updates to the document structure.

```javascript
// JavaScript code snippet
// Example: Appending a new element to an existing one
let newElement = document.createElement('div');
element.appendChild(newElement);
```

### Basic HTML Document

```html
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
```
- The <!DOCTYPE html> declaration specifies the document type and version (HTML5).
- The <html> element serves as the root element of the document and defines the document's language as English (lang="en").
- The <head> section contains meta tags for specifying the character encoding (`
UTF-8) and viewport settings for responsive design. Additionally, it includes a <title>` element to provide a title for the document.
- Inside the <head> section, there's a <script> tag that references an external JavaScript file named "arrays.js", using the src attribute. The defer attribute is used to indicate that the script should be executed after the document has been parsed, ensuring that it doesn't block the rendering of the page.
- The <body> section contains the main content of the document, which in this case consists of a single <h1> heading element with the text "hello".

- Example of how to access value of content attribute

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

## Window Object: (Gateway to Browser Environment)

- The Window object represents the browser window or tab in which the web page is displayed. It serves as the global object for the browser environment and provides properties and methods for controlling the browser window, navigating between pages, and interacting with the browser environment

- window.document -> this will give you the HTML document of that particular web page.
- window is the object of browser, it is not the object of javascript.
- The Document object represents the content of a single web page, whereas the Window object represents the entire browser window or tab containing the page.
- window has lot of inbuilt methods such as alert(), prompt(), open(), close(), setTimeout(),... etc.
- alert() -> displays the alert box containing message with ok button. 
- prompt() -> displays a dialog box to get input from the user.
- open() -> opens the new window.

```javascript
// Example: Opening a new browser window using the Window object
let newWindow = window.open('https://example.com', '_blank');
```

- window.open() method, which opens a new browser window or tab. The first argument specifies the URL to be opened. The second argument, '_blank', specifies the target attribute for the newly opened window/tab. When ' _blank' is specified as the target, it instructs the browser to open the URL in a new, unnamed browsing context (typically a new tab or window). If no 2nd argument which is 
let newWindow = window.open('https://example.com'); This typically means that the URL will open in the same tab or window where the code is running, replacing the current page with the new URL.

- close() -> closes the current window.
- setTimeout() -> performs action after specified time like calling function,... etc.

