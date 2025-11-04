# Change String Case

**In this lesson, you'll learn about** changing the case of strings in
JavaScript, using simple methods to convert text to **uppercase** or
**lowercase**.

## Changing the Case of a String

What is the case? You've definitely heard about **uppercase** and **lowercase**
letters. In JavaScript, we have two straightforward methods for changing the
character case:

- `string.toLowerCase()`
- `string.toUpperCase()`

These methods allow you to **convert a string** to all lowercase or all
uppercase letters, respectively.

Let's see how these methods work in practice:

```javascript
const mixedCaseString = "Hello! How are you, James?";

console.log(mixedCaseString.toLowerCase()); // "hello! how are you, james?"
console.log(mixedCaseString.toUpperCase()); // "HELLO! HOW ARE YOU, JAMES?"
```

## How It Works

Notice how we have **parentheses**`( )` on these methods. That's because they
are `functions`, more precisely `methods`, that we call on a `string`. These
methods do not modify the original string; instead, they `return` a `new string`
with the desired case transformation.

Now that you've learned how to change the case of a string, let's explore more
useful string methods! 😊
