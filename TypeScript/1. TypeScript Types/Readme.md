# TypeScript types

## Basic Types

Let's make this painless. Hop into the
[official typescript playground](https://www.typescriptlang.org/play/) and just
delete all of the code they provide us.

You'll see a code editor to the left- and as we type we'll see any errors in our
code pop up on the right.

Let's add some simple Javascript to the page:

```javascript
let userName = "Billy";
let userAge = 22;
```

Done. No errors. This is completely valid Typescript! And we haven't even had to
set any types! So let's change a value after we've declared it.

```typescript
let userName = "Billy";
let userAge = 22;
userAge = "old";
```

We'll get an error:

```console
Type 'string' is not assignable to type 'number'.
```

So what gives? We didn't set a type for anything yet, why does it tell us we
can't make a string a number? Because you don't have to directly tell Typescript
to assign a type to a variable (explicit), it will also infer the types of
everything based on the initial value (implicit).

So we actually implicitly set the types to "string" and "number" just by
declaring them. If we **explicitly** type them it might be more obvious what the
issue is:

```typescript
let userName: string = "Billy";
let userAge: number = 22;
userAge = "old";
```

`userAge` is a number, but we assigned it a 'string' value. This is very
helpful. This stops us from writing code where we declare a variable as a string
or object- and then later try to map over it like an array. Typescript knows and
keeps track of our variable types and will yell at us when we do something
wrong.

Let's look at some basic types and examples:

```typescript
let userName: string; // "Hello" or "Brandon"
let userAge: number; // 200 or 12.5 or -49
let isActive: boolean; // true or false

let interests: string[]; // ["Hey","Brandon"]
let favoriteNumbers: number[]; // [200,12.5,-49]

let usuallyBad: any; // anything at all

let linkedInLink: undefined; // undefined
let facebookLink: null; // null
```

Most of pretty obvious- but notice that you can make an `array` out of any of
the basic types by just adding `[]` to the end. This tells Typescript that the
variable will be an array **of** that type.

You also see 'any' listed as a type. For the most part- if you write this you're
doing something wrong. You really want to only do this in special circumstances
like when using a third party library that doesn't have types, when creating
some dynamic data that might rely on unpredictable user input, or for example in
a `try...catch` block as the type of 'error'.

## Multiple Types

You've seen that we assign a type to each variable- either implicitly or
explicitly- and that Typescript get's mad if we change it. But sometime we
really do want to have a variable hold more than one type of value. What if the
`facebookLink` in the above example could also be a string depending upon what
we get back from our database or an API?

We can use a 'union type' with the `|` symbol.

```typescript
let facebookLink: null | string;
facebookLink = "http://somelink.com";
facebookLink = null;
```

Now `facebookLink` can be either null OR string. And we won't get any errors for
changing the type around.
