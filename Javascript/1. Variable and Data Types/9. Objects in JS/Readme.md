# Objects in JS

**Learning Objective**: Introduce the concept of objects as collections of data.

## What Are Objects?

An `Object` is the most important data-type and forms the building block for
modern JavaScript.ds

The` object` type is special. All other types are called “primitive” because
their values can contain only a single thing (a string or a number or whatever).
In contrast, objects are used to store collections of data and more complex
entities.

"_in simple language object are used to group variables_."

## Examples of Objects

**Create** a variable of name, and age:

```javascript
const name = "John";
const age = 25;
```

### 1. Assigning values to an object

We can create an `object` called person and put them together:

```javascript
const person = {
	name: 'John',
	age: 25;
}

console.log(person) // { name: 'John', age: 25 }
```

### 2. Extract values from an object

Once you assign the value to an `object`. We can now extract specific values
from that object using the dot notation:

```javascript
person.name;
person.age;

console.log(person.name); // John
console.log(person.age); // 25
```

## Using Objects to Store Data in Real World

Objects are very much useful, when it comes to storing data in real world. For
example, you want to store the details of a person:

```javascript
const person = {
  name: "John",
  age: 25,
  isMarried: false,
  hobbies: ["reading", "coding", "gaming"],
};

console.log(person); // { name: 'John', age: 25, isMarried: false, hobbies: ['reading', 'coding', 'gaming'] }
```

## Interactive Activity

1. Open **VS Code** and create a file called `objects.js`.
2. Declare variable `person` and assign the following properties:
   - `name`: 'John'
   - `age`: 25
   - `isMarried`: false
   - `hobbies`: ['reading', 'coding', 'gaming']
3. Extract and display the `name` and `age` from the person object.

Example:

```javascript
const person = {
  name: "John",
  age: 25,
  isMarried: false,
  hobbies: ["reading", "coding", "gaming"],
};

console.log(person.name); // John
console.log(person.age); // 25
```

1. Experiment with adding more properties to the `person` object and extracting
   them.

## What’s Next?

In this lesson, you learned how to create an object and access its values using
dot notation. Objects have many special features, which we will explore later.
Now, let’s dive into **Statically** vs **Dynamically** Typed Languages!
