# Closures

**In this lesson, you'll learn about** `closures` in JavaScript, a powerful
concept that allows functions to access variables from their outer scope even
after the outer function has finished executing.

## Closures

`Closures` are a fundamental concept in JavaScript that enable functions to
retain access to their **lexical scope**, even when the function is executed
**outside of that scope**. This is particularly useful when you have a function
defined inside another function.

Here's a basic example to illustrate `closures`:

```javascript
const outer = () => {
  const outerVar = "Hello!";

  const inner = () => {
    const innerVar = "Hi!";
    console.log(innerVar, outerVar);
  };

  return inner;
};

const innerFn = outer();
innerFn();
```

## How Closures Work

Normally, when you exit a function, all its **variables** “disappear” because
nothing needs them anymore. But if you declare a function inside another
function, the **inner function** can still be called later and access the
variables of the **outer function**. For this to work, the outer function’s
variables need to “stick around.” JavaScript handles this by keeping the
variables alive instead of forgetting them, creating what is known as a
"`closure`."

### Example of a Closure

```javascript
const init = () => {
  const hobby = "Learning JavaScript"; // hobby is a local variable created by init

  const displayHobby = () => {
    // displayHobby() is the inner function, a closure
    console.log(hobby); // using variable declared in the parent function
  };

  displayHobby();
};

init();
```

- In this example, `init()` creates a local variable called hobby and a function
  called `displayHobby()`.
- The `displayHobby()` function is an inner function that is defined inside
  `init()` and is only available within the body of the `init()` function.
- However, since inner functions have access to the variables of outer
  functions, `displayHobby()` can access the variable `hobby` declared in the
  parent function, `init()`.

In other words, a `closure` gives you access to an outer function’s scope from
an inner function. In JavaScript, `closures` are created every time a function
is created, at function creation time.

### Returning a Closure

```javascript
const init = () => {
  const hobby = "Learning JavaScript"; // hobby is a local variable created by init

  const displayHobby = () => {
    // displayHobby() is the inner function, a closure
    console.log(hobby); // using variable declared in the parent function
  };

  return displayHobby;
};

const myFunc = init();
myFunc();
```

Running this code has the same effect as the previous example, but with a twist:
the `displayHobby()` **inner function** is returned from the **outer function**
before being executed.

At first glance, it may seem **unintuitive** that this code still works. In some
programming languages, the **local variables** within a function exist only for
the duration of that function's execution. However, in JavaScript, functions
form **closures**. A **closure** is the combination of a **function** and the
**environment** within which that function was declared. This environment
consists of any **local variables** that were **in-scope** at the time the
closure was created.

- In this case, `myFunc` is a reference to the instance of the function
  `displayHobby` created when `init` is run.
- The instance of `displayHobby` maintains a reference to its **lexical
  environment**, within which the variable `hobby` exists.
- For this reason, when `myFunc` is invoked, the variable `hobby` remains
  available for use.

**Closures** are a powerful feature in JavaScript, enabling more **flexible**
and **modular** code. Understanding closures will enhance your ability to write
**efficient** and **effective** JavaScript programs.
