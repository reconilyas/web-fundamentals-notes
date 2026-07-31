# JavaScript Events

## What are Events?

Events are actions or occurrences that happen inside the browser.

Examples:

- Clicking a button
- Moving the mouse
- Typing in an input field
- Submitting a form
- Focusing on an element

JavaScript can listen for these events and execute functions when they occur.

---

# addEventListener()

`addEventListener()` is used to attach an event listener to an HTML element.

Syntax:

```javascript
element.addEventListener('event', function);

Example:

var button = document.getElementById('button');

button.addEventListener('click', buttonClick);

function buttonClick(e){

    console.log('Button clicked');

}
Event Object

When an event occurs, JavaScript automatically creates an event object.

The event object contains information about the event.

Example:

function buttonClick(e){

    console.log(e);

}
Event Properties
target

target returns the element that triggered the event.

Example:

console.log(e.target);

Getting the ID of the clicked element:

console.log(e.target.id);
className

Returns the class name of the element.

Example:

console.log(e.target.className);
tagName

Returns the HTML tag name of the element.

Example:

console.log(e.target.tagName);

Output:

BUTTON
type

Returns the type of event.

Example:

console.log(e.type);

Output:

click
Mouse Events

Mouse events happen when users interact with the mouse.

click

Runs when an element is clicked.

Example:

button.addEventListener('click', runEvent);
mousedown

Runs when the mouse button is pressed.

Example:

button.addEventListener('mousedown', runEvent);
mouseup

Runs when the mouse button is released.

Example:

button.addEventListener('mouseup', runEvent);
mouseenter

Runs when the mouse enters an element.

Example:

box.addEventListener('mouseenter', runEvent);
mouseleave

Runs when the mouse leaves an element.

Example:

box.addEventListener('mouseleave', runEvent);
mouseover and mouseout
mouseover

Runs when the mouse moves over an element.

mouseout

Runs when the mouse leaves an element.

Example:

box.addEventListener('mouseover', runEvent);

box.addEventListener('mouseout', runEvent);
Mouse Position
clientX and clientY

Returns the mouse position relative to the browser window.

Example:

console.log(e.clientX);

console.log(e.clientY);
offsetX and offsetY

Returns the mouse position relative to the target element.

Example:

console.log(e.offsetX);

console.log(e.offsetY);
Keyboard Events

Keyboard events occur when users interact with the keyboard.

keydown

Runs when a key is pressed.

Example:

input.addEventListener('keydown', runEvent);
keyup

Runs when a key is released.

Example:

input.addEventListener('keyup', runEvent);
keypress

Runs when a key is pressed.

Note:

keypress is an older event and is not commonly used in modern JavaScript.

Example:

input.addEventListener('keypress', runEvent);
Input Events

Input events happen when users interact with form elements.

focus

Runs when an element becomes active.

Example:

input.addEventListener('focus', runEvent);
blur

Runs when an element loses focus.

Example:

input.addEventListener('blur', runEvent);
cut

Runs when text is cut.

Example:

input.addEventListener('cut', runEvent);
paste

Runs when text is pasted.

Example:

input.addEventListener('paste', runEvent);
input

Runs whenever the input value changes.

Example:

input.addEventListener('input', runEvent);

Example function:

function runEvent(e){

    console.log(e.target.value);

}
Event Handler Function

A single function can handle multiple events.

Example:

function runEvent(e){

    console.log('EVENT TYPE: ' + e.type);

}

Example:

button.addEventListener('click', runEvent);

input.addEventListener('keyup', runEvent);
JavaScript Events and Web Security

Understanding JavaScript events is important for web security because events often process user input.

Security risks related to event handling include:

DOM-based XSS
Unsafe input processing
Client-side validation bypass

Important rule:

Client-side JavaScript should never be trusted as a security control. Validation and authorization must always be enforced on the server side.
