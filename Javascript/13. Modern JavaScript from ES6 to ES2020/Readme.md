# ES6+ What you already know

**In this lesson, you'll explore** some of the key features introduced in
**ES6**, also known as **ECMAScript 6**. These features have significantly
enhanced JavaScript, making it more powerful and easier to work with. Let's dive
into what **ES6** brought to the table and how you're already using these
features in your code.

## What is ES6?

**ECMAScript 6**, or simply **ES6**, is the 6th edition of the ECMAScript
standard, which specifies the core features of JavaScript. Released in 2015,
**ES6** introduced a host of **new features** that have become essential for
modern JavaScript development. Think of **ES6** as a **major update** to
JavaScript, similar to a significant update to your favorite software or game.

## Key Features of ES6

### `const` & `let`

You're already a master at these! From the first lecture, you've been using
`const` and `let` to declare variables. Before ES6, JavaScript only had `var`,
which could lead to issues with variable re-declaration and scope. `let` and
`const` provide better control over variable **scope** and **immutability**.

**var & let**

```javascript
var age = 27;
console.log(age); // 27
var age = 28;
console.log(age); // 28

let age = 27;
console.log(age); // 27
let age = 28; // SyntaxError: Identifier 'age' has already been declared
```

**const**

```javascript
const password = "123123";
password = "123456"; // TypeError: Assignment to constant variable

let password = "123123";
password = "123456"; // Allowed
```

### Arrow Functions

Arrow functions provide a **concise syntax** for writing functions. You've used
them extensively throughout the course.

```javascript
function multiply(x) {
  return x * x;
}

// Arrow function
const multiply = (x) => x * x;
```

### Default Parameters

Default parameters allow you to **set default values** for function
**parameters**, making your functions more robust and easier to use.

```javascript
const add = (x = 1, y = 2, z = 10) => {
  return x + y + z;
};

console.log(add(10, 3)); // 23
```

### Template Strings

Template strings, or **template literals**, allow you to embed expressions
within strings using backticks (``) and ($) syntax. This makes **string
interpolation** much easier and more **readable**.

```javascript
const customer = "John";
const order = { name: "iPad", price: 1400 };

const customer = "John";
const order = {
  name: "iPad",
  price: 1400,
};

// Old way
const message =
  "Hello " +
  customer +
  ", do you want to buy an " +
  order.name +
  " for " +
  order.price +
  " bucks?";

// New way with template strings
const message = `Hello ${customer}, do you want to buy an ${order.name} for ${order.price} bucks?`;
```

## Conclusion

These **ES6 features** have transformed JavaScript into a more **modern** and
**efficient** language. By using `const` and `let`, **arrow functions**,
**default parameters**, and **template strings**, you can write **cleaner**,
more **maintainable** code. As you continue to develop your JavaScript skills,
these features will become second nature, enhancing your ability to build
**powerful applications**.
