# Data Types

**Learning Objective**: Understand JavaScript’s data types and their
significance.

In the previous lecture, we talked about how we can store values in variables.
These values need to be in the form of one of JavaScript’s predefined **data
types**. If this sounds abstract—don’t worry! We’ll go through it step by step,
and by the end of this lesson, it’ll all make sense.

Think of data types as **different kinds of containers** that hold specific
types of information. JavaScript has two main categories of data types:

## 1. Primitive Data Types

These are the basic building blocks of data in JavaScript. Let’s break them down
with fun examples:

### a. Numbers

Numbers represent both whole numbers and decimals in JavaScript.

Example: Let’s say you’re counting the number of stars in the sky (simplified,
of course):

```javascript
const stars = 1000000; // A million stars!
const pi = 3.14; // A decimal value for mathematical calculations.
```

### b. Strings

Strings are sequences of characters enclosed in quotes. Think of them as text.

Example: Imagine you’re sending a message:

```javascript
const message = "Hello, world!";
```

### c. Boolean

Booleans represent yes/no, true/false values. They’re super useful for
decision-making in code.

Example: Are the cookies baked?

```javascript
const isBaked = true; // Yes, they’re ready!
const isBurnt = false; // Thankfully, not burnt.
```

### d. Null

`Null` represents the absence of a value. It’s like an empty container.

Example: You’ve reserved a table at a restaurant, but the details aren’t
finalized yet:

```javascript
let reservation = null; // No table assigned yet.
```

### e. Undefined

`Undefined` means a variable has been declared but not given a value yet.

Example: Imagine writing a note, but forgetting to fill in the details:

```javascript
const id = Symbol("uniqueID");
console.log(id); // Symbol(uniqueID)
```

## 2. Complex Data Type: Objects

Objects are the most important data type in JavaScript and the foundation of
modern web development.

Think of an object as a collection of related data. For example:

```javascript
const person = {
  name: "James Bond",
  age: 007,
  car: {
    make: "Aston Martin",
    model: "DBS",
    year: 1969,
  },
};
```

You can access specific properties using dot notation:

```javascript
console.log(person.car.make); // Aston Martin
```

## Arrays: Special Objects

Arrays are a type of object that store ordered lists of items.

Example: Imagine listing your favorite movies:

```javascript
const movies = ["Casino Royale", "Skyfall", "Spectre"];
console.log(movies[1]); // Skyfall
```

Arrays are perfect for keeping track of collections like shopping lists, to-do
tasks, or top-secret missions.

## How to Identify Data Types

You can easily check the data type of a value using the `typeof` operator. This
is incredibly useful for debugging and understanding your variables.

Example:

```javascript
console.log(typeof 42); // "number"
console.log(typeof "Hello!"); // "string"
console.log(typeof true); // "boolean"
console.log(typeof null); // "object" (a JavaScript quirk!)
console.log(typeof undefined); // "undefined"
console.log(typeof person); // "object"
console.log(typeof movies); // "object"
```

## Interactive Activity

1. Open **VS Code** and create a new file called `dataTypes.js`.

2. Experiment by declaring variables for each data type:

- A number for your age.
- A string for your favorite movie or book quote.
- A Boolean for whether you’ve eaten lunch today.
- A `Null` value for a task you haven’t started yet.
- An array for your top three hobbies.

3. Use `console.log()` and typeof to check the data type of each variable.
   Example:

```javascript
const age = 25;
console.log(typeof age); // "number"
```

## What’s Next?

In the next lessons, we’ll explore each data type in greater detail. You’ll
learn how to work with strings, numbers, Booleans, and objects effectively. By
the end, you’ll have a solid foundation to build powerful programs.

So, go ahead—experiment with these examples, get comfortable with `typeof`, and
let’s dive deeper into JavaScript types.
