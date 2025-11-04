# Length and Basic Properties

**In this lesson, you'll learn about** some common operations you can perform on
strings in JavaScript, such as finding their **length** and accessing **specific
characters**.

## String Length

One thing we often want to know about strings is their **length**. You might
think that calculating this requires complex operations, like looping through
all the characters and counting them. Fortunately, it's much simpler than that!

To find the length of a string, you can use the `.length` property:

```javascript
const name = "John";

console.log(name.length); // 4
```

## Accessing Characters in a String

Another common operation is accessing a character at a **specific position** in
a string. This is also straightforward.

To get the **first letter** of a string:

```javascript
console.log(name[0]); // J
```

To get the **last letter** of a string:

```javascript
console.log(name[name.length - 1]); // n
```

Let's break down this line:

- `name.length` is equal to `4`.
- `4` minus `1` is `3`.
- `name[3]` is the last letter because string indices start from `0`, not `1`.

In the same way, you can access **any character** in the string:

```javascript
console.log(name[2]); // h
```

In this lesson, we learned how to get the length of a string using the `.length`
property and how to access specific characters within a string using bracket
notation `[ ]`.

Now let's learn how we can change the case of a string!
