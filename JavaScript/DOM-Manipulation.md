# DOM (Document Object Model)

## What is DOM?

The **DOM (Document Object Model)** is a programming interface that represents an HTML document as a tree of objects.

When a browser loads a webpage, it converts the HTML document into the DOM.

JavaScript can interact with the DOM to:

- Read HTML elements
- Modify content
- Change styles
- Create new elements
- Remove elements
- Handle user interactions

Example:

HTML:

```html
<h1 id="title">Hello</h1>

JavaScript:

document.getElementById("title").textContent = "New Title";

The webpage content changes dynamically without reloading the page.

Document Object

The document object represents the entire HTML page.

To view information about the document:

console.dir(document);

Access document information:

console.log(document.title);

console.log(document.URL);

console.log(document.domain);
Selecting Elements

JavaScript provides different methods to select HTML elements.

getElementById()

getElementById() selects an element using its ID.

Example:

HTML:

<h1 id="header-title">
    Hello
</h1>

JavaScript:

var headerTitle = document.getElementById('header-title');

headerTitle.textContent = "New Title";

headerTitle.innerText = "Goodbye";
getElementsByClassName()

Selects elements using their class name.

Example:

var items = document.getElementsByClassName('list-group-item');

console.log(items);

items[1].textContent = "Hello";

items[2].textContent = "Booo";

items[1].style.fontWeight = "bold";

items[1].style.backgroundColor = "yellow";
getElementsByTagName()

Selects elements using their HTML tag.

Example:

var items = document.getElementsByTagName('li');

console.log(items);

items[1].textContent = "Hello";

items[2].textContent = "Booo";
querySelector()

querySelector() selects the first element that matches a CSS selector.

Example:

var input = document.querySelector('input');

input.value = "Type here";

Examples:

document.querySelector("#id");

document.querySelector(".class");

document.querySelector("div");
Changing Elements

JavaScript can modify HTML content and styles.

Changing Text
document.getElementById('header-title').textContent = "New Title";
Changing Styles

Example:

headerTitle.style.borderBottom = "solid 3px #000";
Parent Elements

Parent elements contain child elements.

parentNode

Returns the parent node of an element.

Example:

var itemList = document.querySelector('#items');

console.log(itemList.parentNode);

itemList.parentNode.style.background = "#aa1414";
parentElement

Returns the parent element.

Example:

console.log(itemList.parentElement);
Child Elements

Child elements are elements inside another element.

childNodes

Returns all child nodes.

Example:

console.log(itemList.childNodes);
firstChild

Returns the first child node.

Example:

console.log(itemList.firstChild);
firstElementChild

Returns the first HTML element.

Example:

console.log(itemList.firstElementChild);

itemList.firstElementChild.textContent = "Hello";
lastChild

Returns the last child node.

Example:

console.log(itemList.lastChild);
lastElementChild

Returns the last HTML element.

Example:

console.log(itemList.lastElementChild);

itemList.lastElementChild.textContent = "Hello";
Creating Elements

JavaScript can create new HTML elements dynamically.

createElement()

Creates a new element.

Example:

var newDiv = document.createElement('div');
Add Class
newDiv.className = "hello";
Add ID
newDiv.id = "hiii";
Add Attributes
newDiv.setAttribute('title','hello div');
Adding Elements to the DOM

JavaScript can insert created elements into the webpage.

Example:

var container = document.querySelector('header .container');

var h1 = document.querySelector('header h1');

container.insertBefore(newDiv, h1);

This inserts the new element before the selected element.

Common DOM Methods
Method	Purpose
getElementById()	Select element by ID
getElementsByClassName()	Select elements by class
getElementsByTagName()	Select elements by tag
querySelector()	Select using CSS selectors
createElement()	Create new elements
appendChild()	Add elements
insertBefore()	Insert before another element
DOM and Web Security

Understanding the DOM is important for web security because JavaScript can manipulate webpage content.

Security issues related to DOM manipulation include:

DOM-based XSS
Unsafe user input handling
Client-side validation bypass

Important rule:

Never trust user-controlled input, even when it is processed by JavaScript.

