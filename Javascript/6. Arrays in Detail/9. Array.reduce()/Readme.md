# Array.reduce()

**In this lesson, you'll learn about** the `array.reduce()` method in
JavaScript, which is used to **reduce an array to a single value** by iterating
over its elements and applying a function.

## Array.reduce()

The `reduce()` method starts with **all the elements** from an array, **iterates
over them**, and computes them to **a single value** . It's one of the more
complex array methods, but it's incredibly powerful for tasks like **summing
numbers** , **finding maximum values** , and more.

### Example: Calculating Total Price

Let's say we have a grocery list with all the groceries we want to buy, along
with their prices:

```javascript
const groceryList = [29, 12, 45, 35, 87, 110];
```

We want to calculate the total price of all the items. This is a perfect example
for the `reduce` method.

#### Using `forEach` to Sum Prices

Here's how you might solve this with a `forEach` loop:

```javascript
const groceryItems = [29, 12, 45, 35, 87, 110];

let total = 0;
groceryItems.forEach((item) => (total += item));

console.log(total); // 318
```

While this works, it requires an **external variable** to keep track of the
total.

#### Using `reduce` to Sum Prices

Now, let's use the `reduce` method to achieve the same result **without an
external variable**:

```javascript
const groceryItems = [29, 12, 45, 35, 87, 110];

const total = groceryItems.reduce((accumulator, currentValue) => {
  return accumulator + currentValue;
}, 0);

console.log(total); // 318
```

## How `reduce()` Works

- **Accumulator**: The initial value (in this case, `0`) that accumulates the
  results of the function.
- **CurrentValue**: The current element being processed in the array.

The `reduce` method takes two arguments:

- A callback function that runs for each element in the array.
- The initial value of the accumulator.

The result of the `reduce` method is always a **single value**. In this example,
that value is the total of all item prices.

### Example: Sum of Numbers

Here's another example where we calculate the sum of numbers in an array:

```javascript
const numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];

const sum = numbers.reduce((accumulator, currentValue) => {
  return accumulator + currentValue;
}, 0);

console.log(sum); // 55
```

### Understanding the Process

```javascript
const numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];

// a = 0, c = 1 => a = 1
// a = 1, c = 2 => a = 3
// a = 3, c = 3 => a = 6
// ...

const sum = numbers.reduce((accumulator, currentValue) => {
  return accumulator + currentValue;
}, 0);

console.log(sum); // 55
```

## Simplifying with ES6

You can simplify the `reduce` function using `ES6` syntax for an instant return:

```javascript
const sum = numbers.reduce(
  (accumulator, currentValue) => accumulator + currentValue
);
console.log(sum); // 55
```

### Exercise: Find Maximum Value

Here's an exercise to find the maximum value in an array:

```javascript
const values = [5, 2, 3, 1, 2];

const findMax = (acc, val) => (val > acc ? val : acc);

const maximumNumber = values.reduce(findMax);

console.log(maximumNumber); // 5
```

The `array.reduce()` method is a versatile tool for **aggregating data**, making
it an essential part of functional programming in JavaScript.
