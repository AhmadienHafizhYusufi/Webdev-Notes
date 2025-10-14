## Advanced Array Methods

### `concat(...items)`

Returns a new array with all members of the current one and adds items to it.

```js
const moreNames = ["Eve", "Frank"];
const allNames = names.concat(moreNames);
console.log(allNames); // ["Dean", "Bob", "Jenny", "Johnny", "David", "Mark", "Eve", "Frank"]
```

### `indexOf(item, pos)`

Looks for an item starting from position pos, returns the index if found or -1
if not found.

```js
console.log(names.indexOf("Bob")); // 1
```

### `lastIndexOf(item, pos)`

Same as indexOf() but starts from the end.

```js
console.log(names.lastIndexOf("Bob")); // 1
```

### `includes(value)`

Returns `true` if the array contains the value, otherwise returns `false`.

```js
console.log(names.includes("David")); // true
```

### `find(func)`

Returns the first element for which func returns a `truthy` value.

```js
const foundName = names.find((name) => name.startsWith("D"));
console.log(foundName); // "Dean"
```

### `filter(func)`

Filters elements through `func`, returning all values that make it return
`true`.

```js
const filteredNames = names.filter((name) => name.length > 3);
console.log(filteredNames); // ["Dean", "Jenny", "Johnny", "David"]
```

### `findIndex(func)`

Like `find`, but returns the index of the first matched element.

```js
const index = names.findIndex((name) => name.startsWith("J"));
console.log(index); // 2
```

### `forEach(func)`

Calls `func` for every element. Does not return anything.

```js
names.forEach((name) => console.log(name));
// Logs: "Dean", "Bob", "Jenny", "Johnny", "David", "Mark"
```

### `map(func)`

Creates a new array from the results of calling `func` for every element.

```js
const uppercasedNames = names.map((name) => name.toUpperCase());
console.log(uppercasedNames); // ["DEAN", "BOB", "JENNY", "JOHNNY", "DAVID", "MARK"]
```

### `sort(func)`

**Sorts** the array in-place and returns it.

```js
names.sort();
console.log(names); // ["Bob", "David", "Dean", "Jenny", "Johnny", "Mark"]
```

### `reverse()`

Reverses the array and returns it.

```js
names.reverse();
console.log(names); // ["Mark", "Johnny", "Jenny", "Dean", "David", "Bob"]
```

### `split(by)`

Converts a string to an array.

```js
const str = "apple,banana,cherry";
const fruits = str.split(",");
console.log(fruits); // ["apple", "banana", "cherry"]
```

### `join(by)`

Converts an array to a string.

```js
const fruitString = fruits.join(", ");
console.log(fruitString); // "apple, banana, cherry"
```

### `reduce(func, initialValue)`

Calculates a single value over the array by calling `func` for each element.

```js
const numbers = [1, 2, 3, 4];
const sum = numbers.reduce((acc, num) => acc + num, 0);
console.log(sum); // 10
```

### `some(func)`

Returns `true` if any element passes the test implemented by `func`.

```js
const hasShortName = names.some((name) => name.length < 4);
console.log(hasShortName); // true
```

### `every(func)`

Returns `true` if all elements pass the test implemented by `func`.

```js
const allLongNames = names.every((name) => name.length > 3);
console.log(allLongNames); // true
```

### `fill(value, start, end)`

Fills the array with a repeating value from index `start` to `end`.

```js
const filledArray = new Array(3).fill("Hello");
console.log(filledArray); // ["Hello", "Hello", "Hello"]
```
