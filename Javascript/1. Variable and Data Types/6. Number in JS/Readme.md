# Numbers in JS

**Learning Objective**: Understand JavaScript’s flexible number handling and how
to work with basic numbers.

## What Are Numbers in JavaScript?

Numbers are a fundamental data type in JavaScript. Unlike some programming
languages, you don’t need to specify whether a number is an **integer** or a
**float**—JavaScript takes care of it for you. This is because JavaScript is
**dynamically typed**.

## Example: Dynamically Typed Numbers

In JavaScript:

```javascript
const wholeNumber = 5; // Integer
const decimalNumber = 3.14; // Float
```

In other languages like C, you would need to explicitly declare the type:

```c
int wholeNumber = 5;
float decimalNumber = 3.14;
```

In JavaScript, both integers and decimals fall under the same `number` type,
simplifying how we work with them.

## Basic Math Operations

You can perform all the standard math operations in JavaScript, such as
addition, subtraction, multiplication, and division.

### Examples:

```javascript
const a = 10;
const b = 5;

console.log(a + b); // Addition: 15
console.log(a - b); // Subtraction: 5
console.log(a * b); // Multiplication: 50
console.log(a / b); // Division: 2
```

## What About NaN?

`NaN`, short for **Not a Number**, is a special numeric value in JavaScript. It
often occurs when you try to perform an invalid mathematical operation.

### Examples:

```javascript
console.log("hello" * 3); // NaN
```

Interestingly, even though `NaN` stands for "Not a Number," its type is still
`number`:

```javascript
console.log(typeof NaN); // "number"
```

Why? In computing, `NaN` is technically part of the numeric type system, even
though it doesn’t represent a valid number.

## Advanced Number Operations

We’re keeping it simple for now, but JavaScript also has operators for more
advanced calculations, like modulus `%`, exponentiation `**`, and more.

You’ll learn about these in detail in the upcoming module, **Operators and
Equality**, where we’ll explore:

- Arithmetic operators
- Logical operators
- Assignment operators
- Comparison and equality

For now, focus on getting comfortable with basic numbers and operations.

## Interactive Activity

Let’s put this into practice:

1. Open **VS Code** and create a new file called `numbers.js`.
2. Try the following:
   - Declare variables for:
     - A whole number (e.g., your lucky number).
     - A decimal number (e.g., a measurement or value like 3.14).
   - Perform addition, subtraction, multiplication, and division with these
     numbers.
   - Log the results to the console.

Example:

```javascript
const whole = 7;
const decimal = 3.14;

console.log(whole + decimal); // Addition
console.log(whole - decimal); // Subtraction
console.log(whole * decimal); // Multiplication
console.log(whole / decimal); // Division
```

## What’s Next?

You’ve just learned the basics of working with numbers in JavaScript. Keep
practicing, as numbers are a key part of programming. In the next lesson, we’ll
explore **Booleans**, which will help us add logic and decisions to our
programs.
