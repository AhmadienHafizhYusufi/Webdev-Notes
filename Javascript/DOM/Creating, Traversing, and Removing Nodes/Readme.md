## Creating Nodes

For this commonly use method `document.createElement("element")`.

```javascript
document.createElement("tagname"); // tagname can be any valid HTML tag
```

This method `creates` a new HTML element **but does not add** it to the DOM. You
can set attributes and content using element properties and methods. To **add
the element** to the DOM, use the `appendChild` method.

```javascript
const newElement = document.createElement("div");
newElement.textContent = "Hello, World!";
document.body.appendChild(newElement);
```

## Traversing the DOM

Sometimes, you may not know the **exact element** you want to **manipulate**,
but you know its **relationship** to other elements. JavaScript provides methods
to **traverse** the DOM tree.

```htm
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

The `remove` method **only** removes the element from the DOM, but it
**remains** in memory and can be **re-added** if needed.
