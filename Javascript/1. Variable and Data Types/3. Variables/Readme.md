# Variables

**Learning Objective**: Learn the three ways to declare variables and understand
the rules for naming them.

In earlier versions of JavaScript, variables were solely declared using the
_var_ keyword followed by the name of the variable and a semicolon. This is how
we would do it.

```javascript
var variableName = "Old school!";
```

After ES6 (a newer version of JavaScript) , we now have two new ways to declare
a variable: `let` and `const`.

We can take a look at both of them one by one.

- The variable type `let` shares lots of similarities with var but unlike var it
  has some scope constraints. The scope is out of "scope" of this introductory
  video but we will explain it in great detail in a later video! The only thing
  that you need to know right now is that `let` is the preferred way of creating
  variables in modern JavaScript.

```javascript
let mutable = "This can change!";
```

- `Const` is another variable type assigned to data who se value cannot and will
  not change through the script.

```javascript
const immutable = "This cannot change!";
```

As you can see, I used different names for naming our variables. Everything from
`variableName`, to `mutable`, and `immutable`. It can be anything.

But what do you think, do we really have the complete freedom of choosing our
variable names? In most cases, yes, you can choose whatever name makes most
sense. But there are some quick rules.

**Rules for Naming Variables:**

1. Names must be unique.
2. Avoid reserved keywords (e.g., `var let = 5;` is invalid).
3. the first character must be a letter, an underscore (`_`), or a dollar sign
   (`&`). Subsequent characters may also include numbers.

Try creating some variables yourself!

To recap, there are three different ways to make (or declare) a variable: `var`,
`let` and `const`.

From now on, whenever we're creating a new variable, we're going to use either
the `const` or the `let` keyword.

`const` when variable is going to be constant and `let` when we plan on changing
it!

Let's move on to data types to see what kind of data can we store inside of
variables!
