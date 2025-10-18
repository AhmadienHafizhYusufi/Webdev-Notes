## Import and Exports

JavaScripts **modules** allow you to break up your code into separate files,
each responsible for a specific piece of functionality. This modular approach is
particularly useful in frameworks like **React**, where components and utilities
are often separated into different files.

## Exporting from a Module

In JavaScript, you can export variables, functions, or objects from a module so
that they can be used in other files. There are to main types of exports:
**named exports** and **default exports**.

### Named Exports

Named exports allow you to export multiple items from a module. Each item must
be explicitly exported.

```javascript
const dogs = ["Bear", "Fluffy", "Doggo"];
const woof = (dogName) => console.log(`${dogName} says Woof!`);
const number = 5;
export { dogs, woof, number };
```

In this example, `dogs`, `woof`, and `number` are exported as named exports. You
can export multiple items by listing them inside curly braces.

### Default Exports

Default exports allow you to export a single item from a module. This is useful
when a module primarily exports one thing.

```javascript
const onlyOneThing = "test";
export default onlyOneThing;
```

Here, `onlyOneThing` is exported as the default export. A module can have only
one default export.

## Importing into a Module

To use the exported items in another file, you need to import them. The syntax
for importing depends on whether you're importing **named exports** or a
**default export**.

### Importing Named Exports

When importing named exports, you must use the same names as the exported items.

```javascript
import { dogs, woof, number } from "./dogs.js";

console.log(dogs); // ['Bear', 'Fluffy', 'Doggo']
woof(dogs[0]); // 'Bear says Woof!'
console.log(number); // 5
```

### Importing a Default Export

When importing a default export, you can choose any name for the imported item.

```javascript
import onlyOneThing from "./test.js";
console.log(onlyOneThing); // 'test'
```
