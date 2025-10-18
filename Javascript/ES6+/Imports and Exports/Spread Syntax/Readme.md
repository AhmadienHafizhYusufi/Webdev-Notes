## Spread Syntax

Spread syntax allows you to expand elements of an iterable (like an array or
string) in places where multiple arguments or elements are expected.

- The **spread syntax** `...` allows you to **expand an iterable into individual
  elements**.
- It is the **opposite** of rest syntax, which **collects multiple elements into
  a single array**.
- Spread syntax can be used in **function calls**, **array literals**, and
  **object literals**.

### Using Spread in Function Calls

Spread syntax can replace `Function.prototype,apply()` to pass array elements as
arguments to a function.

```javascript
function add(x, y, z) {
  return x + y + z;
}

const numbers = [1, 2, 3];

console.log(add(...numbers)); // Expected output: 6
```

### Using Spread in Array Literals

Spread syntax allows you to **create new arrays** by expanding elements from
existing arrays.

```javascript
const parts = ["shoulders", "knees"];
const lyrics = ["head", ...parts, "and", "toes"];
console.log(lyrics); // ["head", "shoulders", "knees", "and", "toes"]
```

## Copying and Concatenating Arrays

Spread syntax can be used to **make shallow copies** of arrays or
**concatenate** multiple arrays.

```javascript
const arr1 = [0, 1, 2];
const arr2 = [3, 4, 5];

const combined = [...arr1, ...arr2];
console.log(combined); // [0, 1, 2, 3, 4, 5]
```

## Using Spread in Object Literals

Spread syntax can also be used to **copy** and **merge objects**.

```javascript
const obj1 = { foo: "bar", x: 42 };
const obj2 = { bar: "baz", y: 13 };

const mergedObj = { ...obj1, ...obj2 };
console.log(mergedObj); // { foo: "bar", x: 42, bar: "baz", y: 13 }
```
