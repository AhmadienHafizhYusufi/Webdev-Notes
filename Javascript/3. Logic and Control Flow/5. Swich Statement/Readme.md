# 'switch' Statement

**In this lesson, you'll learn** about the **switch statement** in JavaScript,
which is useful for performing different operations based on various conditions.

## Switch Statement

The **switch statement** is extremely similar to the `if` statement. They can be
used interchangeably, but there are situations where a **switch** is preferred.

With `if` statements, you mostly have just a few conditions: one for the `if`, a
few for the `else if`, and the final `else` statement. If you have a larger
number of conditions, you might want to consider using the `switch`
**statement**. Let's explore how it works.

The `switch` **statement** is used to perform different operations based on
different conditions.

Let's say that you have a variable called `superHero`.

```javascript
var superHero = "Captain America";
```

Based on the name of the superhero, you want to display his voice line.

We can do that using the `switch statement`. The `switch statement` takes in a
value and then checks it against a bunch of `cases`:

```javascript
switch (superHero) {
  case "Iron Man":
    console.log("I am Iron Man...");
    break;
  case "Thor":
    console.log("That is my hammer!");
    break;
  case "Captain America":
    console.log("Never give up.");
    break;
  case "Black Widow":
    console.log("One shot, one kill.");
    break;
}
```

### How It Works

In this example, we passed the `superHero` variable to the `switch` statement.

It executes the first check with a `===` triple equal sign. It looks something
like this:

```javascript
"Captain America" === "Iron Man";
```

Since this evaluates to `false`, it skips it and goes to the next one. As soon
as it finds the one that matches correctly, it prints the output.

## The Break Keyword

What is that `break` keyword?

The `break` keyword ends the `switch` when we get the correct `case`.

If we omit the `break` statement, the next `case` will be executed even if the
condition does not match the `case`.

## The Default Case

And finally, what if none of the names in the `switch` match the name of our
`superHero`? There must be something like an `else` statement, right? There is!
That something is called `default`.

If none of the `cases` match, the `default` case is going to be executed. We can
implement it like this:

```javascript
switch (superHero) {
  case "Iron Man":
    console.log("I am Iron Man...");
    break;
  case "Thor":
    console.log("That is my hammer!");
    break;
  case "Captain America":
    console.log("Never give up.");
    break;
  case "Black Widow":
    console.log("One shot, one kill.");
    break;
  default:
    console.log("Enter a valid superhero name");
    break;
}
```

That's it! Now you know how to use the `switch statement`. As always, I would
advise going into the Chrome console or a code sandbox and playing with it
yourself. You learn the most by trying things yourself.
