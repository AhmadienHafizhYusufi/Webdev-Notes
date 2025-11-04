# Searching for a Substring

**In this lesson, you'll learn about** various methods to search for
**substrings** within a string in JavaScript, which are useful for checking the
presence and position of text.

## Finding Substrings in a String

There are multiple ways to look for a substring within a string in JavaScript.
Let's explore some of the most common methods.

### str.indexOf()

The first method is `str.indexOf(substr, pos)`. It searches for the `substr` in
`str`, starting from the given position `pos`, and returns the position where
the match was found or `-1` if nothing can be found.

For instance:

```javascript
const exampleString = "I love ducks, he said, ducks are great!";

console.log(exampleString.indexOf("ducks")); // 7
console.log(exampleString.indexOf("Ducks")); // -1
```

The **optional** second parameter allows us to search starting from the given
position. For instance, the first occurrence of `'ducks'` is at position `7`. To
look for the next occurrence, let’s start the search from position `8`:

```javascript
console.log(exampleString.indexOf("ducks", 8)); // 23
```

### str.lastIndexOf()

`str.lastIndexOf(substr, position)` is similar to `indexOf`, but it searches
from the end of a string to its beginning.

```javascript
console.log(exampleString.lastIndexOf("ducks")); // 23
```

### includes()

If you're just interested in whether a string contains a substring, and not its
position, you can use `string.includes()`. It simply returns `true` or `false`.

```javascript
console.log(exampleString.includes("ducks")); // true
```

As with the `indexOf` method, the optional second argument of `str.includes` is
the **position** to start searching from.

### str.startsWith() & str.endsWith()

The methods `str.startsWith` and `str.endsWith` check if a string starts or ends
with a specific substring:

```javascript
console.log(exampleString.startsWith("I")); // true
console.log(exampleString.endsWith("ducks")); // false
```

These **methods** provide powerful ways to **search and check** for substrings
within strings, making it easier to **manipulate** and **analyze** text in
JavaScript.
