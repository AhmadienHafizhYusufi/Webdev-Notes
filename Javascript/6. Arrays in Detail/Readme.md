# Arrays Introduction

**In this lesson, you'll learn about** arrays in JavaScript, a fundamental data
structure used to store ordered collections of elements.

## Introduction `[ ]`

In programming, we often need an **ordered collection** where we have a 1st,
2nd, 3rd element, and so on. For example, we might need this **to store** a list
of **users, items, or elements**.

JavaScript provides a special data structure named **Array** `[ ]` to store
ordered collections.

## Declaration

This is how we declare an array, the most important part here is the **square
brackets** `[ ]`:

```javascript
const months = ["January", "February", "March", "April"];
```

Array elements are **numbered**, starting with **zero**.

## Accessing Elements

We can get an element by its **index** using **square brackets** `[ ]`:

```javascript
console.log(months[0]); // 'January'
```

## Modifying Elements

We can **replace** an element:

```javascript
months[2] = "Not March"; // [ 'January', 'February', 'Not March', 'April' ]
```

Or add a **new one** to the array:

```javascript
months[4] = "May"; // [ 'January', 'February', 'Not March', 'April', 'May' ]
```

## Array Length

The **total count** of the elements in the array is its `length`:

```javascript
console.log(months.length); // 5
```

## Storing Different Types

An array can store elements of **any type**:

```javascript
const arr = [
  "Apple",
  { name: "John" },
  true,
  function () {
    console.log("hello");
  },
];
```

## Looping Through Arrays

You'll often need to **loop** through all the **elements** of an array. That's
where the `for` loop comes in handy:

```javascript
for (let i = 0; i < months.length; i++) {
  console.log(months[i]);
}
```

Later, we'll dedicate a few lessons to different built-in `array methods` for
**looping**. These methods allow us to loop faster, with added functionality and
less code. `Arrays` are a powerful tool in JavaScript, enabling you to
**manage** collections of data efficiently.
