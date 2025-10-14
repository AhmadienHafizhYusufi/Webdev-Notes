## Object

object is an unordered collection of related data in the form of key-value
pairs.

### Creating an Object

```js
const person = {
  firstName: "John",
  lastName: "Doe",
  age: 25,
};
```

- **Curly Braces**: To create an object, use curly braces {} and assign it to a
  variable.
- **Key-Value Pairs**: Inside the object, define key-value pairs. For example,
  the key `firstName` has the value `'John'`.

### Unordered Nature of Objects

Objects are **unordered**, meaning the order of properties can change and won't
always stay the same as declared.

### Nested Objects and Different Data Types

```js
const person = {
  firstName: "John",
  lastName: "Doe",
  age: 25,
  car: {
    year: 2015,
    color: "Red",
  },
};
```

### Using Variables as Values

```js
const firstName = "Johnny";

const person = {
  firstName: firstName,
};

console.log(person); // { firstName: 'Johnny' }
```

### Shorthand Property Names

If the key and value have the same name, JavaScript allows us to use shorthand
syntax:

```js
const person = {
  firstName,
};

console.log(person); // { firstName: 'Johnny' }
```

## Accessing, Adding, and Updating an Object's Properties

access, add, or update these properties using two main notations: dot notation
and square bracket notation.

### Dot Notation `.`

#### Accessing Properties

```js
const person = {
  firstName: "John",
  lastName: "Doe",
  age: 25,
};

console.log(person.firstName); // "John"
```

#### Adding or Updating Properties

```js
// Adding a new property
person.dog = { name: "Fluffy", age: 2 };

// Updating an existing property
person.age = 26;

console.log(person);
// { firstName: 'John', lastName: 'Doe', age: 26, dog: { name: 'Fluffy', age: 2 } }
```

### Square Bracket Notation `[]`

#### Accessing Properties

```js
console.log(person["firstName"]); // "John"
```

#### Dynamic Property Access

```js
const property = "age";
console.log(person[property]); // 26
```

#### Handling Unusual Key Names

```js
// Adding properties with unusual key names
person["this-is-a-key-with-dashes"] = "value1";
person["this is another key"] = "value2";

console.log(person["this-is-a-key-with-dashes"]); // "value1"
console.log(person["this is another key"]); // "value2"

// Using dot notation with these keys would result in an error
// person.this-is-a-key-with-dashes - error
// person.this is another key - error
```
