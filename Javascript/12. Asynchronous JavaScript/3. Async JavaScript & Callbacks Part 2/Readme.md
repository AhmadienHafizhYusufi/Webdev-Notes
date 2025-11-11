# Async JavaScript & Callbacks Part 2

**In this lesson, you'll learn about** the challenges of using **callback
functions** in JavaScript, particularly when dealing with multiple asynchronous
operations. This pattern, known as "**callback hell**," can make code difficult
to read and maintain. We'll explore this issue and introduce the concept of
**promises** as a solution.

## Expanding Our Asynchronous Example

This was just a simple example, but now, let's add more **complexity** to it.
Later on, we're going to exchange callback functions for both **Promises** and
**Async/Await**. To complicate it, imagine we're working on a social media
platform. Once the user profile is fetched, we want to fetch their **photos**.
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

## Problem: Callback Hell

As you can see, if we use **callbacks**, we get this weird structure that just
keeps moving to the **right**. If we added a few more callbacks, this is how it
would look:

```javascript
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

This is called **callback hell**. It becomes **unreadable**.

In this code, we can see on the left side, there's a triangle-like structure to
the indentation, infamously known as "**callback hell**."

**In short, every function gets an argument which is another function that is
called with a parameter that is the response from the previous one.**

You might find this sentence baffling, which describes the **CALLBACK HELL**.

As in our case, you can only imagine how many callback functions we will have to
make to display several results. It's **difficult** to manage a lot of
**callback functions**. Even if you wrote them yourself, you're going to have a
hard time understanding them once you come back to the code after some time!

This pattern of coding at a large scale is **not maintainable**, is
**confusing**, and also violates the **DRY (Don't Repeat Yourself)** principle,
making it a **bad practice** to follow. To resolve this issue, JavaScript
introduced the concept of **promises**. In the next lesson, you'll fully
understand how promises work, and we'll refactor this code to use promises.
