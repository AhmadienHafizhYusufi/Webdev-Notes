# "new" Keyword

**In this lesson, you'll learn about** the `new` keyword in JavaScript, which is
crucial for creating objects and understanding how JavaScript handles
object-oriented programming.

## Introduction

The `new` keyword in JavaScript is used to create a new object. At its core, the
new keyword performs a simple yet powerful function: it creates a new object.
Let's explore this with some code examples.

## Creating an Object with `new`

When you use the `new` keyword, you create an **empty object**. Here's how you
can **create an object** using the `new` keyword:

```javascript
const person = new Object();
```

This line of code creates an **empty object** called `person`. It's equivalent
to writing `person =`. You can **add properties** to this object just like any
other object:

```javascript
person.lastname = "John";
console.log(person.lastname); // prints "John"
```

You can also check the **type** of the `person` object:

```javascript
console.log(typeof person); // prints "object"
```

## Object Methods & Object() Constructor

The `Object()` function is a **built-in constructor** in JavaScript that allows
you to **create objects**. You can also define your own constructor functions to
create objects of a specific type.

### Creating Custom Constructors

Here's how you can create a custom constructor function:

```javascript
function Person(name, age, profession) {
  this.name = name;
  this.age = age;
  this.profession = profession;
}

const john = new Person("John", 23, "Teacher");
console.log(john.name); // prints "John"
```

In this example, we created a`Person` constructor **function** and used the
`new` keyword to create an **instance** of `Person` object.

```javascript
function Person(name, age, profession) {
  this.name = name;
  this.age = age;
  this.profession = profession;
}
```

In this example, we created a `Person` constructor **function** and used the
`new` keyword to create an **instance** of `Person`.

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

These constructors provide methods that you can use on the objects they create.
For example, arrays have methods like `pop`, `push`, `slice`, and `splice`.

## Literal Syntax vs `new` Keyword

JavaScript also provides literal syntax for creating objects and arrays, which
is a shorthand for using the `new` keyword.

```javascript
const names = ["wes", "kait"];
console.log(typeof names); // prints "object"
console.log(names instanceof Array); // prints true
```

The literal syntax is a more concise way to create objects and arrays, but under
the hood, they are still objects with methods.

Understanding the `new` keyword and how it interacts with constructors and the
`this` keyword is essential for mastering object-oriented programming in
JavaScript.
