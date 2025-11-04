# Parameters vs Arguments

**In this lesson, you'll learn about** the difference between `parameters` and
`arguments` in JavaScript functions, which is crucial for understanding how data
is passed to functions.

## Parameters vs Arguments

If you’re new to JavaScript, you may have heard the terms `parameters` and
`arguments` used interchangeably. While very similar, there is an **important
distinction** between these two concepts.

- `Parameters` are used when defining a function. They are the **names** created
  in the function definition. A parameter acts like a **variable** that is only
  meaningful **inside the function**. It won't be accessible outside of the
  function.
- `Arguments` are the real **values** passed to the function when making a
  **function call**.

Let's revisit our example to illustrate this distinction. We would say that our
function accepts one `parameter`. Parameters can be named anything. The only
thing that matters is the **order**. Let's try replacing `name` with
`firstName`.

```javascript
const sayHi = (firstName) => {
  console.log(`Hi, ${firstName}`);
};

sayHi("Joe"); // Hi, Joe
```

**Nothing changed; our function still works**. This shows that `parameters` are
just **names** we create for the `arguments` we're planning to pass into the
**function**. As you can see, when calling the function, we have one `argument`.
The argument is a real JavaScript value, in this case, a `string` of `'Joe'`.

Let's try adding another `parameter` to practice a bit more. Suppose we want to
take in both the name and the age of the person. To do that, we'd need to add a
**second** `parameter`, separated by a comma `","`. We also need to provide an
`argument` to fill the **value** of age when making a **function call**:

```javascript
const logAge = (name, age) => {
  console.log(`${name} is ${age} years old.`);
};

logAge("Joe", 25); // Joe is 25 years old.
```

Understanding the **difference** between `parameters` and `arguments` is key to
effectively using functions in JavaScript. As you practice, you'll become more
comfortable with **how data flows through your functions**.
