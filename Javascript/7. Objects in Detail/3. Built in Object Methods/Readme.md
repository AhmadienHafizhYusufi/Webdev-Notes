# Built in Object Methods

**In this lesson, you'll learn about** built-in object methods in JavaScript,
which provide powerful tools for **creating, modifying, and interacting** with
**objects**. These methods help streamline working with objects and enhance your
ability to manage data effectively.

## Built-in Object Methods

Objects in JavaScript are collections of **key-value pairs**, capable of holding
various data types, including **strings, numbers, and booleans**. All objects in
JavaScript **inherit from the parent** `Object` constructor, which offers
several built-in methods to simplify object manipulation. Unlike array methods
like `sort()` and `reverse()`, which are used on array instances, object methods
are **static** and used directly on the `Object` constructor, taking the object
instance as a **parameter**.

## Key Built-in Object Methods

### `Object.create()`

The `Object.create()` method creates a new object **linked** to the prototype of
an existing object. This is useful for **extending** objects without
**duplicating** code.

```js
const role = {
  title: "developer",
  type: "full-time",
  isOpen: true,
  showDetails() {
    const status = this.isOpen
      ? "is open for applications"
      : "is not open for applications";
    console.log(`The ${this.title} role is ${this.type} and ${status}.`);
  },
};

const designer = Object.create(role);
designer.title = "designer";
designer.showDetails(); // The designer role is full-time and is open for applications.
```

### `Object.keys()`

`Object.keys()` returns an array of an object's keys, allowing you to iterate
over them or check their count.

```js
const team = {
  leader: "Alice",
  developer: "Bob",
  designer: "Charlie",
  tester: "Dana",
};

const keys = Object.keys(team);
console.log(keys); // ["leader", "developer", "designer", "tester"]

keys.forEach((key) => {
  console.log(`${key}: ${team[key]}`);
});
```

### `Object.values()`

`Object.values()` returns an array of an object's values, useful for iterating
over or analyzing data.

```js
const device = {
  brand: "Samsung",
  model: "Galaxy S21",
  year: 2021,
};

const values = Object.values(device);
console.log(values); // ["Samsung", "Galaxy S21", 2021]
```

### `Object.entries()`

`Object.entries()` returns a nested array of an object's key-value pairs,
allowing for easy iteration and manipulation.

```js
const software = {
  name: "Photoshop",
  version: "2021",
  license: "Commercial",
};

const entries = Object.entries(software);
entries.forEach(([key, value]) => {
  console.log(`${key}: ${value}`);
});
```

### `Object.assign()`

`Object.assign()` copies values from one object to another, useful for merging
objects.

```js
const personalDetails = { firstName: "Jane", lastName: "Doe" };
const jobDetails = { position: "Manager", company: "Tech Inc" };

const profile = Object.assign({}, personalDetails, jobDetails);
console.log(profile); // {firstName: "Jane", lastName: "Doe", position: "Manager", company: "Tech Inc"}
```

### `Object.freeze()`

`Object.freeze()` prevents modifications to an object's properties and values,
ensuring immutability.

```js
const settings = { theme: "light", notifications: true };
Object.freeze(settings);

settings.theme = "dark"; // No effect
console.log(settings); // {theme: "light", notifications: true}
```

### `Object.seal()`

`Object.seal()` prevents new properties from being added to an object but allows
modification of existing properties.

```js
const account = { username: "user123", password: "pass123" };
Object.seal(account);

account.password = "newpass"; // Allowed
account.email = "user@example.com"; // Not allowed
console.log(account); // {username: "user123", password: "newpass"}
```

### `Object.getPrototypeOf()`

`Object.getPrototypeOf()` retrieves the prototype of an object, useful for
understanding inheritance and prototype chains.

```js
const gadgets = ["laptop", "tablet", "smartphone"];
console.log(Object.getPrototypeOf(gadgets) === Array.prototype); // true
```

## Conclusion

JavaScript's **built-in object methods** provide essential tools for
**managing** and **manipulating** objects, allowing you to **create, modify, and
protect data** effectively. Understanding these methods enhances your ability to
work with objects and leverage their full potential in your applications.
