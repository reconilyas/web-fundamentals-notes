# DOM Events and Input Handling

## Event Listeners

JavaScript can listen for user actions using `addEventListener()`.

Syntax:

```javascript
element.addEventListener('event', function);

Common events:

click
submit
input
change
keyup
Form Submit Event

Example:

var form = document.getElementById('addForm');

form.addEventListener('submit', addItem);

The submit event runs when the user submits a form.

Prevent Default Behavior

preventDefault() prevents the browser's default action.

Example:

function addItem(e){

e.preventDefault();

}

Example:

Preventing a form from refreshing the page after submission.
Creating Elements Dynamically

JavaScript can create new HTML elements.

Example:

var li = document.createElement('li');

Adding a class:

li.className = 'list-group-item';

Adding text:

li.appendChild(document.createTextNode(newItem));
Adding Elements to the DOM

Example:

itemList.appendChild(li);

This adds the new element to the webpage.

Creating a Delete Button

Example:

var deleteBtn = document.createElement('button');

deleteBtn.className = 
'btn btn-danger btn-sm float-right delete';

deleteBtn.appendChild(
document.createTextNode('X')
);

The button is then added inside the list item:

li.appendChild(deleteBtn);
Event Delegation

Instead of adding an event listener to every delete button, we can add one listener to the parent element.

Example:

itemList.addEventListener('click', removeItem);

The parent detects clicks from its child elements.

This is useful when elements are created dynamically.

Removing Elements

Example:

function removeItem(e){

if(e.target.classList.contains('delete')){

if(confirm('Are you sure?')){

var li = e.target.parentElement;

itemList.removeChild(li);

}

}

}

Steps:

Check if the clicked element has the delete class.
Get the parent element.
Remove it from the DOM.
Filtering Items

Input filtering allows users to search through elements.

Example:

function filterItems(e){

var text = e.target.value.toLowerCase();

}

The input is converted to lowercase to make searching easier.

Getting List Elements

Example:

var items = itemList.getElementsByTagName('li');

This gets all list items.

Converting HTML Collection to Array
Array.from(items).forEach(function(item){

});

This allows using array methods such as forEach().

Checking Text Content

Example:

var itemName = item.firstChild.textContent;

Gets the text inside the element.

Display Filtering Logic

If the item contains the search text:

item.style.display = 'block';

Otherwise:

item.style.display = 'none';
