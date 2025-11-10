# Selecting Elements

**In this lesson, you'll learn about** selecting elements in the DOM using
JavaScript, which is a fundamental skill for **manipulating** and
**interacting** with web pages.

## Selecting Elements

One of the key tasks in JavaScript is to **modify** or **manipulate** existing
**elements** on a **web page**. To do this, you first need to select the
elements you want to work with. There are several **methods** to select elements
in the DOM.

### 1. Finding Elements by ID

The **easiest** and **most efficient** way to find an element is by its **ID**.
Each element on a web page should have a **unique ID**, similar to how each
student in a college has a unique enrollment ID.

```html
<div id="element-below-input"></div>

<script>
  var element = document.getElementById("element-below-input");
</script>
```

### 2. Finding Elements by Tag Name

If you want to manipulate **all elements** of a particular type, you can select
them by their **tag name**. For example, to manipulate all images on a webpage:

```html
<img src="image1path" alt="image1" />
<img src="image2path" alt="image2" />

<script>
  var images = document.getElementsByTagName("img");
</script>
```

### 3. Finding Elements by Class Name

**Class names** are often used to style elements uniquely. You can **select**
elements by their class name to **manipulate** them. For example, if all links
on a website have the class `our-link`:

```htm
<a class="our-link" href="link1">Link1</a>
<a class="our-link" href="link2">Link2</a>

<script>
  var links = document.getElementsByClassName("our-link");
</script>
```

### 4. Finding Elements by CSS Selectors

**CSS selectors** allow you to use any combination of **class, ID, tag name, and
more** to select elements. This method is very flexible and powerful.

For example, to select all span elements with the class `link`:

```html
<a class="link" href="link1">Link1</a>
<a class="link" href="link2">Link2</a>
<span class="link">Made to look like link</span>
<span class="link">Also Made to look like link</span>

<script>
  var dummylinks = document.querySelectorAll("span.link");
</script>
```

In this example, `span.link` selects all span elements with the class `link`.

Understanding how to **select elements** is crucial for **DOM manipulation**,
enabling you to create **dynamic** and **interactive** web pages by modifying
the structure and content of HTML documents.
