## Simulating Asynchronous Data Fetching

**APIs**, or Application Programming Interfaces, allow you top access data from
various services. When fetching data, the time it takes can vary based on
factors like **data size** and **network speed**. Unlike `setTimeout`, where you
specify a delay, real data fetching times are **unpredictable**.

```javascript
const fetchUser = (username) => {
  setTimeout(() => {
    return { user: username };
  }, 2000); // Simulating a delay of 2000ms
};

const user = fetchUser("test");

console.log(user); // undefined
```

- The `fetchUser` function simulates a **delay** using `setTimeout`.
- It attempts to return a user object after **2 seconds**.
- However, `console.log(user)` outputs `undefined` because the function doesn't
  return the data **immediately**. The return statement inside `setTimeout`
  doesn't affect the outer function's return value.

## Callback Functions

To handle **asynchronous operations** like data fetching, we can use **callback
functions**. A callback function is a function passed into another function as
an argument, which is then invoked inside the outer function to complete some
kind of routine or action.

```javascript
const fetchUser = (username, callback) => {
  setTimeout(() => {
    console.log("Now we have the user");
    callback({ user: username });
  }, 2000);
};

fetchUser("test", (user) => {
  console.log(user);
});
```

- The `fetchUser` function now accepts a `callback` parameter.
- Inside `setTimeout`, once the simulated **delay** is over, the callback
  function is called with the user data.
- When `fetchUser` is called, we pass a callback function that logs the user
  data to the **console**.

## Key Takeaways

- **Asynchronous Operations**: These operations, like data fetching, do not
  complete **immediately** and require handling mechanisms to manage their
  completion.
- **Callback Functions**: These are a fundamental way to handle asynchronous
  operations in JavaScript. They allow you to specify what should happen **once
  an asynchronous task is complete**.

## Expanding Our Asynchronous Example

This was just a simple example, but now, let's add more **complexity** to it.
Later on, we're going to exchange callback functions for both **Promise** and
**Async/Await**. To complicate it, imagine we're working on a social media
platform. Once the user profile is fetched, we went to fetch their **photos**.
So let's create a function for that:

```javascript
const fetchUser = (username, callback) => {
  setTimeout(() => {
    console.log("Now we have the user");
    callback(username);
  }, 2000);
};

const fetchUserPhotos = (username, callback) => {
  setTimeout(() => {
    console.log("Now we have the photos");
    callback(["photo1", "photo2"]);
  }, 2000); // Simulating a delay
};

const user = fetchUser("test", (username) => {
  console.log(username);

  fetchUserPhotos(username, (userPhotos) => {
    console.log(userPhotos);
  });
});
```

This is already getting **messy**. Let's add just one more function, and you'll
easily notice the **problem**.

```javascript
const fetchPhotoDetails = (photo, callback) => {
  setTimeout(() => {
    console.log("Now we have the photo details");
    callback("details...");
  }, 2000); // Simulating a delay
};

const user = fetchUser("test", (username) => {
  console.log(username);

  fetchUserPhotos(username, (userPhotos) => {
    console.log(userPhotos);

    fetchPhotoDetails(userPhotos[0], (details) => {
      console.log(details);
    });
  });
});
```

### Problem: Callback Hell

As you can see, if we use **callbacks**, we get this weird structure that just
keeps moving to the **right**. If we added a few more callbacks, this is how it
would look:

```js
const user = fetchUser("test", (username) => {
  fetchUserPhotos(username, (userPhotos) => {
    fetchPhotoDetails(userPhotos[0], (details) => {
      fetchPhotoDetails(userPhotos[0], (details) => {
        fetchPhotoDetails(userPhotos[0], (details) => {
          fetchPhotoDetails(userPhotos[0], (details) => {
            console.log(details);
          });
        });
      });
    });
  });
});
```

This is called **callback hell**. It becomes unreadable.

In this code, we can see on the left side, there's a triangle-like structure to
the indentation, infamously knows as "**callback hell**".

**In short, every function gets an argument which is another function that is
called with a parameter that is the response from the previous one**.

As in our case, you can only imagine how many callback functions we will have to
make to display several results. It's **difficult** to manage a lot of
**callback functions**.

This pattern of coding at a large scale is **not maintainable**, is
**confusing**, and also violates the **DRY (Don't Repeat Yourself)** principle,
making it a **bad practice** to follow. To resolve this issue, JavaScript
introduced the concept of **promise**.
