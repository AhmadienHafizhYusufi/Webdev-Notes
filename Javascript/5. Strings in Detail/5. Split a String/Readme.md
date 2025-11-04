# Split a String

**In this lesson, you'll learn about** splitting strings into multiple
substrings using the `split()` method in JavaScript, which is useful for
breaking down text into manageable parts.

## Splitting Strings

Sometimes, we might want to **split** a string into **multiple** substrings. For
that, we'll use a string **method** called `split()`.

The `split()` method divides a string into an **array of substrings** based on a
specified separator. Let's look at some examples.

### Splitting a Word into Characters

To split a word into **individual** characters, you can use an `empty string` as
the separator:

```javascript
const exampleString = "dog";

console.log(exampleString.split("")); // ["d", "o", "g"]
```

### Splitting a Sentence into Words

To split a sentence into **words** , use a `space character` as the separator:

```javascript
const exampleString = "The quick brown fox jumps over the lazy dog.";

console.log(exampleString.split(" ")); // ["The", "quick", "brown", "fox", "jumps", "over", "the", "lazy", "dog."]
```

### Result

The result of both examples is an **array** `[ ]` . The `split()` method returns
an array of **substrings** , allowing you to easily manipulate and analyze parts
of the **original** string.

The `split()` method is a powerful tool for **breaking down strings into smaller
parts**, making it easier to work with text data in JavaScript.
