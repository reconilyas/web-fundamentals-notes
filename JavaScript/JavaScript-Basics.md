# JavaScript Basics

## What is JavaScript?

JavaScript is a high-level programming language used to create interactive and dynamic web applications.

It can be used in:

- Frontend (Client-side)
- Backend (Server-side) using environments such as Node.js

JavaScript allows developers to:

- Create interactive web pages
- Handle application logic
- Process and manipulate data

---

# Variables

JavaScript has three main keywords for declaring variables:

- `var`
- `let`
- `const`

---

## var

`var` is the older way to declare variables.

Characteristics:

- Function-scoped
- Can be redeclared
- Mostly replaced by `let` and `const` in modern JavaScript

Example:

```javascript
var name = "John";

console.log(name);
let

let allows values to be changed after declaration.

Example:

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

Output:

Error

The value cannot be changed after declaration.

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

Splits a string into an array.

const s = "hello world, network";

console.log(s.split(","));
toUpperCase()

Converts text to uppercase.

console.log(s.toUpperCase());
toLowerCase()

Converts text to lowercase.

console.log(s.toLowerCase());
substring()

Returns a part of a string.

console.log(s.substring(0,5));
Arrays

An array stores multiple values inside one variable.

Example:

const cars = [
    "BMW",
    "Dacia",
    "Nissan",
    "Porsche"
];

console.log(cars);
Array Methods
Add Item
cars.push("McLaren");
Add Item at Beginning
cars.unshift("Kaka");
Remove Last Item
cars.pop();
Find Index
console.log(cars.indexOf("Dacia"));
Check if Value is an Array
console.log(Array.isArray(cars));
Objects

Objects store data using key-value pairs.

Example:

const person = {

    firstName: "John",

    lastName: "Adolf",

    age: 10,

    hobbies: [
        "sport",
        "reading"
    ],

    address: {

        city: "New York",

        state: "Bark",

        street: "51 Highway"

    }

};

console.log(person.address.city);
Destructuring

Destructuring allows extracting values from objects.

Example:

const {
    firstName,
    lastName,
    address
} = person;

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
for...of Loop
for(let todo of todos){

    console.log(todo.text);

    console.log(todo.id);

}
Array Methods
forEach()

Runs a function for every item.

todos.forEach(function(todo){

    console.log(todo.text);

});
map()

Creates a new array from existing values.

const todoText = todos.map(function(todo){

    return todo.text;

});
filter()

Filters values based on a condition.

const completed = todos.filter(function(todo){

    return todo.isCompleted === true;

});
Conditional Statements
if Statement
if(x === 10 || y > 15){

    console.log("Condition is true");

}
switch Statement

Used when comparing multiple values.

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

Constructor functions create objects.

Example:

function Person(firstName,lastName,dOB){

    this.firstName = firstName;

    this.lastName = lastName;

    this.dOB = new Date(dOB);

}
Classes

Classes provide a cleaner way to create objects.

Example:

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
Creating an Object

Example:

const person1 = new Person(
    "Pepe",
    "Kaka",
    "9-9-2000"
);

console.log(person1.getFullname());
Key Takeaways
JavaScript is used for both frontend and backend development.
Variables can be declared using var, let, and const.
Arrays store multiple values.
Objects store data using key-value pairs.
Array methods such as map(), filter(), and forEach() help process data.
Classes and constructors help create reusable objects.
Understanding JavaScript is important for web security because many web vulnerabilities involve JavaScript logic and client-side behavior.
