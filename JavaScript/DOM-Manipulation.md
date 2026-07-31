# DOM (Document Object Model)

## What is DOM?

The DOM (Document Object Model) is a representation of an HTML document as a tree of objects.

The browser creates the DOM when it loads a webpage.

JavaScript can interact with the DOM to:

- Read elements
- Modify content
- Change styles
- Create new elements
- Remove elements

---

# Exploring the Document Object

To see all information about the document:

```javascript
console.dir(document);

To access specific document information:

console.log(document.title);
console.log(document.URL);
console.log(document.domain);
Selecting Elements
getElementById()

Used to select an element by its ID.

Example:

var headerTitle = document.getElementById('header-title');

headerTitle.textContent = 'Hello';

headerTitle.innerText = 'Goodbye';
getElementsByClassName()

Used to select elements by their class name.

Example:

var items = document.getElementsByClassName('list-group-item');

console.log(items);

items[1].textContent = 'Hello';

items[2].textContent = 'Booo';

items[1].style.fontWeight = 'bold';

items[1].style.backgroundColor = 'yellow';
getElementsByTagName()

Used to select elements by their HTML tag.

Example:

var items = document.getElementsByTagName('li');

console.log(items);

items[1].textContent = 'Hello';

items[2].textContent = 'Booo';
querySelector()

Used to select the first element that matches a CSS selector.

Example:

var input = document.querySelector('input');

input.value = 'Type here';
Changing Elements

JavaScript can modify HTML elements.

Example:

document.getElementById('header-title').textContent = 'New Title';

Changing styles:

headerTitle.style.borderBottom = 'solid 3px #000';
Parent Elements
parentNode

Returns the parent node of an element.

Example:

var itemList = document.querySelector('#items');

console.log(itemList.parentNode);

itemList.parentNode.style.background = '#aa1414';
parentElement

Returns the parent element.

Example:

console.log(itemList.parentElement);
Child Elements
childNodes

Returns all child nodes.

console.log(itemList.childNodes);
firstChild

Returns the first child node.

console.log(itemList.firstChild);
firstElementChild

Returns the first child element.

console.log(itemList.firstElementChild);

itemList.firstElementChild.textContent = 'Hello';
lastChild

Returns the last child node.

console.log(itemList.lastChild);
lastElementChild

Returns the last child element.

console.log(itemList.lastElementChild);

itemList.lastElementChild.textContent = 'Hello';
Creating Elements

JavaScript can create new HTML elements.

Create Element
var newDiv = document.createElement('div');
Add Class
newDiv.className = 'hello';
Add ID
newDiv.id = 'hiii';
Add Attributes
newDiv.setAttribute('title','hello div');
Adding Elements to the DOM

Example:

var container = document.querySelector('header .container');

var h1 = document.querySelector('header h1');

container.insertBefore(newDiv, h1);

This inserts the new element into the webpage.

DOM Manipulation Summary

Common DOM methods:

Method	Purpose
getElementById()	Select element by ID
getElementsByClassName()	Select elements by class
getElementsByTagName()	Select elements by tag
querySelector()	Select using CSS selectors
createElement()	Create new elements
appendChild()	Add elements
insertBefore()	Insert before another element

