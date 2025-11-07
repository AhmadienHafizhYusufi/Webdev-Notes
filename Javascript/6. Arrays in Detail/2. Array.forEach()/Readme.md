# Array.forEach()

**In this lesson, you'll learn about** the `array.forEach` method in JavaScript,
which is used to execute a function for each element in an array. This method
provides a cleaner and more readable alternative to the traditional `for` loop
for certain use cases.

## What is array.forEach method?

The `array.forEach` method performs an action for each element in the array.
While you can achieve the same result using a standard `for` loop, `forEach`
offers a more **concise** and **expressive** syntax.

Let's take an example where we need to **log** each value in an **array** called
`myArray` to the **console**, along with their respective **indices** . Here's
how we can do it using a standard `for` loop:

```javascript
let names = ["Jon", "Jenny", "Johnny"];

for (let i = 0; i < names.length; i++) {
  console.log(i, names[i]);
}

// Output:
// 0 'Jon'
// 1 'Jenny'
// 2 'Johnny'
```

In this case, we declare and initialize a variable `i`, and the loop compares it
with `array.length`. If the expression evaluates to `true`, the loop executes.
After the loop body is executed, the value of `i` increments by one.

**We can eliminate this process using the `array.forEach` method!**

## Syntax

Here is the syntax of the `array.forEach` method:

```javascript
array.forEach((value, index) => {
  // ...
});
```

The first argument of the `forEach` method is the function you want to execute
for each element of the array. This `callback function` can have **three
arguments**:

- The **value** of the current element
- The **index** of the current element
- The **array** itself

So, we can perform the same action using `forEach` in this manner:

```javascript
let names = ["Jon", "Jenny", "Johnny"];

names.forEach((value, index) => {
  console.log(index, value);
});
```

## Using a Named Function as a Callback

If you want to use a **named function** as a **callback**, it can be done like
this:

```javascript
function logArrayElement(element, index) {
  console.log(index, element);
}

names.forEach(logArrayElement);
```

## Return Value

This method returns `undefined` and is not chainable, meaning you can't call
another method on the array after using `forEach`. Therefore, you cannot use
cascading notation with `forEach`.

```javascript
let returnValue = names.forEach(function (value) {
  console.log(value);
});

console.log(returnValue); // undefined
```

## How to use it

**Use When:**

- The callback function is to be executed on **every single element** of the
  array.
- You want to **improve performance** (provided the first condition is
  satisfied).

**Don't Use When:**

- You want to **stop or break the loop when some condition is true**. For
  example, if you want to log elements of `myArray` but break the loop if the
  value of the current element is 3, you must use a standard `for` loop.
- The callback function is asynchronous. Instead, use the standard `for` loop.

## Example

Here is a real example where `array.forEach` can be used:

```javascript
let sum = 0;
const numbers = [65, 44, 12, 4];

numbers.forEach((number) => {
  sum += number;
});

console.log(sum); // 125
```

The `array.forEach` method is a powerful tool for iterating over arrays,
providing a clean and expressive way to perform actions on each element.
