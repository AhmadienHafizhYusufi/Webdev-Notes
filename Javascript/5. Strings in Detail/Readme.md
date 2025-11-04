# Strings Introduction

**In this lesson, you'll learn about** strings in JavaScript, which are used to
store and manipulate text.

## Strings in JavaScript

In JavaScript, and in any programming language for that matter, we need a way to
store text. In JavaScript, we use **strings** to store text. A string is a
**primitive data type** that represents a sequence of characters.

## Creating Strings

There are a few ways to create strings in JavaScript:

```javascript
const single = "This is a string written inside of single quotes.";
const double = "This is a string written inside of double quotes.";
const backticks = `This is a string written inside of backticks.`;
```

- **Single and Double Quotes**: Strings created with single `' '` and double
  quotes `" "` are the same. We can call them simple or basic strings. They
  represent **static** textual values.
- **Backticks**: Strings created with backticks `` provide extended
  functionality. They are **dynamic** and allow us to execute JavaScript logic
  inside them.

## Dynamic Strings with Backticks ``

Backticks `` allow for string interpolation, where you can embed expressions
inside a string:

```javascript
const backticks = `${2 + 2}`; // 4
```

- Everything inside $ is evaluated as JavaScript logic.
- Therefore, `2 + 2` returns `4`, rather than the string '2 + 2'.

You can also make function calls inside a `` string:

```javascript
const sum = (a, b) => a + b;
const total = `The sum is ${sum(2, 2)}`; // The sum is 4
```

## Multiline Strings with Backticks ``

Backtick strings can span multiple lines:

```javascript
const numbers = `
  1
  2
  3
`;
```

If you tried doing this with basic single or double quote strings, you would get
an error.

## Handling Quotes Inside Strings

Consider the following string:

```javascript
const greeting = 'Hi, I'm John';
```

This would produce an **error** because the single quote after "I" ends the
string prematurely. JavaScript doesn't know how to evaluate the rest of the
code.

One way to fix this is to use different types of **quotes**: ' ', " ", ``

```javascript
const greeting = "Hi, I'm John.";
```

But if you have **both types of quotes** in the sentence, it can get tricky:

```javascript
const greeting = "Hi, I'm John, "Johnny John".";
```

This would break again. To handle this, you can use an **escape character** `\`
to treat special characters like normal letters:

```javascript
const greeting = 'Hi, I\\'m John, \\"Johnny John\\".';
```

However, using **backticks** `` simplifies this:

```javascript
const greeting = `Hi, I'm John, "Johnny John".`;
```

This way, you can write the string however you want without worrying about
escaping quotes `\`.

Great! This lesson covered all the **basics** of strings, and you've learned it
all! Strings are pretty **simple**, yet **powerful** tools in JavaScript.
