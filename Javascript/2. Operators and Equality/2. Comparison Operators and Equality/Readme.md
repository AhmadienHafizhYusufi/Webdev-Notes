# Comparison Operators and Equality

**In this lesson, you'll learn** how to use `comparison operators` in JavaScript
to compare values and understand the concept of **equality**, including the
differences between **strict** and loose **equality**.

## Comparison Operators and Equality

As you've already learned about **arithmetic** operators, **comparison**
operators work similarly in that they are fundamental tools in programming.
You've most likely heard of operators like greater than `>`, less than `<`, or
equal to `==`.

**Comparison operators** compare two values and return a **boolean** value:
`true` or `false`. This is the main takeaway: the return value of a comparison
operator is always a **boolean**.

The topic of **equality** in JavaScript is closely connected to comparison
operators. We'll cover both topics in this lesson. Let's start with an example
using two numbers:

```javascript
// Comparison Operators Demo in JavaScript

const x = 10;
const y = 5;
const z = "10"; // A string with the same value as x

// Greater than (>)
console.log("Is x > y? ", x > y); // true (10 is greater than 5)

// Greater than or equal to (>=)
console.log("Is x >= y? ", x >= y); // true (10 is greater than 5)

// Less than (<)
console.log("Is y < x? ", y < x); // true (5 is less than 10)

// Less than or equal to (<=)
console.log("Is y <= x? ", y <= x); // true (5 is less than 10)

// Loose equality (==) - Compares values, but ignores types
console.log("Is x == z? ", x == z); // true (10 == "10" because == allows type conversion)

// Strict equality (===) - Compares both value and type
console.log("Is x === z? ", x === z); // false (10 is a number, "10" is a string)

// Loose inequality (!=) - Checks if values are different, ignoring type
console.log("Is x != z? ", x != z); // false (10 == "10" due to type coercion)

// Strict inequality (!==) - Checks if values OR types are different
console.log("Is x !== z? ", x !== z); // true (10 is a number, "10" is a string)
```

Everything we've covered so far is straightforward. The key point to remember is
that **comparison operators always return a boolean value**.

The only aspect that requires a deeper look is the difference between:
**strict** `===`, `!==` and **loose** `==`, `!=` equality.

Understanding when to use each is crucial, and we'll explore that in the next
lesson!
