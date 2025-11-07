# Array.find()

**In this lesson, you'll learn about** the `array.find()` method in JavaScript,
which is used to **locate the first element in an array that satisfies a
specified condition**.

## Array.find()

The `find()` method returns the **first element** in the **array** that
satisfies the provided testing **function**. If no elements satisfy the testing
function, `undefined` is returned.

### Example: Finding a State

Let's start with a simple example where we find a specific state in an array:

```javascript
var states = ["tx", "ca", "nm"];

// The find method for arrays returns the first value that satisfies the condition
var stateFoundUsingFind = states.find(function (state) {
  return state === "tx";
});

console.log("First value to satisfy the condition is: " + stateFoundUsingFind); // "tx"

// Using a for loop to achieve the same result
for (var i = 0; i < states.length; i++) {
  if (states[i] === "tx") {
    console.log("First value to satisfy the condition: " + states[i]); // "tx"
    break; // Exit the loop once the condition is satisfied
  }
}
```

## Example: Finding an Item in a Store

Here's an example where we find an item in a store's inventory:

```javascript
var itemsInStore = ["fruits", "tvs", "ipods", "carpets"];
var customerRequestedItem = "tvs";

// Returns item if it is found and undefined if it is not
var targetItem = itemsInStore.find(function (item) {
  return item === customerRequestedItem;
});

console.log("Target item: " + targetItem); // "tvs"
```

## Example: Finding a Tree in a Store

Let's find a specific type of tree in a tree store:

```javascript
var treeStore = ["birch", "maple", "oak", "poplar"];
var targetTree = "birch";

var tree = treeStore.find(function (tree) {
  return tree === targetTree;
});

console.log("Tree: " + tree); // "birch"
```

The `array.find()` method is a useful tool for **quickly locating elements** in an
array that meet specific criteria , making it an essential part of data
manipulation in JavaScript.
