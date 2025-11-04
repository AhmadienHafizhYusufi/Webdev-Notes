# Strings Exercise

**In this lesson, you'll practice** manipulating strings in JavaScript through a
series of exercises. These exercises will help reinforce your understanding of
**string methods** and **operations**.

## Strings Exercise

We have a string representing a list of guests:

```javascript
const guestList = "Our guests are: emma, jacob, isabella, ethan";
```

Let's perform a series of operations on this string.

### 1. Get the Length of the String

Get the length of the string and store it in a variable called `length`.

_Expected output_:

```javascript
console.log(length); // 44
```

### 2. Uppercase the Entire String

Uppercase the entire string and store the result in a variable called
`uppercasedGuestList`.

_Expected output_:

```javascript
console.log(uppercasedGuestList); // OUR GUESTS ARE: EMMA, JACOB, ISABELLA, ETHAN
```

### 3. Check if 'ETHAN' is on the List

Check whether `'ETHAN'` is on the `uppercasedGuestList`. Store the answer in a
variable called `isEthanOnTheList`. The data type of the variable must be a
boolean.

_Expected output_:

```javascript
console.log(isEthanOnTheList); // true
```

### 4. Create a Substring of Guest Names

Create a substring that only contains `'EMMA, JACOB, ISABELLA, ETHAN'`. Store
the answer in a variable called `substringGuests`.

_Expected output_:

```javascript
console.log(substringGuests); // 'EMMA, JACOB, ISABELLA, ETHAN'
```

### 5. Create an Array of Guest Names

Out of the substring you just created, create an array of names of people that
are on the list. Store that array in a variable called `guests`.

_Expected output_:

```javascript
console.log(guests); // [ 'EMMA', 'JACOB', 'ISABELLA', 'ETHAN' ]
```

## Solutions

Here are the solutions to the exercises:

```javascript
// 1. Get the Length of the String
const length = guestList.length;
console.log(length); // 44

// 2. Uppercase the Entire String
const uppercasedGuestList = guestList.toUpperCase();
console.log(uppercasedGuestList); // OUR GUESTS ARE: EMMA, JACOB, ISABELLA, ETHAN

// 3. Check if 'ETHAN' is on the List
const isEthanOnTheList = uppercasedGuestList.includes("ETHAN");
console.log(isEthanOnTheList); // true

// 4. Create a Substring of Guest Names
const substringGuests = uppercasedGuestList.slice(17);
console.log(substringGuests); // 'EMMA, JACOB, ISABELLA, ETHAN'

// 5. Create an Array of Guest Names
const guests = substringGuests.split(", ");
console.log(guests); // [ 'EMMA', 'JACOB', 'ISABELLA', 'ETHAN' ]
```

These exercises provide hands-on practice with **string methods**, helping you
become more comfortable with **text manipulation** in JavaScript.
