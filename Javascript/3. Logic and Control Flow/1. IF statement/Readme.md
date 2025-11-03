# 'if' Statement

**In this lesson, you'll learn** about the `if` **statement** in JavaScript, a
fundamental concept for controlling the flow of logic in your programs.

## `If` Statement

You might have read the title of the current section, "**Logic and Control
Flow**" and wondered what it means. It's much simpler than it may seem.

In every programming language, we have something known as an `if` **statement**.

An if statement consists of a condition that is evaluated to either `true` or
`false` and a block of code. If the condition is `true`, then the code inside
the block will run; otherwise, it's going to be skipped. It's that simple. Let's
explore it in an example:

Imagine a nightclub that only allows people over the age of 18 to enter.

```javascript
const age = 18;

if (age >= 18) {
  console.log("You may enter, welcome!");
}
```

## `If-Else` Statement

`If` statements can also have `else if` and `else` statements. To continue with
our example:

```javascript
const age = 18;

if (age >= 18) {
  console.log("You may enter, welcome!");
} else if (age === 18) {
  console.log("You just turned 18, welcome!");
}
```

Notice how we have another condition there. If we run this code, what do you
expect to see in your console?

Some of you might expect the code that's under the `else if` statement, but
currently, that would not be the case. Let's test it out.

Why did the first block get logged out? For a really simple reason. It was the
first one to pass the check. Our first condition specified that the age must be
more than or equal to 18. 18 is indeed equal to 18. So how could we fix this? We
can simply change the condition to just a greater than sign.

## `Else` Statement

But what if the person is younger than 18? We currently aren't handling that
case. That's where the `else` statement comes in handy. We implement it like
this:

```javascript
const age = 18;

if (age > 18) {
  console.log("You may enter, welcome!");
} else if (age === 18) {
  console.log("You just turned 18, welcome!");
} else {
  console.log("Go away!");
}
```

Try noticing the difference between the `if` and the `else if` compared to the
`else` statement. Can you see it?

- An `else` statement does not have a condition.
- If nothing is matched, `else` is executed.
- `else` does not need a condition.
- Simply, if none of the other conditions evaluate to `true`, `else` runs.

That's it! You've just learned one of the key concepts of all programming
languages! Congrats! 😊
