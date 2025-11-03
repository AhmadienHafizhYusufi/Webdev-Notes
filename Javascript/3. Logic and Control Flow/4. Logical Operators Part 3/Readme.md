# Logical Operators Part 3 (!NOT)

In this lesson, you'll learn about the `Logical NOT (!)` operator in JavaScript,
which inverts the truthiness of values, helping you manage conditions
effectively.

## Not Operator `!`

An exclamation sign `!` is known as the **NOT operator**. It reverses the
boolean result of the condition.

The syntax is pretty simple:

```javascript
console.log(!true); // false
```

The operator accepts a single argument and does the following:

1. Converts the operand to boolean type: `true/false`.
2. Returns the inverse value.

For instance:

```javascript
console.log(!true); // false
console.log(!0); // true
```

## Double Not Operator `!!`

A double NOT `!!` is sometimes used for converting a value to boolean type:

```javascript
console.log(!!"truthy"); // true
console.log(!!null); // false
```
