# Arrow Functions

**In this lesson, you'll learn about** arrow functions in JavaScript, which
provide a modern and concise way to define functions.

## Arrow Functions

Arrow functions have a **key difference** from **"normal" functions** : they do
not create their own `this` value.

The `this` **keyword** is a special JavaScript reserved keyword, which we'll
explain in more detail later. For now, just know that arrow functions
**inherit** `this` from their **surrounding context**. In most cases, this
behavior is beneficial, so you'll often see arrow functions used in JavaScript
code.

Here's how you can declare a function using **arrow function syntax**:

```javascript
const square = (number) => {
  return number * number;
};
```

## Concise Arrow Function Syntax

Arrow functions also have a shorter and more concise version. Whenever a
function consists of a single `return statement`, you can write it in one line:

```javascript
const square = (number) => number * number;
```

## Characteristics of Arrow Functions

- **Conciseness**: Arrow functions are concise and are often used for
  one-liners.
- `this` **Context**: Arrow functions do not have their own `this` context.
  Instead, they inherit `this` from the closest non-arrow function. This
  behavior is similar to using a variable or argument that exists in a function
  above.

Practically, this means that people use **arrow functions** when they want to
maintain the same `this` **context** as the surrounding code.

Arrow functions are a **powerful tool** in JavaScript, especially when you want
to **write clean and concise code**. As you become more familiar with them,
you'll find them to be an invaluable part of your JavaScript toolkit.
