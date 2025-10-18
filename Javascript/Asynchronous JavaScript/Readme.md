## Intervals and Timers

JavaScript provides several **built-in functions** that enablke you to execute
code at specified **intervals** or after a **delay**, even while other code is
running. This is particularly useful in scenarios like updating a game screen or
tracking time on a website.

### `setInterval()`

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

### `setTimeout()`

The `setTimeout` function allows you to **execute** a block of code after a
specified **delay**. Unlike `setInterval`, it only runs **once** unless set op
to repeat.

```javascript
const myTimeout = setTimeout(() => console.log("Hello, World"), 1000); // logs "Hello World" after a thousand ms

// To cancel the timeout
clearTimeout(myTimeout);
```

## Understanding Asynchronous Execution

JavasScript doesn't execute **linearly** from top to bottom. Instead, it is
**asynchronous**, meaning that some code can be executed after other code, even
if it appears earlier in the file. This is a fundamental concept that allows
JavaScript to handle tasks like **network requests** and **user interactions**
efficiently.

## Synchronous JavaScript

Synchronous JavaScript is code that is executed **line by line**, with each task
completing **instantly**. There is **no delay** in the execution of tasks for
these lines of code.

```javascript
const functionOne = () => {
  console.log("Function One");

  functionTwo();

  console.log("Function One, Part 2");
};

const functionTwo = () => {
  console.log("Function Two");
};

functionOne();

// Output:
// Function One
// Function Two
// Function One, Part 2
```

- The code executes in a **straight forward** manner.
- First, `Function One` is logged.
- Then, `functionTwo` is invoked, logging `Function Two`.
- Finally, back in `functionOne`, `'Function One, Part 2'` is logged.
- The execution is **linear** and **predictable**.

## Asynchronous JavaScript

```javascript
const functionOne = () => {
  console.log("Function One"); // 1

  functionTwo();

  console.log("Function One, Part 2"); // 2
};

const functionTwo = () => {
  setTimeout(() => console.log("Function Two"), 2000); // 3
};

functionOne();

// Output:
// Function One
// Function One, Part 2
// (after a two-second delay)
// Function Two
```

- In `functionTwo` instead of a normal `console.log`, we use `setTimeout` to
  simulate a **delay**, similar to fetching data from a server.
- The `setTimeout` function schedules `'Function Two'` to be logged after a
  **2000-millisecond delay**.
- When you run the script, `'Function One'` and `'Function One, Part 2'` are
  logged **immediately**.
- After a **two-second delay**, `'Function Two'` is logged.

**Why doesn't JavaScript wait?**

- JavScript is designed to be **non-blocking**. If the engine waited for every
  time-consuming task, it could lead to **unresponsive applications**,
  especially if users interact with the webpage during these delays.
- This **non-blocking behavior** allows the JavaScript engine continues
  executing other lines of code. When the result of the asynchronous task is
  **available**, it is then used in the program.

## Key Takeaways

- **Synchronous JavaScript**: Executes code line by line, waiting for each task
  to complete before moving on.
- **Asynchronous JavaScript**: Allows tasks to run in the background, enabling
  the engine to continue executing other code. This is essential for handling
  tasks like network requests without freezing the application.
