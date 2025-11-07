# Array.filter()

**In this lesson, you'll learn about** the `array.filter()` method in
JavaScript, which is used to create a new array containing elements that pass a
specified test. This method is a powerful tool for **extracting** elements from
an array based on **specific criteria**.

## Array.filter()

The `filter()` method creates a **new array** with all elements that **pass the
test** implemented by the provided **function**. It's a concise and efficient
way to **filter out** unwanted elements from an **array**.

### Filtering Positive Numbers

Let's start with a simple example where we filter out positive numbers from an
array:

```javascript
var numbers = [-10, 0, -2, 15, -36, 25]; // Array of positive and negative integers

// Using filter to get positive numbers
var positiveNumbers = numbers.filter(function (number) {
  return number >= 0; // Elements that pass (true) the test are kept
});

console.log("Positive numbers: " + positiveNumbers); // [0, 15, 25]
```

## Using a For Loop to Filter

You can think of the `filter()` method as a more concise and readable
alternative to using a `for` loop for filtering:

```javascript
var positiveNumbersUsingLoop = []; // Array to store positive numbers

for (var i = 0; i < numbers.length; i++) {
  if (numbers[i] >= 0) {
    positiveNumbersUsingLoop.push(numbers[i]);
  }
}

console.log("Positive numbers using loop: " + positiveNumbersUsingLoop); // [0, 15, 25]
```

### Example: Rewarding Employees with Overtime

A startup wants to reward employees with 7 or more hours of overtime:

```javascript
var employeesData = [
  { name: "Sebastian Zuñiga", overtime: 5 },
  { name: "Cardi Vee", overtime: 10 },
  { name: "George Lopez", overtime: 12 },
];

var selectedEmployees = employeesData.filter(function (employee) {
  return employee.overtime >= 7;
});

console.log("Filtered Employees data: ", selectedEmployees);
```

### Example: Filtering Cities by Population

Filter cities with a population greater than 6,000,000:

```javascript
let cities = [
  { name: "Los Angeles", population: 2200000 },
  { name: "New York", population: 8000000 },
  { name: "Chicago", population: 6900098 },
  { name: "Houston", population: 2099451 },
  { name: "Philadelphia", population: 1535079 },
];

var filteredCities = cities.filter(function (city) {
  return city.population > 6000000;
});

filteredCities.forEach((city) =>
  console.log("Filtered Cities data: " + city.name)
);
```

### Example: Students with an A Grade

Filter students with a grade of 90 or above:

```javascript
const students = [
  { name: "Quincy", grade: 96 },
  { name: "Jason", grade: 84 },
  { name: "Alexis", grade: 100 },
  { name: "Sam", grade: 65 },
  { name: "Katie", grade: 90 },
];

var aStudents = students.filter(function (student) {
  return student.grade >= 90;
});

console.log("Students with an A: ", aStudents);
```

## Example: Real Estate Listings

Filter real estate listings based on user search criteria:

```javascript
const dataListings = [
  {
    address: "2301 Grand Avenue",
    city: "Oklahoma",
    state: "TX",
    rooms: 1,
    price: 220000,
    floorSpace: 2000,
    homeType: "Ranch",
  },
  {
    address: "3205 Chucky Avenue",
    city: "Houston",
    state: "TX",
    rooms: 8,
    price: 500000,
    floorSpace: 5000,
    homeType: "Apartment",
  },
  {
    address: "1234 Numbers Avenue",
    city: "Dallas",
    state: "TX",
    rooms: 5,
    price: 300000,
    floorSpace: 3500,
    homeType: "Studio",
  },
];

const searchData = {
  city: "Oklahoma",
  homeType: "Ranch",
  rooms: 1,
};

var newDataListings = dataListings.filter((item) => {
  return (
    searchData.city === item.city &&
    searchData.homeType === item.homeType &&
    searchData.rooms === item.rooms
  );
});

console.log("Filtered Listings: ", newDataListings);
```

The `array.filter()` method is a versatile tool for extracting elements from
arrays based on specific conditions, making it an essential part of data
manipulation in JavaScript.
