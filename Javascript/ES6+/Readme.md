## ES6+

**ECMAScript6** (**ES6**) is the 6th edition of the ECMAScript standard, which
specifies the core features of JavaScript. Here's some key features of ES6:

### `const` & `let`

**let** and **const** provide better control over variable scope and
immutability.

```javascript
var age = 27;
console.log(age); // 27
var age = 28;
console.log(age); // 28

let age = 27;
console.log(age); // 27
let age = 28; // SyntaxError: Identifier 'age' has already been declared

const password = "123123";
password = "123456"; // TypeError: Assignment to constant variable

let password = "123123";
password = "123456"; // Allowed
```

### Arrow Functions

Arrow functions provide a **concise syntax** for writing functions.

```javascript
function multiply(x) {
  return x * x;
}

// Arrow function
const multiply = (x) => x * x;
```

### Default Parameters

Default parameters allow you to **set default values** for function **parameters**.

```javascript
const add = (x = 1, y = 2, z = 10) => {
    return x + y + z;
}

console.log(add(10, 3)); // 23
```

### Template Strings

Template strings, or **template literals**, allow you to embed expressions within strings using backticks (``) and ($) syntax. This makes **string interpolation** much easier and more **readable**.

const customer = 'John';
const order = {
    name: 'iPad',
    price: 1400
};

```javascript
// Old way
const message = 'Hello ' + customer + ', do you want to buy an ' + order.name + ' for ' + order.price + ' bucks?';

// New way with template strings
const message = `Hello ${customer}, do you want to buy an ${order.name} for ${order.price} bucks?`;
```