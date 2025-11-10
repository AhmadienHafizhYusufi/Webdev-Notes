# Value vs Reference Introduction

**In this lesson, you'll learn about** the difference between **value** and
**reference** in JavaScript, which is crucial for understanding how data is
stored and manipulated in your programs.

## Value vs Reference Introduction

JavaScript differentiates data types into **two categories**:

- **Primitive values**: Number, String, Boolean, Null, Undefined, etc.
- **Complex values**: Objects, Arrays

Understanding how these types are **copied** and **manipulated** is key to
avoiding unexpected behavior in your code.

## Copying Primitive Values

When copying **primitive values**, JavaScript behaves as you might expect. The
value is copied directly, and changes to one variable do not affect the other.

**Copying Numbers**

```javascript
let x = 1;
let y = x;

x = 2;

console.log(x); // 2
console.log(y); // 1
```

**Copying Strings**

```javascript
let firstPerson = "Mark";
let secondPerson = firstPerson;

firstPerson = "Austin";

console.log(firstPerson); // Austin
console.log(secondPerson); // Mark
```

In both cases, the original value is **copied**, and changes to the original
variable **do not affect** the copied variable.

## Copying Complex Values

When copying **complex values**, such as **objects** and **arrays**, JavaScript
behaves differently. Instead of copying the value, it copies a **reference** to
the value. This means changes to one variable **can affect the other** .

**Copying Arrays**

```javascript
const animals = ["dogs", "cats"];
const otherAnimals = animals;

animals.push("llamas");

console.log(animals); // ['dogs', 'cats', 'llamas']
console.log(otherAnimals); // ['dogs', 'cats', 'llamas']
```

**Copying Objects**

```javascript
const person = {
  firstName: "Jon",
  lastName: "Snow",
};

const otherPerson = person;

person.firstName = "JOHNNY";

console.log(person); // { firstName: 'JOHNNY', lastName: 'Snow' }
console.log(otherPerson); // { firstName: 'JOHNNY', lastName: 'Snow' }
```

In both examples, changes to the original array or object **also affect** the
copied variable. This is because both variables **reference the same**
underlying data.

## Conclusion

This behavior can be surprising if you're not expecting it, but it makes sense
once you understand that **complex values are stored as references**. In the
next lesson, we'll dive deeper into why this happens and how you can manage it
effectively in your code. Understanding the **difference between value and
reference** is essential for writing robust and predictable JavaScript programs.
