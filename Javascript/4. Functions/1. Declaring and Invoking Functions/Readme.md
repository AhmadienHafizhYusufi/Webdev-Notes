# Declaring and Invoking Functions

**In this lesson, you'll learn about** declaring and invoking functions in
JavaScript, which are essential for structuring and executing code efficiently.

## Declaring and Invoking Functions

As we learned in the last section, functions are **subprograms** designed to
perform a particular task.

The code of the function is executed when the function is called. This is known
as **invoking** a function. Let's first revisit the process of **creating** or
**defining** a function.

There are a few different ways to define a function in JavaScript:

## Function Declaration

A **Function Declaration** defines a named function. To create a function
declaration, you use the `function` keyword followed by the name of the
function.

```javascript
function name(parameters) {
  // statements
}
```

## Function Expression

A **Function Expression** defines a named or anonymous function. An anonymous
function is a function that has no name. In the example below, we are setting
the anonymous function object equal to a variable.

```javascript
let name = function (parameters) {
  // statements
};
```

## Arrow Function Expression

An **Arrow Function Expression** is a shorter syntax for writing function
expressions.

```javascript
const name = (parameters) => {
  // statements
};
```

**Arrow functions** are the most modern way to create JavaScript functions. For
that reason, we're going to explore them in much more detail in the upcoming
lessons! 😊

## Invoking a Function

Functions execute when they are called. This process is known as `invocation`.
You can invoke a function by referencing the function name, followed by an open
and closed parenthesis: `( )`.

Let's explore an example.

First, we’ll **define** a function named `sayHi`. This function will take one
**parameter**, `name`. When executed, the function will **log** that `name` back
to the **console**:

```javascript
function sayHi(name) {
  console.log(`Hi, ${name}`);
}
```

To `invoke` our function, we **call it** while passing in the singular
**argument**. Here I am calling this function with the name `Joe`:

```javascript
sayHi("Joe"); // Hi, Joe
```

Notice how we got back the **console log**, but we also got back `undefined`.
Why is that? That is connected to the **return** of the function. If a function
does not explicitly **return** a value, it **returns** `undefined` by default.
We'll explore this concept further in upcoming lessons.
