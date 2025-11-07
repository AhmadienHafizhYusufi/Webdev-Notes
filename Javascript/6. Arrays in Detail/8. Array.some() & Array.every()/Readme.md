# Array.some() & Array.every()

**In this lesson, you'll learn about** the `array.some()` and `array.every()`
methods in JavaScript, which are used to **test** whether some or all elements
in an array **pass a specified test**.

## Array.some()

The `some()` method tests whether **at least one element** in the array **passes
the test** implemented by the provided **function**. It returns `true` if the
callback function returns a truthy value for any array element; otherwise, it
returns `false`.

### Example: Checking for Even Numbers

Let's say we want to check if there are any even numbers in an array:

```javascript
var numbers = [1, 3, 5, 8, 9];

// Check if there is at least one even number
var hasEvenNumber = numbers.some(function (number) {
  return number % 2 === 0;
});

console.log(hasEvenNumber); // true
```

## Array.every()

The `every()` method tests whether **all elements** in the array **pass the
test** implemented by the provided **function**. It returns true if the callback
function returns a truthy value for every array element; otherwise, it returns
`false`.

### Example: Checking for All Positive Numbers

Let's say we want to check if all numbers in an array are positive:

```javascript
var numbers = [1, 3, 5, 8, 9];

// Check if all numbers are positive
var allPositive = numbers.every(function (number) {
  return number > 0;
});

console.log(allPositive); // true
```

## How They Work

- `some()`: Returns `true` if **at least one element** passes the test.
- `every()`: Returns `true` if **all elements** pass the test.

The `array.some()` and `array.every()` methods are powerful tools for
**evaluating conditions** across array elements, making them essential for data
validation and logic checks in JavaScript.
