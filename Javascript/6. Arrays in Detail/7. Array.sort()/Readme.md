# Array.sort()

**In this lesson, you'll learn about** the `array.sort()` method in JavaScript,
which is used to **sort the elements of an array**. This method is particularly
useful for **organizing data** in a specific order.

## Array.sort()

The `sort()` method **sorts** the elements of an array. By default, it sorts the
elements as strings in **alphabetical** and **ascending** order. This can lead
to unexpected results when sorting numbers, as they are compared based on their
character values.

### Example: Sorting an Array of Names

Let's take an example of sorting an array of names alphabetically:

```javascript
var names = ["Anne", "Carl", "Bob", "Dean"];

// Sort the array alphabetically
names.sort();

console.log(names); // ["Anne", "Bob", "Carl", "Dean"]
```

## Important Note on Sorting Numbers

The `sort()` method, when used without a comparison function, converts the
elements to strings and sorts them **alphabetically**. This can cause **issues
when sorting numbers** , as they are sorted based on their character values
rather than their numeric values. For example, `10` would come before `2`
because `1` is less than `2`.

To sort numbers correctly, you need to provide a **comparison function**:

```javascript
var numbers = [10, 2, 5, 1, 9];

// Sort numbers in ascending order
numbers.sort((a, b) => a - b);

6console.log(numbers); // [1, 2, 5, 9, 10]
```

### How It Works

- **Strings**: By default, `sort()` arranges strings in **alphabetical** order.
- **Numbers**: To sort numbers correctly, use a **comparison function** that
  defines the sort order.

The `array.sort()` method is a versatile tool for organizing data, but it's
important to understand its behavior with different data types to avoid
unexpected results.
