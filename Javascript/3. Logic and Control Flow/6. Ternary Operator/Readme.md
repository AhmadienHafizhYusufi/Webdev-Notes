# Ternary Operator

**In this lesson, you'll learn** about the `ternary operator` in JavaScript, a
concise way to perform simple `true or false` checks.

## Ternary Operator

You could say that the `switch` statement is a more complex version of the `if`
statement. There's yet another version of it: the **ternary operator**.

It should be used just for simple **true or false** checks.

To explain the **ternary operator** , let's first take a look at the syntax of a
typical `if` statement:

```javascript
if (condition) {
    value if true
} else {
    value if false
}
```

Now, the ternary operator:

```javascript
condition ? value if true : value if false
```

Although this is just pseudocode, meaning the code is written in half English
and half real syntax, I think you can still see how we would use the `ternary`.
Let's use the same old driver's license example we had when we were learning
about the `if` **statement** .

```javascript
if (person.age > 18) {
  console.log("You can drive");
} else {
  console.log("You may not drive yet");
}
```

And now let's transfer it to a `ternary`. I'll first write it out and then we're
going to explore it in detail:

```javascript
person.age > 18
  ? console.log("You can drive")
  : console.log("You may not drive yet");
```

## How It Works

- Reading from left to right, we first have our **condition**.
- Following a **question mark** `?`, is the expression that is going to be
  executed if the condition evaluates to `true`.
- Finally, following the colon sign `:`, is the expression that is going to be
  executed if the condition evaluates to `false`.

At first, `ternary operators` may seem a bit weird and hard to read. But as you
write more of them, you'll quickly get better at understanding them. They'll
quickly become your go-to tool if you have just a simple `true` or `false`
question.
