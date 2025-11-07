# Array.includes()

**In this lesson, you'll learn about** the `array.includes()` method in
JavaScript, which is used to **determine** whether an array contains a
**specific value**.

## Array.includes()

The `includes()` method checks if an array contains a **certain value** and
returns `true` or `false` based on the result. This method is
**case-sensitive**, meaning it distinguishes between **uppercase** and
**lowercase** letters.

### Example: Checking for a Book in a Bookshelf

Let's say we're a librarian looking for a particular book inside a "bookshelf"
array:

```javascript
var bookshelf = [
  "Moby Dick",
  "Little Women",
  "The Great Gatsby",
  "Pride And Prejudice",
];
```

Here's how you can use the `includes()` method to check for a specific book:

```javascript
if (bookshelf.includes("Moby Dick")) {
  console.log("The book you were looking for was found.");
} else {
  console.log("Couldn't find the book, sorry. :c");
}
```

### How It Works

- The `includes()` method scrolls through the entire array and returns `true`
  once it finds the **first instance** of the value it received.
- If the value is **not found** , it returns `false`.

The `array.includes()` method is a straightforward and efficient way to **check
for the presence of a value in an array**, making it a useful tool for data
validation and search operations in JavaScript.
