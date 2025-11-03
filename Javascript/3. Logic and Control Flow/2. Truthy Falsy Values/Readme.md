# Truthy/Falsy Values

**In this lesson, you'll learn** about truthy and falsy values in JavaScript,
which are crucial for understanding how **conditions** are evaluated in your
code.

## Truthy and Falsy Values

In the previous section, we learned about **strict and loose equality** in
JavaScript. Equality always results in a boolean value, which can either be
`true` or `false`.

Unlike some other languages, `true` and `false` in JavaScript are not limited to
**boolean data types** and **comparisons**. They can take many other forms.

In JavaScript, we have something known as **truthy values** and **falsy
values**.

- **Truthy expressions** always evaluate to boolean `true`.
- **Falsy expressions** always evaluate to boolean `false`.

Understanding **truthy** and **falsy** values in JavaScript is **essential** .
If you don't know which values evaluate to truthy and which to falsy, you might
struggle to read and understand other people's code.

Longtime JavaScript developers often use the terms "**truthy**" and "**falsy**"
but for those new to JavaScript, these terms can be a bit confusing.

When we say a value is "**truthy**" in JavaScript, we don't just mean that the
value is `true`. Rather, it means the value coerces to `true` when evaluated in
a boolean context. Let's explore what that means.

## Falsy Values

The easiest way to learn truthy and falsy values is to memorize the falsy
values. There are only six falsy values; all other values are truthy.

**FALSY VALUES:**

- `false`
- `0` (zero)
- `""`, `''`, **``** (empty strings)
- `null`
- `undefined`
- `NaN` (not a number)

Note: An empty array `[]` is not falsy.

## Truthy Values

**Everything that is not falsy**

That's a pretty straightforward list. But how can we actually use truthiness?
Let's look at an example.

## Using Truthiness in Code

Taking advantage of truthiness can make your code more concise. You don't need
to explicitly check for `undefined`, `""`, etc. Instead, you can just check
whether a value is truthy. However, there are some caveats to keep in mind.

**Example:**

```javascript
let value = "Hello";

if (value) {
  console.log("This is a truthy value!");
} else {
  console.log("This is a falsy value!");
}
```
