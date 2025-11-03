# Logical Operators Part 2 (&&, ||)

`In this lesson, you'll learn` about logical operators in JavaScript, focusing
on more complex examples and understanding their behavior in different contexts.

## Logical Operators Recap

Logical operators are used to combine two or more conditions. If you remember
correctly, JavaScript includes three logical operators: `||` (OR), `&&` (AND),
`!` (NOT).

## AND Operator `&&`

The double ampersand `&&` is known as the **AND operator**. It checks whether
two operands are truthy values. If they are truthy, it returns `true`;
otherwise, it returns `false`. They are often used as a condition in an if
statement. Let's show that in an example.

Let's say that we want to choose which people may enter our club. To enter, they
need to be cool, and they also need to be older than 18.

```javascript
const age = 19; // age is represented by a number
const isCool = true; // isCool is represented by a boolean

if (isCool && age > 18) {
  // notice how we didn't say isCool === true
  console.log("You may enter.");
} else {
  console.log("You cannot enter.");
}
```

Now, the point of this lecture is not an `if/else` statement. Let's remove that
so we can focus purely on the **logical operators**. The only thing that

```javascript
const age = 19;
const isCool = true;

console.log(isCool && age > 18);
```

We got `true`, which is not a surprise. But now, instead of these true boolean
values, let's test it with some truthy values.

```javascript
console.log("truthy" && 1 && "test" && 999);
```

The output of this is `999`, and why is that so? Shouldn't the logical operator
`AND` return a boolean value? Here's how it works.

The AND `&&` operator does the following:

- It evaluates operands from left to right.
- It converts them to a boolean value.
  - If the result is `true`, it continues to the next value.
  - If the result is `false`, it stops and returns the original value of that
    operand.
- If all operands have been evaluated to true, it returns the last operand.

Now you know why `999` was returned; all the values were **truthy**, and it was
the last one on the list.

What if we change one value to be **falsy**?

```javascript
console.log("truthy" && 0 && "test" && 999);
```

As you can see, if even one `falsy` value exists, it's going to stop and
immediately return that value.

In other words, AND returns the first **falsy** value or the last **truthy**
value if no **falsy** values have been found.

## OR Operator `||`

The syntax for the OR operator is two straight vertical lines `||`. It checks
whether any one of the operands is a **truthy** value.

Let's see it in action:

```javascript
console.log("truthy" || 0 || "test" || 999);
```

We get `truthy`. Why is that? Well, let's see how the OR operator works:

The OR `||` operator does the following:

- For each operand, it converts it to boolean.
- If the result is `true`, it stops and returns the original value of that
  operand.
- If all operands have been evaluated to falsy, it returns the last operand.

In other words, a chain of OR `"||"` returns the first **truthy** value or the
last one if no **truthy** value is found.

So now, if we change all of the values to be **falsy**, it is going to return
the last one:

```javascript
console.log("" || 0 || null || undefined);
```

As you can see, we get `undefined`.

## Summary

JavaScript is lazy. It will want to do the least amount of work possible to get
its return value.

With the `AND` **operator**: JavaScript will first try to return the first
**falsy** value. If none were found, it will return the last **truthy** value

And with the `OR` **operator**: JavaScript will first try to return the first
**truthy** value. If none were found, it will return the last **falsy** value.
