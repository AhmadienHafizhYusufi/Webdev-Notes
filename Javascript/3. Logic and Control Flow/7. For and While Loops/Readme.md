# 'for' and 'while' Loops

**In this lesson, you'll learn** about `for` and `while` loops in JavaScript,
which are essential for repeating actions multiple times efficiently.

## For and While Loops

Sometimes we want to repeat an action a number of times. For example, let’s
imagine we want to display numbers from zero to nine on the console. You might
think of doing something like this:

```javascript
console.log(0);
console.log(1);
console.log(2);
console.log(3);
console.log(4);
console.log(5);
console.log(6);
console.log(7);
console.log(8);
console.log(9);
```

But that’s not a good idea at all. Instead, we use `for` or `while` loops.

## `for` Loop

The `for` loop is more complex, but it’s also the most commonly used loop. It’s
called a `for` loop because **it runs "for" a specific number of times**.

`For` loops are declared with three optional expressions separated by
semicolons: **initialization**, **condition**, and **final-expression**,
followed by a statement (usually a block statement).

```javascript
for ([initialization]; [condition]; [final - expression]) {
  // statement
}
```

- **Initialization**: Executed once before the loop starts. It's typically used
  to define and set up your loop variable.
- **Condition**: Evaluated at the beginning of every loop iteration and will
  continue as long as it evaluates to `true`. If the condition is `false` at the
  start of the iteration, the loop will stop executing.
- **Final-expression**: Executed at the end of each loop iteration, prior to the
  next condition check, and is usually used to increment or decrement your loop
  counter.

Let's use a `for` loop to print numbers from zero to nine:

```javascript
for (let i = 0; i < 10; i++) {
  console.log(i);
}
```

- **Initialization**: We initialize our variable `i = 0` because we start
  counting from 0. "i" stands for index and is a standard for loop variables.
- **Condition**: We set our condition to `i < 10`. Before each loop execution,
  it checks if i is less than ten. If i is equal to or greater than 10, the loop
  terminates.
- **Final-expression**: We use `i++`, which is shorthand for `i = i + 1`. Each
  iteration increases i by one.

## Optional Expressions in for Loop

Expressions in a `for` loop are optional, meaning we can skip parts. For
example, we can initialize the loop variable before the loop like this:

```javascript
let i = 0; // we have i already declared and assigned
for (; i < 10; i++) {
  // no need for "initialization"
  console.log(i); // 0, 1, 2, ..., 9
}
```

We can even remove everything, creating an `infinite loop` :

```javascript
for (;;) {
  // repeats without limits
}
```

## `while` Loop

The `while` loop is simpler than the `for` loop and is used when the number of
iterations is not known beforehand. It continues to execute a block of code as
long as a specified condition evaluates to `true`.

```javascript
while (condition) {
  // statement
}
```

- `Condition`: Evaluated before each loop iteration. If it evaluates to `true`,
  the loop continues; if `false`, the loop stops.

Let's use a `while` loop to print numbers from zero to nine:

```javascript
let i = 0;
while (i < 10) {
  console.log(i);
  i++;
}
```

- **Initialization**: We initialize `i = 0` before the loop starts.
- **Condition**: The loop continues as long as `i < 10`.
- **Increment**: We manually increment `i` within the loop using `i++`.

## Infinite `while` Loop

A `while` loop can also become an infinite loop if the condition never evaluates
to `false`. Be cautious to ensure that the loop has a way to terminate:

```javascript
while (true) {
  // This will run forever unless there's a break statement
}
```
