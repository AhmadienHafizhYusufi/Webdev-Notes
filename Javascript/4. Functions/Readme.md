# Functions Intro

**In this lesson, you'll learn about functions** in JavaScript, which are
essential for organizing and reusing code efficiently.

## Introduction

In this section, we're going to talk about **functions**. I'm really excited to
show you how **functions** work! 😊 **Functions** are one of the most
interesting and important parts of any programming language.

So what are **functions**, and why should we use them? A JavaScript **function**
is a block of code designed to perform a particular task. Remember that: a
**block of code** designed to **perform a particular task**. We often need to
perform similar tasks many times in our application.

**Functions** are the main building blocks of a program. They allow the code to
be called many times without repetition.

You've already seen a **function** in JavaScript. Not only have you seen it, but
you've also used it multiple times by now. It was the **function** called
`console.log`. `console.log` has the task of printing values to the console.
After finishing this section, you'll be able to create your own `functions` as
well! 😊

Now, let's dive right in!

When talking about **functions**, you're often going to hear two terms:
`function declaration` and `function call`. So let's explain each one of these.

**Function**: A function is a special value with one purpose: it represents
_some code_ in your program. Functions are handy if you don’t want to write the
same code many times. **Calling** a function like `sayHi()` tells the computer
to run the code inside it and then go back to where it was in the program. There
are **many ways** to define a function in JavaScript, with slight differences in
what they do.

## Defining Functions

A `function declaration` consists of:

- the **function** keyword
- followed by the **function name**
- a list of **parameters** enclosed in parentheses ( )
- and a **block of code** enclosed in {}

I'm first going to show you an example of a simple function called `square`:

```javascript
function square(number) {
  return number * number;
}
```

Let's break it down:

- `function`: The reserved JavaScript keyword for creating a function.
- `square`: The name of the function; you can name it however you'd like.
- `Parameters`: Inside the parentheses `( )`, we have parameters. These are
  values we'll send to our function when calling it. The function `square` takes
  one parameter, called `number`. You can name parameters however you'd like.

The function body, enclosed in curly braces `{}`, contains the code to be
executed. In this example, it returns the parameter `number` multiplied by
itself.

The `return` **statement** is crucial; it specifies the value that will be
returned by the function. To retrieve values from functions, we need to **call**
them.

```javascript
square(5);
```

**Arguments** are the **values** we want to pass to our **parameters**.

For example, if we send the `value` of `5`, the parameter `number` becomes `5`.
The function then multiplies it by itself and **returns** the result.

As you can see, we get `25`. Exactly as expected.

To use the `value` from the function, we can store it in a `variable`:

```javascript
const result = square(5);
```

This **stores** the return value of the function `square` (called with an
argument of `5`) in the `result` variable. Now we can log it to the console:

```javascript
console.log(result);
```
