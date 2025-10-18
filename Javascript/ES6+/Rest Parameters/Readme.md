## Rest Parameters

Rest parameters enable you to represent an **indefinite number of arguments** as
an **array**. This is particularly useful when you want to work with functions
that can take a **variable number of arguments**.

### Syntax and Usage

The rest parameter **syntax** uses **three dots** `...` followed by a name,
which collects all remaining arguments into an array.

```javascript
function calculateTotal(...numbers) {
  let sum = 0;
  for (const num of numbers) {
    sum += num;
  }
  return sum;
}

console.log(calculateTotal(1, 2, 3)); // Expected output: 6
console.log(calculateTotal(1, 2, 3, 4)); // Expected output: 10
```

**Key Points:**

- A function can only have one rest parameter.
- The rest parameter must be the last parameter in the function definition.
- Trailing commas are not allowed after the rest parameter.
- The rest parameter cannot have a default value.

### Differences Between Rest Parameters and the arguments Object

1. **Array Nature**: Rest parameters are true arrays, allowing you to use array
   methods like `sort()`, `map()`, `forEach()`, or `pop()` directly. The
   `arguments` object is not a real array.
2. **Callee Property**: The `arguments` object has a deprecated `callee`
   property, which rest parameters do not have.
3. **Parameter Syncing**: In non-strict mode, the `arguments` object syncs its
   indices with parameter values, while rest parameters do not.
4. **Content**: Rest parameters bundle only the extra parameters into an array,
   excluding named arguments. The `arguments` object includes all parameters.

### Examples of Using Rest Parameters

**Basic Usage:**

```javascript
function displayInfo(first, second, ...additionalInfo) {
  console.log("First:", first);
  console.log("Second:", second);
  console.log("Additional Info:", additionalInfo);
}

displayInfo("apple", "banana", "cherry", "date", "elderberry");
// First: apple
// Second: banana
// Additional Info: ["cherry", "date", "elderberry"]
```

**Using Rest Parameters With Other Parameters:**

```javascript
function scaleValues(factor, ...values) {
  return values.map((value) => factor * value);
}

const scaledArray = scaleValues(3, 10, 20, 30);
console.log(scaledArray); // [30, 60, 90]
```

**Converting `arguments` to an Array (Pre-ES6):** Before rest parameters, you
had to convert `arguments` to a normal array:

```javascript
function oldStyleFunction(a, b) {
  const arrayVersion = Array.prototype.slice.call(arguments);
  // — or —
  const arrayVersion2 = [].slice.call(arguments);
  // — or —
  const arrayVersionFrom = Array.from(arguments);

  const firstElement = arrayVersion.shift(); // OK, gives the first argument
}
```

**Using `Rest Parameters` (ES6+):** With rest parameters, you can directly
access a normal array:

```javascript
function newStyleFunction(...args) {
  const arrayVersion = args;
  const firstElement = arrayVersion.shift(); // OK, gives the first argument
}
```
