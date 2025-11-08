# Hoisting

**In this lesson, you'll learn about** `hoisting` in JavaScript, a mechanism
that affects how variables and functions are declared and accessed in your code.

## Hoisting

**Hoisting** is a JavaScript mechanism where **variables** and **function
declarations** are moved to the top of their **scope** before code execution.
This means that no matter where functions and variables are declared, they are
moved to the top of their scope, whether **global** or **local**.

## Variable Hoisting

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

**Example 2:**

```javascript
function hoist() {
  var message;
  console.log(message);
  message = "Hoisting is cool!";
}
hoist(); // undefined
```

## Only Declarations are Hoisted

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

The variable declaration, `var message`, whose scope is the function `hoist()`,
is hoisted to the top of the function.

- This section of the course is the only time you'll see me use older syntax
  like **function declarations** and the var keyword.
- **Why?** It shows that newer versions of JavaScript are moving away from this
  style. It's good to know that **hoisting** exists, but you should **never
  rely** on it.
- Always declare variables exactly where they should be: **at the top of the
  scope they're used in**.
- This ensures your code is **predictable** and doesn't rely on hoisting.

`let` and `const` are also hoisted, but you cannot access them before the actual
declaration is evaluated at runtime. What does this mean? Let's see it in a
**simple example**:

```javascript
console.log(myVarString); // undefined
var myVarString = "var";

console.log(myLetString); // ReferenceError
let myLetString = "let";

console.log(myConstString); // ReferenceError
const myConstString = "const";
```

With `let` and `const`, you get exactly what you would expect: a
`reference error`. This is JavaScript's way of encouraging **clean code**.

**You should always declare variables before using them**.

## Function Hoisting

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

## Function Expressions

Function expressions, the more modern way of writing functions with the `const`
keyword, **are not hoisted**

```javascript
functionExpression(); // ReferenceError

const functionExpression = () => {
  console.log("Will this work?");
};
```

`Hoisting`, like `closures` (which we'll discuss in the next lesson), are complex topics. They might not be useful in everyday coding, but understanding them is important for **technical interviews**. If you stick to good programming habits, you won't encounter **hoisting** or **closures** often. However, knowing about these "tricky concepts" can be beneficial, especially in **interview scenarios**.