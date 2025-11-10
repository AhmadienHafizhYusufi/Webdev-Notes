# Value vs Reference Explanation

**In this lesson, you'll learn about** the concept of **reference** in
JavaScript, particularly how it applies to **objects** and **arrays**. This
understanding is crucial for managing data and avoiding unintended side effects
in your code.

## Understanding Reference in JavaScript

In our previous lesson, we explored how **primitive values** are copied by
**value**, meaning each variable gets its own copy of the data. However, when it
comes to **non-primitive** values like objects and arrays, JavaScript uses
**references** .

## Revisiting the Example

Let's revisit the example from our last lesson:

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

## What Happened Here?

When a **variable** is assigned a **primitive value**, it simply **copies** that
value. We saw this with numbers and strings. However, when a variable is
assigned a **non-primitive value** (such as an object, array, or function), it
is given a **reference** to that object’s location in memory.

In the example above, the variable `otherPerson` doesn’t actually contain the
value `firstName: 'Jon'` `lastName: 'Snow`'.

Instead, it points to a **location in memory** where that value is **stored**.

```javascript
const otherPerson = person;
```

When a **reference** type value is copied to another variable, like
`otherPerson`, the object is copied by **reference** instead of **value**. In
simple terms, `person` and `otherPerson` don’t have their **own copy** of the
value. They point to the same location in memory.

```javascript
person.firstName = "JOHNNY";

console.log(person); // { firstName: 'JOHNNY', lastName: 'Snow' }
console.log(otherPerson); // { firstName: 'JOHNNY', lastName: 'Snow' }
```

When a property is **modified** on `person`, the object in memory is
**updated**, and as a result, `otherPerson` also reflects that change.

## Equality Check

We can demonstrate this behavior with a simple **equality check**:

```javascript
const person = { firstName: "Jon" };
const otherPerson = { firstName: "Jon" };

console.log(person === otherPerson); // FALSE
```

You might expect `person === otherPerson` to resolve to true because they look
identical. However, they point to **two distinct objects** stored in
**different** locations in memory.

Now, let's create a **copy** of the `person` object by copying the
**reference**:

```javascript
const anotherPerson = person;

console.log(person === anotherPerson); // TRUE
```

`person` and `anotherPerson` hold **references** to the **same** location in
memory and are therefore considered **equal**.

## Conclusion

We've learned that **primitive values** are copied by **value**, while
**objects** and **arrays** are copied by **reference**. This means that changes
to one reference affect all references pointing to the same object. In the next
lesson, we'll explore how to make a **true copy** of an object, allowing you to
**modify one without affecting the other**. Understanding these concepts is
essential for writing robust and predictable JavaScript code.
