## Method

A method is a function associated with an object. Simply put, a method is a
property of an object that is a function. Methods allow objects to perform
actions and are defined similarly to regular functions, but they are assigned as
properties of an object.

### Defining Methods

#### Assigning a Function to an Object Property

```js
var myObj = {
  myMethod: function (params) {
    // ...do something
  },

  // OR using shorthand syntax
  myOtherMethod(params) {
    // ...do something else
  },
};
```

In this example, `myMethod` and `myOtherMethod` are methods of `myObj`.

#### Using a Function as a Method

```js
objectName.methodname = functionName;
```

Where `objectName` is an existing object, `methodname` is the name you are
assigning to the method, and `functionName` is the name of the function.

### Calling Methods

```js
object.methodname(params);
```

### Defining Methods for an Object Type

```js
function displayCar() {
  var result = `A Beautiful ${this.year} ${this.make} ${this.model}`;
  pretty_print(result);
}
```

Here, `pretty_print` is a function to display a formatted string. Notice the use
of `this` to refer to the object to which the method belongs.

### Adding Methods to an Object Constructor

You can make this function a method of `Car` by adding the statement:

```js
this.displayCar = displayCar;
```

So, the full definition of `Car` would now look like this:

```js
function Car(make, model, year, owner) {
  this.make = make;
  this.model = model;
  this.year = year;
  this.owner = owner;
  this.displayCar = displayCar;
}
```

### Calling Methods on Objects

You can call the `displayCar` method for each of the `Car` objects as follows:

```js
var car1 = new Car("Toyota", "Corolla", 2020, "Alice");
var car2 = new Car("Honda", "Civic", 2019, "Bob");

car1.displayCar();
car2.displayCar();
```
