# Comments

As you progress through the course, you’ll see comments used frequently in the
code examples. But what are comments, and why are they important?

## What Are Comments?

A **comment** is a line or block of text in your code that JavaScript ignores
while running. Comments are there to help **explain your code**—both for
yourself and for others.

They’re especially useful when:

- You revisit your code after weeks or months and need a reminder of what it
  does.
- You’re working with a team, and others need to understand your logic.
- You want to mark areas for improvement or unfinished tasks.

Good comments explain **why** something is done, not just **what**.

## Types of Comments

JavaScript supports two kinds of comments:

### 1. Single-Line Comments

Single-line comments start with `//`. Anything after `//` on the same line is
ignored by JavaScript.

**Example:**

```javascript
// This is a single-line comment
const age = 25; // Age of the user
```

When to use:

- For short, quick notes or explanations.
- To disable a single line of code during debugging:

```javascript
// console.log("This line is ignored!");
```

### 2. Multi-Line Comments

Multi-line comments start with `/*` and end with `*/`. Everything in between is
ignored by JavaScript.

**Example:**

```javascript
/*
This is a multi-line comment.
You can use it to write detailed notes
or explain complex sections of code.
*/
```

When to use:

- For detailed descriptions of how a function or script works.
- To document larger sections of code:

```javascript
/*
 This function calculates the sum of two numbers.
 It accepts two arguments: a and b.
 Returns the result of a + b.
*/
function sum(a, b) {
  return a + b;
}
```

## Tips for Writing Great Comments

1. **Be Concise but Clear**: Avoid writing long paragraphs. Instead, focus on
   key points.

```javascript
// Bad comment
// This function takes two numbers as input, adds them together, and then returns the result.

// Good comment
// Adds two numbers
```

2. **Explain the Why, Not Just the What**:

```javascript
// Bad comment
// Increment the value
value++;

// Good comment
// Increment value to reflect the next step in the process
value++;
```

3. **Use Comments as Reminders**: Mark unfinished tasks with a TODO comment:

```javascript
// TODO: Add validation for negative numbers
```

## Quick Fun Example

Let’s add comments to a simple program:

```javascript
// This program calculates the area of a rectangle

// Length of the rectangle
const length = 10;

// Width of the rectangle
const width = 5;

/*
Calculate the area by multiplying
length and width
*/
const area = length * width;

console.log("Area of the rectangle:", area); // Display the area
```

In this example:

- Single-line comments are used to explain variables.
- A multi-line comment explains the calculation.

## Interactive Activity

1. Open **VS Code** and create a new file called `comments.js`.
2. Write a small program that:
   - Declares a variable for your name.
   - Declares another variable for your favorite hobby.
   - Logs a message to the console using these variables.
3. Add meaningful comments to your program:
   - Use **single-line comments** to explain each variable.
   - Use a **multi-line comment** to describe the purpose of your program.

Here’s a template to get you started:

```javascript
// Declare a variable for the user's name
const name = "James Bond";

// Declare a variable for the user's favorite hobby
const hobby = "driving Aston Martins";

/*
 This program combines the name and hobby
 to create a fun introduction message.
*/
console.log(`${name} loves ${hobby}.`);
```

## What’s Next?

Now that you know how to use comments, you’re ready to make your code clean and
understandable. In the next lesson, I’ll teach you how to create JavaScript
variables

Go ahead—practice adding comments to your existing code and start building great
habits for writing readable, maintainable JavaScript!
