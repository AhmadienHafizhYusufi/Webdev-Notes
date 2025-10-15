## Hoisting

`Hoisting` is a JavaScript mechanism where **variables** and **function**
declarations are moved to the top of their **scope** before code execution.

### Variable Hoisting

In JavaScript, an undeclared variable is assigned the value `undefined` at
execution and is also of type `undefined`.

```javascript
console.log(typeof name); // undefined
```

A `ReferenceError` is thrown when trying to access a **previously undeclared
variable**.

```javascript
console.log(name); // ReferenceError: name is not defined
```

Key thing to note regarding **hoisting** is that only the **variable
declaration** is moved to the **top**, not the actual **value** assigned to the
variable.

```javascript
console.log(myString); // undefined
var myString = "test";
```

This is equivalent to:

```javascript
var myString;
console.log(myString); // undefined
myString = "test";
```

**Example 1:**

```javascript
var hoist;
console.log(hoist); // undefined
hoist = "The variable has been hoisted.";
```

Example 2:

```javascript
function hoist() {
  var message;
  console.log(message);
  message = "Hoisting is cool!";
}
hoist(); // undefined
```

#### Only Declarations are Hoisted

JavaScript only hoists **declarations**, not **initializations**. If a variable
is declared and initialized after using it, the value will be `undefined`.

```javascript
console.log(num); // undefined
var num;
num = 6;
```

To avoid this pitfall, always **declare** and **initialize** the variable before
using it:

```javascript
function hoist() {
  var message = "Hoisting is cool!";

  return message;
}

hoist(); // Hoisting is cool!
```

### Function Hoisting

Like `var` variables, **function declarations** are completely hoisted to the
top.

```javascript
hoisted(); // 'This function has been hoisted.'

function hoisted() {
  console.log("This function has been hoisted.");
}
```

- Again, would you ever need to do this? **No**.
- **Always declare the function before you call it**.

### Function Expressions

Function expressions, the more modern way of writing functions with the `const`
keyword, **are not hoisted**

```javascript
functionExpression(); // ReferenceError

const functionExpression = () => {
  console.log('Will this work?');
}
```