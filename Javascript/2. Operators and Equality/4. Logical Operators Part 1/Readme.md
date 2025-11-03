# Logical Operators Part 1

**In this lesson, you'll learn** about the basic syntax and functionality of
logical operators in JavaScript, which are used to combine multiple conditions.

## Logical Operators Part 1

**Logical operators** are used to combine two or more conditions. JavaScript
includes three logical operators: `||` (**OR**), `&&` (**AND**), and `!`
(**NOT**).

Complete knowledge of logical operators requires an understanding of **if/else
statements** and **truthy and falsy values**. In this lesson, we'll cover the
**syntax of logical operators**, and we'll revisit them in more detail after
covering those topics.

## AND Operator `&&`

The double ampersand `&&` is known as the **AND operator**. It checks whether
**all operands** are truthy values. If they are, it returns **true**; otherwise,
it returns **false**.

```javascript
// **AND Operator (&&)**
console.log(true && false); // false
console.log(true && true); // true
console.log(false && false); // false
```

You can also pass **multiple conditions**:

```javascript
console.log(true && true && false); // false
```

## OR Operator `||`

The double vertical bar `||` is known as the **OR operator**. It checks whether
**at least one operand** is a truthy value. If there is at least one truthy
value, it returns `true`; otherwise, it returns `false`.

```javascript
// OR Operator (||)
// The double vertical bar **||** is known as the OR operator. It checks whether **at least one operand** is a truthy value. If there is at least one truthy value, it returns **true**; otherwise, it returns **false**.
console.log(true || false); // true
console.log(true || true); // true
console.log(false || false); // false
```

You can also pass **multiple conditions**:

```javascript
console.log(true || true || false); // true
```

## NOT Operator `!`

The exclamation mark `!` is known as the **NOT operator**. It reverses the
boolean result of a condition.

The syntax is straightforward:

```javascript
**// NOT Operator (!)**
// The exclamation mark **!** is known as the NOT operator. It reverses the boolean result of a condition.
console.log(!true);  // false
console.log(!false); // true
```

As you can see, the NOT operator simply converts boolean `false` to `true`, and
boolean `true` to `false`.
