# Strings in JS

**Learning Objective**: Understand how to work with strings and their unique
properties.

## What Are Strings?

A **string** is a sequence of characters used to represent text in JavaScript.
Whether it’s a name, a sentence, or even a symbol, strings are essential for any
programming language.

To create a string in JavaScript, you need to wrap your text in quotes.
JavaScript supports three types of quotes:

1. Single Quotes `'`
2. Double Quotes `"`
3. Backticks `

## Examples of Strings

### 1. Single and Double Quotes

Single and double quotes are essentially the same in JavaScript. They both
create simple strings.

Example:

```javascript
const singleQuoteString = "Hello, world!";
const doubleQuoteString = "Hello, world!";
```

You might choose single quotes if your string contains double quotes:

```javascript
const quote = 'She said, "JavaScript is amazing!"';
```

Or use double quotes if your string contains single quotes:

```javascript
const contraction = "It's a wonderful day!";
```

### 2. Backticks: Template Literals

Backticks `, also known as template literals, offer more functionality than
single and double quotes. They allow you to:

1. Embed variables or expressions using `${}`:

   ```javascript
   const name = "Alice";
   const greeting = `Hello, ${name}!`;
   console.log(greeting); // "Hello, Alice!"
   ```

2. Create multi-line strings:

   ```javascript
   const multiLine = `This is the first line.
   And this is the second line.`;
   console.log(multiLine);
   ```

3. Combine text dynamically:

   ```javascript
   const items = 3;
   const price = 20;
   const total = `You bought ${items} items for $${items * price}.`;
   console.log(total); // "You bought 3 items for $60."
   ```

Backticks are particularly useful when you need to create strings that involve
multiple variables or expressions.

## Inspecting Data Types with `typeof`

You can check if a value is a string using the `typeof` operator:

```javascript
const message = "Hello, world!";
console.log(typeof message); // "string"
```

## Interactive Activity

1. Open **VS Code** and create a new file called `strings.js`.
2. Try creating strings using:
   - **Single quotes** for a simple greeting.
   - **Double quotes** for a message with a quote inside it.
   - **Backticks** to embed variables or perform calculations within a string.

Example:

```javascript
const single = "Learning JavaScript!";
const double = "It's an exciting journey!";
const template = `I solved ${2 + 2} problems today!`;

console.log(single);
console.log(double);
console.log(template);
```

1. Use `typeof` to check the data type of each string:

```javascript
console.log(typeof single); // "string"
console.log(typeof double); // "string"
console.log(typeof template); // "string"
```

## What’s Next?

In this lesson, you’ve learned the basics of how strings work in JavaScript. In
upcoming modules, we’ll explore strings in much greater detail, covering topics
like:

- Changing the case of strings
- Searching for and extracting substrings
- Reversing, repeating, and trimming strings

For now, get comfortable with the basics of strings, practice creating different
types of strings, and experiment with using backticks to make your code dynamic!

Now, let’s explore numbers! 🚀
