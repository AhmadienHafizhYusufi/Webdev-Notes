# Array.map()

**In this lesson, you'll learn about** the `array.map()` method in JavaScript,
which is used to create a new array by applying a function to each element of an
existing array.

## Array.map()

The key difference between `array.map()` and `array.forEach()` is that the
`map()` method allocates memory to store and return a **new array**, while
`forEach()` **does not allocate** memory and returns `undefined`.

The `forEach()` method is used for executing a function on each array element
**without returning a new array**, whereas `map()` **returns a new array** with
the results of applying a function to each element.

When using `map()`, you can think of it as **iterating over each element** and
**transforming** it in some way, resulting in a **new array**.

## How to use

Let's consider a local shop's inventory:

```javascript
// A local shop's inventory
const inventory = [
  { price: 5, name: "eggs" },
  { price: 5, name: "ham" },
  { price: 5, name: "mayo" },
  { price: 5, name: "bread" },
];

// A customer asks for a list of all the inventory they have
const requestFullInventory = inventory.map((item) => item);

console.log(requestFullInventory); // requestFullInventory is filled with the inventory that we have
```

## How it works

- **Transformation**: The `map()` method applies a function to each element of
  the array, transforming it in some way.
- **New Array**: It returns a new array containing the transformed elements,
  leaving the original array unchanged.

The `array.map()` method is a powerful tool for **creating new arrays** based on
**transformations** of **existing arrays** , making it an essential part of
functional programming in JavaScript.
