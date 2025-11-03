# Strict vs Loose Equality

**In this lesson, you'll learn** about the differences between strict and loose
equality in JavaScript, and why understanding these concepts is crucial for
writing reliable code.

## Equality in JavaScript

Equality is a fundamental concept in JavaScript. We say two values are equal
when they are the same value. For example:

```javascript
console.log("This is a string." === "This is a string."); // true
console.log(2 === 2); // true
```

Note that we use _three_ equal signs `===` to represent this concept of equality
in JavaScript.

## Loose Equality `==`

JavaScript also allows us to test **loose equality**. It is written using _two_
equal signs `==`. Things may be considered _loosely equal even_ if they refer to
_different_ values that look similar. An example would be:

```javascript
console.log(5 == "5"); // true
```

Let's explore each one in more detail:

## Strict Equality Using `===`

The strict equality method of comparison `===` is a preferred option because its
behavior can be easily predicted, which leads to fewer bugs and unexpected
results. The JavaScript interpreter **compares the values as well as their types
and only returns true when both are the same**.

```javascript
console.log(20 === "20"); // false
```

The code above will print `false` because even though the values seem to be the
same, they are of different types. The first one is of type **String** and the
second is of type **Number**.

Here's just one short thing that I wanted to show you. If we strictly compare
**objects**, we're never going to get **true**. Let's test it out:

```javascript
console.log({} === {}); // false
// we get false, even though they have the same type and content, weird

// the same thing happens for arrays as they are actually objects under the hood
console.log([] === []); // false
```

For the sake of simplicity, we're not going to go into too much depth about
non-primitive data types like **objects** and **arrays**. That is a rather
complex topic on its own. Because of that, later in the course we have a whole
separate section called "**Value vs Reference**." In there, we're going to
explore the mentioned inconsistencies of the **equality operator**.

## Loose Equality `==`

We write **loose equality** using a double equal sign `==`. It uses the same
underlying logic as **strict equality** `===` except for a minor, yet huge,
difference.

The **loose equality** `==` **doesn’t compare the data types**.

**You should almost never use the loose equality** `==`.

Douglas Crockford, in his excellent book _JavaScript: The Good Parts_, wrote:

JavaScript has two sets of equality operators: `===` and `!==`, and their evil
twins `==` and `!=`.

The evil twins `==` and `!=` do the right thing when the operands are of the
same type, but if they are of different types, they attempt to change the
values. The rules by which they do that are complicated and unmemorable. These
are some of the interesting cases:

```javascript
"" == "0"; // false
0 == ""; // true
0 == "0"; // true

false == "false"; // false
false == "0"; // true

false == undefined; // false
false == null; // false
null == undefined; // true
```

Here are a few more examples:

Using the `==` operator:

```javascript
true == 1; // true, because 'true' is converted to 1 and then compared
"5" == 5; // true, because the string of "5" is converted to the number 5 and then compared
```

Using the `===` operator:

```javascript
true === 1; // false
"5" === 5; // false
```

That's exactly how it should be. On the other hand:

```javascript
5 == "5"; // true
```

This isn't and should never be equal. `"5"` is a string, and should be treated
like that. As I mentioned, most JavaScript developers completely avoid **loose
equality** `==` and rely only on **strict equality** `===`. It is considered
better practice and causes fewer bugs. From now on, you're going to see me use
only **strict equality** `===`.

And for the end, I found for you a great visual representation of strict versus
loose equalities:

[JavaScript Equality Table](https://dorey.github.io/JavaScript-Equality-Table/)

As you can see, using the loose equality `==` we get these green boxes all over
the place. They're unpredictable. But if we switch to the strict equality `===`,
we get this nice predictable line.

**So what's the moral of the story? Always use three equal signs** `===`.
