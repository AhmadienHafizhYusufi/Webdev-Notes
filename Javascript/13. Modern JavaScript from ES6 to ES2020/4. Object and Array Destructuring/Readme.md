## Destructuring Arrays

Destructuring arrays allows you to **extract values** from an array and
**assign** them to variables in a **single**, **concise statement**. This is
particularly useful when you want to work with specific elements of an array
without manually accessing each index.

### Basic Array Destructuring

Instead of accessing each element **individually**, you can use destructuring to
**extract values**:

```javascript
let introduction = ["Hello", "I", "am", "Sarah"];
let [greeting, pronoun] = introduction;

console.log(greeting); // "Hello"
console.log(pronoun); // "I"
```

### Declaring Variables Before Assignment

You can declare variables **before assigning** them values from an array:

```javascript
let greeting, pronoun;
[greeting, pronoun] = ["Hello", "I", "am", "Sarah"];

console.log(greeting); // "Hello"
console.log(pronoun); // "I"
```

### Skipping Items in an Array

You can **skip elements** in an array by using commas `,`:

```javascript
let [greeting, , , name] = ["Hello", "I", "am", "Sarah"];
console.log(greeting); // "Hello"
console.log(name); // "Sarah"
```

### Assigning the Rest of an Array

You can use the rest syntax to **collect remaining elements** into an array:

```javascript
let [greeting, ...intro] = ["Hello", "I", "am", "Sarah"];
console.log(greeting); // "Hello"
console.log(intro); // ["I", "am", "Sarah"]
```

### Using Default Values

Default values can be **assigned to variables** if the array element is
**undefined**:

```javascript
let [greeting = "Hi", name = "Sarah"] = ["Hello"];
console.log(greeting); // "Hello"
console.log(name); // "Sarah"
```

## Destructuring Objects

Destructuring objects allows you to **extract properties from an object and
assign them to variables**. This is useful for working with objects where you
only need specific properties.

### Basic Object Destructuring

```javascript
let user = { name: "Alice", age: 25 };
let { name, age } = user;

console.log(name); // "Alice"
console.log(age); // 25
```

### Renaming Variables

You can \*\*rename variables while destructuring:

```javascript
let { name: userName, age: userAge } = user;
console.log(userName); // "Alice"
console.log(userAge); // 25
```

### Using Default Values

You can **assign default values** to variables if the property does not exist:

```javascript
let { name, isAdmin = false } = { name: "Alice" };
console.log(isAdmin); // false
```

## Destructuring in Function Parameters

Destructuring can be used directly in function parameters to **extract values**
from **objects** or **arrays** passed as **arguments**.

```javascript
function displayUser({ name, age }) {
  console.log(`Name: ${name}, Age: ${age}`);
}

let user = { name: "Bob", age: 30 };
displayUser(user); // Name: Bob, Age: 30
```
