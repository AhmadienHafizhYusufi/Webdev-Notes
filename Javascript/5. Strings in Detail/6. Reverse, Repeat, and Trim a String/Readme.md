# Reverse, Repeat, and Trim a String

**In this lesson, you'll learn about** reversing, repeating, and trimming
strings in JavaScript, which are useful operations for manipulating text.

## Reverse, Repeat, & Trim a String

Let's explore how to perform these common string operations.

### Reverse

There isn't a built-in string method that reverses a string directly. However,
we can use the knowledge we've previously gained! Remember how we can **split**
a string into an **array of characters** ? Arrays have a `reverse()` method.

Here's the process:

- **Split** the string into an array of characters.
- **Reverse** the newly created array.
- **Join** the array back into a string.

```javascript
const exampleString = "test";

const reversedString = exampleString.split("").reverse().join("");
console.log(reversedString); // "test"
```

### Repeat

If you want to **repeat** a string a certain number of times, you can easily do
that using the `string.repeat()` method.

```javascript
const dogSays = "woof";

console.log(dogSays.repeat(5)); // "woofwoofwoofwoofwoof"
```

### Trim

Sometimes, users might accidentally **add extra spaces** to their input, such as
emails or usernames. We can clean these empty spaces using the `trim()` method.

```javascript
const str = "       Hello World!        ";

console.log(str.trim()); // "Hello World!"
```

These **string operations** are powerful tools for text manipulation in
JavaScript, helping you **clean, format, and transform** strings as needed.
