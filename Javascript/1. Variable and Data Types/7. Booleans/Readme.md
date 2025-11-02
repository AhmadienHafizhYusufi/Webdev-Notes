# Booleans

**Learning Objective**: Understand what Booleans are, and how to use them to add
basic logic to your programs.

## What Are Booleans?

A `Boolean` is a data type that can only have one of two values:

- `true` — meaning “yes,” “correct,” or “on.”
- `false` — meaning “no,” “incorrect,” or “off.”

Booleans are essential for decision-making in programming. They help control the
flow of your program, allowing it to act differently depending on conditions.

## Examples of Booleans

### 1. Assigning Booleans

You can directly assign `true` or `false` to variables:

```javascript
const isRaining = true;
const isWeekend = false;
```

### 2. Using Booleans in Conditions

Booleans are often used in `if` statements to decide what code to execute:

```javascript
const isRaining = true;

if (isRaining) {
  console.log("Take an umbrella!");
} else {
  console.log("Enjoy the sunshine!");
}
```

## Booleans in the Real World

Booleans also play a key role in **user interactions**. For example:

```javascript
const isLoggedIn = false;

if (isLoggedIn) {
  console.log("Welcome back!");
} else {
  console.log("Please log in.");
}
```

## What About Comparisons?

Boolean values often come from **comparisons**. For instance:

```javascript
const age = 20;
console.log(age >= 18); // true
```

Comparisons return `true` or `false`, making them Booleans. We’ll dive into
comparisons and logical operators in the **Operators and Equality** module.

## Interactive Activity

1. Open VS Code and create a file called booleans.js.
2. Declare Boolean variables for:
   - Whether it’s your birthday today.
   - Whether you’ve completed today’s lesson.
3. Write an if statement for each Boolean:
   - Display a birthday greeting if true.
   - Congratulate yourself for finishing the lesson if true.

Example:

```javascript
const isBirthday = false;
const completedLesson = true;

if (isBirthday) {
  console.log("Happy Birthday!");
}

if (completedLesson) {
  console.log("Great job on completing today's lesson!");
}
```

1. Experiment with reassigning the Booleans to see how the program reacts.

## What’s Next?

In this lesson, you’ve learned how to use Booleans to control the flow of your
program. Next, we’ll dive deeper into comparisons, logical operators, and how to
combine multiple conditions in the **Operators and Equality** module.

Now, let’s dive into **Null** and **Undefined**!
