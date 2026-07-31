# JavaScript Basics

## What is JavaScript?

JavaScript is a high-level programming language.

It can be used in:

- Frontend (Client-side)
- Backend (Server-side) using environments such as Node.js

JavaScript allows developers to create interactive web applications and handle logic.

---

# Variables

JavaScript has three keywords for declaring variables:

- var
- let
- const

## var

`var` is the older way to declare variables.

It is function-scoped and is mostly replaced by `let` and `const` in modern JavaScript.

---

## let

`let` allows values to be changed.

Example:

```javascript
let score = 10;

score = 31;

console.log(score);

Output:

31
const

const creates variables that cannot be reassigned.

Example:

const score = 10;

score = 31;

console.log(score);

This will produce an error because the value cannot be changed.

Data Types

JavaScript has different primitive data types:

String
Number
Boolean
Null
Undefined

Example:

const name = "John";
const age = 10;
const rating = 6.5;
const isCool = true;
const x = null;
const y = undefined;
let z;

console.log(typeof name);
String Methods
Concatenation

Combining strings together:

const text = "My name is " + name + " and my age is " + age;

console.log(text);
Template Strings

A modern way to combine strings:

const text = `My name is ${name} and I am ${age}`;

console.log(text);
Common String Methods
split()

Splits a string into an array:

const s = "hello world, network";

console.log(s.split(","));
toUpperCase()

Converts text to uppercase:

console.log(s.toUpperCase());
toLowerCase()

Converts text to lowercase:

console.log(s.toLowerCase());
substring()

Returns part of a string:

console.log(s.substring(0,5));
Arrays

An array stores multiple values inside one variable.

Example:

const cars = ["BMW", "Dacia", "Nissan", "Porsche"];

console.log(cars);
Array Methods

Add item:

cars.push("McLaren");

Add item at beginning:

cars.unshift("Kaka");

Remove last item:

cars.pop();

Find index:

console.log(cars.indexOf("Dacia"));

Check if it is an array:

console.log(Array.isArray(cars));
Objects

Objects store data using key-value pairs.

Example:

const person = {
    firstName: "John",
    lastName: "Adolf",
    age: 10,
    hobbies: ["sport", "reading"],
    address: {
        city: "New York",
        state: "Bark",
        street: "51 Highway"
    }
};

console.log(person.address.city);
Destructuring

Extract values from objects:

const {firstName, lastName, address} = person;

console.log(firstName);
Arrays of Objects

Example:

const todos = [
{
    id: 1,
    text: "pray",
    isCompleted: true
},
{
    id: 2,
    text: "meeting",
    isCompleted: true
},
{
    id: 3,
    text: "walk",
    isCompleted: true
}
];
Looping Through Arrays
For...of
for(let todo of todos){
    console.log(todo.text);
    console.log(todo.id);
}
Array Methods
forEach()

Runs a function for every item:

todos.forEach(function(todo){
    console.log(todo.text);
});
map()

Creates a new array:

const todoText = todos.map(function(todo){
    return todo.text;
});
filter()

Filters values based on a condition:

const completed = todos.filter(function(todo){
    return todo.isCompleted === true;
});
Conditional Statements
if Statement
if(x === 10 || y > 15){
    console.log("Condition is true");
}
Switch Statement

Used when comparing multiple values:

switch(color){

case "blue":
    console.log("color is blue");
    break;

case "red":
    console.log("color is red");
    break;

default:
    console.log("unknown color");
}
Prototypes and Classes
Constructor Function
function Person(firstName,lastName,dOB){

this.firstName = firstName;
this.lastName = lastName;
this.dOB = new Date(dOB);

}
Classes

A simpler way to create objects:

class Person{

constructor(firstName,lastName,dOB){

this.firstName = firstName;
this.lastName = lastName;
this.dOB = new Date(dOB);

}

getBirthday(){

return this.dOB.getFullYear();

}

getFullname(){

return `${this.firstName} ${this.lastName}`;

}

}

Example:

const person1 = new Person(
"Pepe",
"Kaka",
"9-9-2000"
);

console.log(person1.getFullname());
 
 
 
 
 
 
 























































































     returne todo.Text 
