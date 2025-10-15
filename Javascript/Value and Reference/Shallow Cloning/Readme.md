## Cloning Arrays

When you want to create a **copy** of an array **without keeping a reference**
to the original, you can use several methods.

- Spread Operator
- Array.slice()

### Spread Operator `...`

The **spread** operator `...` is a modern addition to JavaScript that allows you
to "spread" the **values** of **arrays**, **objects**, and **strings**. It's a
concise way to **clone** arrays.

#### How to use

```javascript
const numbers = [1, 2, 3, 4, 5];
const newNumbers = [...numbers];
```

The spread operator `...` takes all the elements from the `numbers` array and
spreads them into a **new** array `newNumbers`.

```javascript
console.log(...numbers); // 1, 2, 3, 4, 5
console.log(newNumbers); // [1, 2, 3, 4, 5]
```

#### Checking Equality

```javascript
const copiedNumbers = numbers;

console.log(numbers === copiedNumbers); // true
console.log(numbers === newNumbers); // false
```

- `copiedNumbers` points to the **same** memory location as `numbers`, so
  changes to one affect the other.
- `newNumbers` is a **separate** array, so changes to `numbers` do not affect
  it.

#### Modifying the Original Array

```javascript
numbers.push(6);

console.log(numbers); // [1, 2, 3, 4, 5, 6]
console.log(copiedNumbers); // [1, 2, 3, 4, 5, 6]
console.log(newNumbers); // [1, 2, 3, 4, 5]
```

The `newNumbers` array remains **unchanged**, demonstrating that it is a
"**shallow clone**".

### `Array.slice()`

The `slice()` method can also be used to **clone** an array:

```javascript
const numbers = [1, 2, 3, 4, 5];
const numbersCopy = numbers.slice();

console.log(numbersCopy); // [1, 2, 3, 4, 5]
```

## Cloning Objects

Just like arrays, **objects** can be **cloned** using similar methods.

### Spread Operator `...`

```javascript
const person = {
  name: "Jon",
  age: 20,
};

const otherPerson = { ...person };

// Modify the cloned object
otherPerson.age = 21;

console.log(person); // { name: 'Jon', age: 20 }
console.log(otherPerson); // { name: 'Jon', age: 21 }
```

### `Object.assign()`

The `Object.assign()` method can also be used to **clone** objects:

```javascript
const A1 = { a: "2" };
const A2 = Object.assign({}, A1);

console.log(A2); // { a: "2" }
```