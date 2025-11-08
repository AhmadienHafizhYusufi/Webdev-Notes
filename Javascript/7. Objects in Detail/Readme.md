# Objects Introduction

**In this lesson, you'll learn about** objects in JavaScript, which are
fundamental data structures used to **store collections of data** and more
complex entities.

## Objects Introduction

Objects are the most important **data type** and **building block** for modern
JavaScript. Unlike primitive data types (numbers, strings, booleans), which
store a single value, objects can store multiple values and more complex data.

Objects in JavaScript can be compared to real-life objects. For example,
consider a cup: it has properties like color, design, weight, and material.
Similarly, JavaScript objects have **properties** that define their
**characteristics**.

## What are Objects?

In simple terms, an **object is an unordered collection of related data in the
form of key-value pairs**.

## Creating an Object

```js
const person = {
  firstName: "John",
  lastName: "Doe",
  age: 25,
};
```

- **Curly Braces**: To create an object, use **curly braces** `{}` and assign it
  to a variable.
- **Key-Value Pairs**: Inside the object, define key-value pairs. For example,
  the key `firstName` has the value `'John'`.

## Unordered Nature of Objects

Objects are **unordered**, meaning the order of properties **can change** and
won't always stay the same as declared. This is perfectly fine because, with
**objects**, we focus on the **data** rather than the **order**.

## Nested Objects and Different Data Types

Values in an object can be of **any type**, including other objects. For
example, if our `person` has a `car`, the car can be an object with its own
properties:

```js
const person = {
  firstName: "John",
  lastName: "Doe",
  age: 25,
  car: {
    year: 2015,
    color: "Red",
  },
};
```

This demonstrates that we can **nest objects within other objects**.

## Using Variables as Values

We can also use **variables as values** in an object. A variable is essentially
a **container** for a value, so we can do the following:

```js
const firstName = "Johnny";

const person = {
  firstName: firstName,
};

console.log(person); // { firstName: 'Johnny' }
```

## Shorthand Property Names

If the **key** and **value** have the **same name**, JavaScript allows us to use
shorthand syntax:

```js
const person = {
  firstName,
};

console.log(person); // { firstName: 'Johnny' }
```

This shorthand makes the code **cleaner** and **easier** to read.

Objects are a versatile and powerful feature in JavaScript, enabling you to
**model complex data** and **relationships** in your applications.
