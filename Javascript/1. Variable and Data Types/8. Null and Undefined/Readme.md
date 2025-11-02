# Null and Undefined

**Learning Objective**: Differentiate between `null` and `undefined` values and
understand their unique roles in JavaScript.

## What is `null`?

`null` is a **special value** in JavaScript used to represent “nothing,”
“empty,” or “value unknown.” It is **intentionally set** by a programmer to
indicate that a variable should have no value.

## Example: Assigning `null`

```javascript
let age = null; // This means "age is unknown or empty."
console.log(age); // null
```

Key Points:

- null is a primitive value in JavaScript.
- It is not an object (although typeof null returns "object" due to a historical
  quirk).

## What is `undefined`?

`undefined` is the default value for variables that **have been declared but not
assigned a value**.

## Example: Uninitialized Variables

```javascript
let x; // No value assigned
console.log(x); // undefined
```

## Can you assign undefined?

While it’s technically possible, it’s not recommended to assign `undefined`
manually. Use `null` for this purpose instead.

```javascript
let x = 123;
x = undefined; // Not recommended
console.log(x); // undefined
```

## Key Differences Between null and undefined

| **Feature**     | **NULL**                             | **UNDEFINED**                              |
| --------------- | ------------------------------------ | ------------------------------------------ |
| **Purpose**     | Represents “no value” (intentional). | Default value for uninitialized variables. |
| **Assigned By** | Programmer.                          | JavaScript.                                |
| **Type**        | `object` (JavaScript quirk).         | `undefined` (its own type).                |

## Understanding the Behavior

1. `undefined` means a variable exists but doesn’t have a value:

```javascript
let name; // Declared but not assigned
console.log(name); // undefined
```

2. `null` means the variable intentionally has no value:

```javascript
let name = null; // Explicitly set to "no value"
console.log(name); // null
```

3. They are not strictly equal:

```javascript
console.log(null === undefined); // false
```

4. But they are loosely equal:

```javascript
console.log(null == undefined); // true
```

## Using typeof to Inspect Types

You can inspect the type of any value using `typeof`:

```javascript
let empty = null;
let notSet;

console.log(typeof empty); // "object" (a JavaScript quirk!)
console.log(typeof notSet); // "undefined"
```

## Interactive Activity

1. Open **VS Code** and create a file called `null-vs-undefined.js`.
2. Write the following:
   - Declare a variable with `null` to represent “no value.”
   - Declare another variable without assigning a value to make it `undefined`.
   - Use `typeof` to inspect the type of both variables.
   - Log the results to the console.

Example:

```javascript
let empty = null; // null value
let notSet; // undefined

console.log(empty); // null
console.log(typeof empty); // "object"

console.log(notSet); // undefined
console.log(typeof notSet); // "undefined"
```

1. Change the value of the `null` variable to something else and observe the
   changes.

## What’s Next?

In this lesson, you learned the difference between `null` and `undefined`. These
concepts are foundational for debugging and writing clear, intentional code.
Practice working with them, and don’t forget to explore their behavior using
`typeof`!

Next, we’ll explore objects, a key data type in JavaScript that enables you to
store and manage collections of data. Let’s keep going! 🚀
