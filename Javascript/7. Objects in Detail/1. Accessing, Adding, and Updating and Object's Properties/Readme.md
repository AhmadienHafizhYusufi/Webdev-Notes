# Accessing, Adding, and Updating and Object's Properties

**In this lesson, you'll learn about** accessing, adding, and updating
properties of objects in JavaScript using **dot notation** and **square bracket
notation**.

## Accessing, Adding, and Updating an Object's Properties

Objects in JavaScript are collections of **key-value pairs**, and you can
access, add, or update these properties using two main notations: **dot
notation** and **square bracket notation**.

## Dot Notation `.`

Dot notation is the most common way to **access, add, or update** properties of
an object. It provides a straightforward syntax for interacting with object
properties using `.`

### Accessing Properties

To retrieve a value from an object, use **dot notation**:

```javascript
const person = {
  firstName: "John",
  lastName: "Doe",
  age: 25,
};

console.log(person.firstName); // "John"
```

### Adding or Updating Properties

You can also use dot notation to **add new properties** or **update existing
ones**:

```javascript
// Adding a new property
person.dog = { name: "Fluffy", age: 2 };

// Updating an existing property
person.age = 26;

console.log(person);
// { firstName: 'John', lastName: 'Doe', age: 26, dog: { name: 'Fluffy', age: 2 } }
```

## Square Bracket Notation `[ ]`

Square bracket notation `[ ]` is another way to **access properties** of an
object. It offers more **flexibility**, especially when dealing with **dynamic**
property names or keys that are not valid JavaScript identifiers.

### Accessing Properties

You can access properties using square brackets:

```javascript
console.log(person["firstName"]); // "John"
```

### Dynamic Property Access

Square bracket notation allows for **dynamic property access**, which is useful
when the property name is stored in a variable:

```javascript
const property = "age";
console.log(person[property]); // 26
```

### Handling Unusual Key Names

Square bracket notation is also necessary when dealing with keys that contain
**spaces, dashes, or other characters not allowed** in JavaScript identifiers:

```javascript
// Adding properties with unusual key names
person["this-is-a-key-with-dashes"] = "value1";
person["this is another key"] = "value2";

console.log(person["this-is-a-key-with-dashes"]); // "value1"
console.log(person["this is another key"]); // "value2"

// Using dot notation with these keys would result in an error
// person.this-is-a-key-with-dashes - error
// person.this is another key - error
```

Understanding how to work with **object properties** is crucial for effectively
**managing data** in JavaScript applications. **Dot notation** `.` and **square
bracket notation** `[ ]` each have their use cases, and knowing when to use each
will enhance your coding skills.
