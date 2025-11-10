# Deep Cloning

**In this lesson, you'll learn about** deep cloning in JavaScript, which is
essential for creating independent copies of complex objects without maintaining
references to the original.

## Deep Cloning

Deep cloning involves creating a **complete copy** of an object, including all
nested objects, so that changes to the new object **do not affect the
original**. This is crucial when working with complex data structures.

## Cloning an Object with Nested Objects

Consider the following object:

```javascript
const person = {
  firstName: "Emma",
  car: {
    brand: "BMW",
    color: "blue",
    wheels: 4,
  },
};
```

### 1. Using the Spread Operator `...`

We can use the spread operator `...` to create a **shallow copy** of the object:

```javascript
const newPerson = { ...person };
```

This **removes** the reference from the outer object, allowing us to change
properties like `firstName` without **affecting** the original:

```javascript
newPerson.firstName = "Mia";

console.log(person); // { firstName: 'Emma', car: { brand: 'BMW', color: 'blue', wheels: 4 } }
console.log(newPerson); // { firstName: 'Mia', car: { brand: 'BMW', color: 'blue', wheels: 4 } }
```

However, if we change a property of the **nested** `car` object:

```javascript
newPerson.car.color = "red";

console.log(person); // { firstName: 'Emma', car: { brand: 'BMW', color: 'red', wheels: 4 } }
console.log(newPerson); // { firstName: 'Mia', car: { brand: 'BMW', color: 'red', wheels: 4 } }
```

Both objects are affected because the `car` object is still **referenced**.

### 2. Creating a Deep Clone

To create a deep clone, we need to remove references from all nested objects.
One way to achieve this is by using `JSON.stringify` and `JSON.parse`.

```javascript
const newPerson = JSON.parse(JSON.stringify(person));
```

This method **converts** the object to a **string** and then back to an
**object**, effectively **removing all references**.

**Testing the Deep Clone:**

```javascript
newPerson.firstName = "Mia";
newPerson.car.color = "red";

console.log(person); // { firstName: 'Emma', car: { brand: 'BMW', color: 'blue', wheels: 4 } }
console.log(newPerson); // { firstName: 'Mia', car: { brand: 'BMW', color: 'red', wheels: 4 } }
```

The original `person` object remains **unchanged**, confirming that `newPerson`
is a **deep clone**.

## Conclusion

**Deep cloning** is a powerful technique for working with complex objects in
JavaScript. By using `JSON.stringify` and `JSON.parse`, you can create
**independent copies** of objects, ensuring that changes to one do not affect
the other. Mastering this concept is crucial for **managing data** effectively
in your applications. If you're still a bit confused, take your time to review
this section and practice with different examples. Mastery takes time!
