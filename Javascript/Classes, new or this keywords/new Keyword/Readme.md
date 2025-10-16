## `new` Keyword

The `new` keyword in JavaScript is used to create a new object.

### Creating an Object with `new`

When you use the `new` keyword, you create an **empty object**.

```javascript
const person = new Object();
```

This line of code creates an **empty object** called `person`. It's equivalent
to writing `person =`. You can **add properties** to this object just like any
other object:

```javascript
person.lastname = "John";
console.log(person.lastname); // prints "John"
console.log(typeof person); // prints "object"
```

### Object Methods & Object() Constructor

The `Object()` function is a **built-in constructor** in JavaScript that allows
you to **create objects**. You can also define your own constructor functions to
create objects of a specific type.

### Creating Custom Constructors

```javascript
function Person(name, age, profession) {
  this.name = name;
  this.age = age;
  this.profession = profession;
}

const john = new Person("John", 23, "Teacher");
console.log(john.name); // prints "John"
```

```javascript
In this example, we created a`Person` constructor **function** and used the `new` keyword to create an **instance** of `Person` object.

function Person(name, age, profession) {
  this.name = name;
  this.age = age;
  this.profession = profession;
}
```

## `new` and `this` (Keywords)

The `new` keyword **binds** `his` to the **new object** being created. In the
`Person` constructor functions, `this` refers to the **new** `Person` object.

```javascript
function Person(name, age, profession) {
  this.name = name;
  this.age = age;
  this.profession = profession;
}
```

## Built-in Constructors and Methods

JavaScript provides several built-in constructors like `Date`, `Array`,
`Number`, etc. When you use the `new` keyword with these constructors, you
create objects with built-in methods.

```javascript
const myDate = new Date("August 11, 2025");
console.log(myDate.getFullYear()); // prints 2025
```

These constructors provide methods that you can use on the objects they create. For example, arrays have methods like `pop`, `push`, `slice`, and `splice`.

## Literal Syntax vs `new` Keyword

JavaScript also provides literal syntax for creating objects and arrays, which is a shorthand for using the `new` keyword.

```javascript
const names = ['wes', 'kait'];
console.log(typeof names); // prints "object"
console.log(names instanceof Array); // prints true
```
