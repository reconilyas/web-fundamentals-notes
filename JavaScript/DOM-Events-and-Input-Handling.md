# DOM Events and Input Handling

## Event Listeners

JavaScript can detect and respond to user actions using `addEventListener()`.

Syntax:

```javascript
element.addEventListener('event', function);

Example:

button.addEventListener('click', function(){

    console.log("Button clicked");

});
Common Events

Common JavaScript events:

Event	Description
click	Runs when an element is clicked
submit	Runs when a form is submitted
input	Runs when input value changes
change	Runs when a value changes
keyup	Runs when a keyboard key is released
Form Submit Event

The submit event runs when the user submits a form.

Example:

var form = document.getElementById('addForm');

form.addEventListener('submit', addItem);

When the form is submitted, the addItem() function is executed.

Prevent Default Behavior

Browsers have default actions for certain events.

Example:

A form submission refreshes the page.
A link redirects the user.

preventDefault() stops the browser's default behavior.

Example:

function addItem(e){

    e.preventDefault();

}

Example use:

Preventing a form from refreshing the page after submission.

Creating Elements Dynamically

JavaScript can create new HTML elements while the webpage is running.

Example:

var li = document.createElement('li');

This creates a new <li> element.

Adding a Class
li.className = 'list-group-item';
Adding Text
li.appendChild(
    document.createTextNode(newItem)
);

This adds text inside the created element.

Adding Elements to the DOM

After creating an element, it must be added to the webpage.

Example:

itemList.appendChild(li);

This inserts the new element into the DOM.

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

Result:

<li>
    Item
    <button>X</button>
</li>
Event Delegation

Event delegation allows us to add one event listener to a parent element instead of adding listeners to every child element.

Example:

itemList.addEventListener('click', removeItem);

The parent element detects clicks from its child elements.

Advantages:

Better performance
Works with dynamically created elements
Less code
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
Remove the element from the DOM.
Filtering Items

Input filtering allows users to search through elements dynamically.

Example:

function filterItems(e){

    var text = e.target.value.toLowerCase();

}

The input is converted to lowercase to make searching case-insensitive.

Example:

User Input:
APPLE

Converted:
apple
Getting List Elements

Example:

var items = itemList.getElementsByTagName('li');

This retrieves all <li> elements inside the list.

Converting HTML Collection to Array

getElementsByTagName() returns an HTML Collection, not a normal array.

To use array methods:

Array.from(items).forEach(function(item){

});

Now methods like:

forEach()
map()
filter()

can be used.

Checking Text Content

Example:

var itemName = item.firstChild.textContent;

This retrieves the text inside an element.

Example:

HTML:

<li>
    Apple
</li>

Output:

Apple
Display Filtering Logic

If the item contains the search text:

item.style.display = 'block';

Otherwise:

item.style.display = 'none';

Example:

Searching:

app

Results:

Apple   → visible
Car     → hidden
Laptop  → hidden
DOM Events and Web Security

Understanding DOM events is important for web security because JavaScript handles user input and modifies webpage content.

Security risks related to DOM manipulation:

DOM-based XSS
Unsafe input handling
Client-side validation bypass

Important rule:

Never trust user-controlled input. Always validate and sanitize data on the server side.
