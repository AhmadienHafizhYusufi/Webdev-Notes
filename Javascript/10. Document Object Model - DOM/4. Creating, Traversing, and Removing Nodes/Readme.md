# Creating, Traversing and Removing Nodes

**In this lesson, you'll learn about** creating, traversing, and removing
**nodes** in the DOM using JavaScript. These operations are fundamental for
dynamically manipulating web pages.

## Creating Nodes

JavaScript provides several ways to **create** HTML elements **dynamically**.
The most commonly used method is `document.createElement`.

## Creating Elements

```javascript
document.createElement("tagname"); // tagname can be any valid HTML tag
```

This method `creates` a new HTML element **but does not add** it to the DOM. You
can set attributes and content using element properties and methods. To **add
the element** to the DOM, use the `appendChild` method.

**Example:**

```javascript
const newElement = document.createElement("div");
newElement.textContent = "Hello, World!";
document.body.appendChild(newElement);
```

## Traversing the DOM

Sometimes, you may not know the **exact element** you want to **manipulate**,
but you know its **relationship** to other elements. JavaScript provides methods
to **traverse** the DOM tree.

**Example:**

```html
<ul class="subjects">
  <li>Maths</li>
  <li class="fav-subject">Science</li>
  <li>English</li>
</ul>

<script>
  const subjects = document.querySelector(".subjects");

  console.log(subjects.firstElementChild); // First element of the list
  console.log(subjects.lastElementChild); // Last element of the list

  const favSub = document.querySelector(".fav-subject");

  console.log(favSub.previousElementSibling); // Element before favorite subject
  console.log(favSub.nextElementSibling); // Element after favorite subject
  console.log(favSub.parentElement); // Parent of favorite subject (entire list)
</script>
```

**Node Traversal Methods:**

- `ele.childNodes`
- `ele.firstChild`
- `ele.lastChild`
- `ele.previousSibling`
- `ele.nextSibling`
- `ele.parentNode`

## Removing Nodes

Removing elements from the DOM is another common task. For example, you might
want to **remove** a login link once a user has logged in.

**Example:**

```javascript
const favSub = document.querySelector(".fav-subject");
favSub.remove(); // Removes element from DOM
```
Understanding how to **create, traverse, and remove** nodes is essential for building **dynamic and interactive** web applications. These operations allow you to modify the structure and content of web pages in response to user actions or other events.