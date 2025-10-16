## `this` Keyword

The `this` keyword in JavaScript refers to the **object** that is executing the
**current function**

It provides a way to access the **properties** and **methods** of the object
within which the function is being executed. Understanding `this` is crucial for
working with object-oriented programming in JavaScript.

### Using it in a Function

```javascript
function Sentence(words) {
  this.words = words;
  console.log(this);
}

const S = new Sentence("hello there, we are learning about the `this` keyword");
```

1. **Function Definition**: We define a function `Sentence` that takes an input
   parameter `words`.
2. **Assigning Properties**: Inside the function, we assign `this.words` to the
   input parameter `words`. This means that the `words` property of the object
   being created will hold the value passed to the function.
3. **Logging** `this`: We use `console.log(this)` to print the current context
   of `this`. When the function is called with the `new` keyword, `this` refers
   to the new object being created.
4. **Creating an Instance**: We create a new instance of `Sentence` by calling
   `new Sentence(...)`. This creates a new object, and `this` within the
   function refers to this new object.

### What Happens When You Run the Code

- When you run the code, the `Sentence` function is executed in the context of a
  **new object**. The `this` keyword inside the function refers to **this** new
  object.
- The `console.log(this)` statement outputs the new object, showing its
  properties, including `words` which is set to the string "hello there, we are
  learning about the `this` keyword".

## Key Points to Remember

- **Context Matters**: The value of `this` depends on how a function is called.
  In the context of a constructor function (like `Sentence`), `this` refers to
  the **new object** being created.
- **Global Context**: If a function is called without an object context (e.g.,
  not as a method or constructor), `this` refers to the global object (or
  `undefined` in strict mode).
- **Method Context**: When a function is called as a method of an object, `this`
  refers to the object the method is called on.
