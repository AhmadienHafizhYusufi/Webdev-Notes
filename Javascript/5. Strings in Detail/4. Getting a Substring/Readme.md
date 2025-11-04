# Getting a Substring

**In this lesson, you'll learn about** extracting substrings from a string in
JavaScript using the `str.slice()` method, which is a powerful tool for string
manipulation.

## Getting a Substring

The best method for getting a substring of a string is `str.slice()`. This
method allows you to extract a portion of a string based on specified start and
end positions.

### str.slice(start, end)

The `str.slice()` method returns the part of the string from `start` to (but not
including) `end`. If the `end` parameter is omitted, `slice()` extracts to the
end of the string.

Let's see it in action with an example:

```javascript
const exampleString = "hotdog";

console.log(exampleString.slice(3, 6)); // "dog"
```

## How It Works

- `start`: The zero-based index at which to begin extraction. In this example,
  `3` corresponds to the character `d`.
- `end`: The zero-based index before which to end extraction. The character at
  this index will not be included. In this example, `6` corresponds to the
  character after `g`.

The `str.slice()` method is a versatile tool for **extracting parts of a
string**, making it easier to **manipulate** and **analyze** text in JavaScript.
