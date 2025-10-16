## Working with Classes

While classes are often associated with styling elements using CSS, they can
also be leveraged in JavaScript to perform **actions** on **elements** with
specific classes. This allows for **dynamic interactions** and **modifications**
on a web page.

### Using Classes for Styling

Classes are commonly used to **apply styles to elements**. Multiple class names
can be assigned to an HTML element, separated by spaces.

```htm
<head>
  <style>
    .menu-item {
      background-color: black;
      color: white;
    }

    .menu-item.active {
      background-color: white;
      color: black;
    }
  </style>
</head>
<body>
  <ul>
    <li class="menu-item">Menu 1</li>
    <li class="menu-item active">Menu 2</li>
    <li class="menu-item">Menu 3</li>
  </ul>
</body>
```

### Manipulating Classes with JavaScript

To **interact** with **elements** based on their classes, you can use
JavaScript.

**Example: Adding and Removing Classes**

```htm
<head>
  <style>
    .menu-item {
      background-color: black;
      color: white;
    }

    .menu-item.active {
      background-color: white;
      color: black;
    }
  </style>
  <script>
    function menuClicked(currentElement) {
      const menuItems = document.getElementsByClassName("menu-item");

      for (var i = 0; i < menuItems.length; i++) {
        menuItems[i].classList.remove("active");
      }

      currentElement.classList.add("active");
    }
  </script>
</head>
<body>
  <ul>
    <li class="menu-item" onclick="menuClicked(this)">Menu 1</li>
    <li class="menu-item active" onclick="menuClicked(this)">Menu 2</li>
    <li class="menu-item" onclick="menuClicked(this)">Menu 3</li>
  </ul>
</body>
```

**Explanation**

- `getElementsByClassName()`: This method is used to select all elements with a
  specific class name.
- `classList.remove()`: Removes a class from an element.
- `classList.add()`: Adds a class to an element.
- `onclick Event`: Triggers the `menuClicked` function when a menu item is
  clicked. While the above code works, there are ways to optimize it. Consider
  using event delegation or modern JavaScript features like `forEach` to improve
  performance and readability.
