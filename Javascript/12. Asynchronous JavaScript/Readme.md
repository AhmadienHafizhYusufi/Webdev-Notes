# Intervals and Timers

**Welcome to a new module in this course!** I am super excited for this one,
because now we're going to understand some important concepts in JavaScript.
These concepts will later help us provide functionalities to our app like
**fetching data** and **sending data** to servers. Until now, in this course, we
have been dealing with something called **synchronous JavaScript**, and it's now
time to understand `asynchronous JavaScript`. You might not understand these
terms yet, but by the end of this lecture, you will know what they are and why
these concepts are crucial to building real-world apps. So, let's get started!

**In this lesson, you'll learn about** `asynchronous JavaScript`, a crucial
concept for building responsive and efficient applications. **Asynchronous
JavaScript** allows you to perform tasks like fetching data from a server or
handling user interactions without blocking the execution of other code.

## Introduction to Asynchronous JavaScript

JavaScript provides several **built-in functions** that enable you to execute
code at specified **intervals** or after a **delay**, even while other code is
running. This is particularly useful in scenarios like updating a game screen or
tracking time on a website.

## `setInterval()`

The `setInterval` function allows you to **execute** a block of code
**repeatedly** at specified **time intervals**. For example, the following code
logs `"Hello World"` every thousand milliseconds:

```javascript
setInterval(() => {
  console.log("Hello World");
}, 1000);
```

To prevent an interval from running **indefinitely** you can store it in a
variable and clear it using the `clearInterval()` function:

```javascript
const myInterval = setInterval(() => console.log("Hello World"), 1000);

// To stop the interval
clearInterval(myInterval);
```

The `clearInterval` function is useful when you want the interval to stop after
a certain condition is met.

### `setTimeout()`

The `setTimeout` function allows you to **execute** a block of code after a
specified **delay**. Unlike `setInterval`, it only runs **once** unless set op
to repeat. Here's how you use it:

```javascript
const myTimeout = setTimeout(() => console.log("Hello, World"), 1000); // logs "Hello World" after a thousand ms

// To cancel the timeout
clearTimeout(myTimeout);
```

The `clearTimeout` function can be used to cancel the timeout before it
executes.

## Understanding Asynchronous Execution

JavasScript doesn't execute **linearly** from top to bottom. Instead, it is
**asynchronous**, meaning that some code can be executed after other code, even
if it appears earlier in the file. This is a fundamental concept that allows
JavaScript to handle tasks like **network requests** and **user interactions**
efficiently.

As we continue through the course, you'll delve deeper into asynchronous
JavaScript, exploring concepts like **promises** and **async/await**, which
provide more **control** and **readability** when working with asynchronous
operations. Understanding these concepts is essential for building real-world
applications that are both **responsive** and **efficient**.
