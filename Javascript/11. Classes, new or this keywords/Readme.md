# Classes Introduction

**In this lesson, you'll learn about** classes in JavaScript, which provide a
structured way to **create objects** with **shared properties** and **methods**.
Classes are a key feature of object-oriented programming, allowing you to define
blueprints for objects.

## Classes Introduction

A **class** in JavaScript is a blueprint for **creating objects**. It defines
the **properties** and **methods** that the objects created from the class will
have. This makes it easy to create **multiple objects** with the **same
structure**.

## Defining a Class

To **define** a class, you use the `class` keyword followed by the **class
name**. Inside the class, you define a `constructor` method, which is used to
initialize the object's **properties**.

### Example: Defining a Person Class

```javascript
class Person {
  constructor(name, age, working) {
    this.name = name;
    this.age = age;
    this.working = working;
  }
}
```

- `class Person`: This defines a new class called `Person`.
- `constructor(name, age, working)`: The constructor method initializes the
  properties of the object. The `this` keyword is used to assign the values to
  the object's properties.

## Creating an Instance of a Class

Once you have **defined** a class, you can **create instance** of it using the
`new` keyword. This creates a **new object** with the structure defined by the
class.

### Example: Creating a User Object

```javascript
let user = new Person("John", 24, true);
console.log(user);
```

- `new Person("John", 24, true)`: This creates a new instance of the `Person`
  class with the specified values for `name`, `age`, and `working`.

## Why Use Classes?

Using classes allows you to **create multiple objects** with the **same
structure** without having to **manually define each one**. This is especially
useful when you need to create many similar objects, such as users or products.

### Example: Creating Multiple Objects

```javascript
let user1 = new Person("Alice", 30, false);
let user2 = new Person("Bob", 28, true);

console.log(user1); // Person {name: "Alice", age: 30, working: false}
console.log(user2); // Person {name: "Bob", age: 28, working: true}
```

## Conclusion

Classes in JavaScript provide a powerful way to **define** and **manage** objects with shared properties and methods. By using classes, you can create clean and maintainable code, making it easier to manage complex applications. Understanding how to define and use classes is essential for effective object-oriented programming in JavaScript.