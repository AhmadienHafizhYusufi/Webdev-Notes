# Statically vs Dynamically Typed Languages

**Learning Objective**: Differentiate between Statically typed and Dynamically
typed languages in terms of data types.

## What are `statically` typed languages?

- Statically typed languages are those in which the type of each variable and
  expression is determined at compile time.
- Once a variable is assigned a specific data type, it cannot store values ofa
  different type.
- Examples: C, C++, and Java.

## What are `dynamically` typed languages?

- Dynamically typed languages are those in which the type of each variable is
  determined at runtime.
- Variables can store different data types at different times.
- Javascript is dynamically typed language.

## Change Variable Data Type

In JavaScript, you can change the data type of a variable at any time. For
example, you can change a variable from a number to a string:

```javascript
let age = 25;
console.log(age); // 25

age = "25";
console.log(age); // 25
```

## Key Differences Between `Statically Typed` and `Dynamically Typed` Languages

| **Feature**         | **Statically Typed**                          | **Dynamically Typed**                       |
| ------------------- | --------------------------------------------- | ------------------------------------------- |
| **Type Checking**   | Performed at compile time.                    | Performed at runtime.                       |
| **Flexibility**     | Less flexible; variables have fixed types.    | More flexible; variables can change types.  |
| **Error Detection** | Catches type-related errors before execution. | Errors may appear only during execution.    |
| **Performance**     | Generally faster due to early type checks.    | Can be slower due to runtime type checking. |
| **Examples**        | C, C++, Java.                                 | JavaScript, Python, Ruby.                   |

## What’s Next?

In this lesson, you learned the difference between statically typed and
dynamically typed languages. Now, let’s dive into **Operators in JavaScript**!
