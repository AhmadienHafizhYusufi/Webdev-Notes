## Basic Array Methods

### `array.push(value)`

**Adds** a new element to the end of the array.

```js
const names = ["Jon", "Bob", "David"];
names.push("Mark");
console.log(names); // ["Jon", "Bob", "David", "Mark"]
```

### `array.pop()`

**Removes** the last element of an array and returns it.

```js
const lastElement = names.pop();
console.log(lastElement); // "Mark"
console.log(names); // ["Jon", "Bob", "David"]
```

### `array.shift()`

**Removes** the first element of an array and returns it.

```js
const firstElement = names.shift();
console.log(firstElement); // "Jon"
console.log(names); // ["Bob", "David"]
```

### `array.unshift(value)`

**Adds** a new value to the start of an array and returns the new length.

```js
names.unshift("Dean");
console.log(names); // ["Dean", "Bob", "David"]
```

### `array.splice(start, deleteCount, ...items)`

**Adds** or **removes** elements from any position in an array.

```js
names.splice(1, 0, "Jenny");
console.log(names); // ["Dean", "Jenny", "Bob", "David"]
```

### `array.slice(start, end)`

**Creates** a new array containing elements from the start index up to, but not
including, the end index.

```js
const slicedNames = names.slice(1, 3);
console.log(slicedNames); // ["Jenny", "Bob"]
```

#### Summary

Here's a code block that demonstrates these basic methods:

```js
const names = ["Jon", "Bob", "David", "Mark"];

// Array Push - Adds a new value to the end of the array.
names.push("Dean");
console.log(names); // ["Jon", "Bob", "David", "Mark", "Dean"]

// Array Pop - Deletes the last element of an array
const lastElement = names.pop();
console.log(lastElement); // "Dean"
console.log(names); // ["Jon", "Bob", "David", "Mark"]

// Array Shift - Deletes the first element of an array
const firstElement = names.shift();
console.log(firstElement); // "Jon"
console.log(names); // ["Bob", "David", "Mark"]

// Array Unshift - Adds a new value to the start of an array
names.unshift("Dean");
console.log(names); // ["Dean", "Bob", "David", "Mark"]

// Array Splice - It adds/removes values from any position of an array
names.splice(2, 0, "Jenny", "Johnny");
console.log(names); // ["Dean", "Bob", "Jenny", "Johnny", "David", "Mark"]

// Array Slice - Copies certain parts of an array into a newly created array
const slicedNames = names.slice(1, 3);
console.log(slicedNames); // ["Bob", "Jenny"]
```
