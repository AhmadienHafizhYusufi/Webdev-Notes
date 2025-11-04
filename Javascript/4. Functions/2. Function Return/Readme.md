# Function Return

**In this lesson, you'll learn about** the **return statement** in JavaScript
functions, which is crucial for understanding how functions output values and
control flow.

## Return Statement in Functions

Every function in JavaScript returns `undefined` unless otherwise specified.
That means **if we don't explicitly specify** what we want our function to
**return** , it will always return `undefined`.

Let's create a function called `double`. It will take in one parameter, called
`number`, and return that number multiplied by two. Don't worry about arrow
function syntax too much; we'll cover it in greater detail in the next lesson!
😊

Here's a simple function that returns the sum of numbers `a` and `b`:

```javascript
function add(a, b) {
  return a + b;
}
```

This function will return the sum of `a` and `b`. We can then invoke the
function and save the `return value` to a variable:

```javascript
const sum = add(2, 2);
```

When we log out our `sum` value, we get `4`:

```javascript
console.log(sum); // 4
```

## Immediate Function Termination

Another important rule of the `return` statement is that it **stops function
execution** immediately.

Consider this example where we have **two** `return` statements in our `test`
function:

```javascript
function test() {
  return true;
  return false;
}

test(); // true
```

The first `return` statement immediately stops execution of our function and
causes it to return `true`. The code on line three, `return false`; is **never**
executed.

We can also **test** it by adding some **console logs**:

```javascript
function test() {
  console.log(1);
  return true;
  console.log(2);
  return false;
  console.log(3);
}

test(); // true
```

As you can see, we only get the **console log** with the value of `1`. As soon
as the function **returns** something, it doesn't care about anything else. It's
done its job, and now other JavaScript code can be run.

In the next lesson, we're going to explore `arrow functions`, the **modern way**
of writing JavaScript functions.
