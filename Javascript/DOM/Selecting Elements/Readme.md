## DOM - Selecting Elements

One of the key tasks in JavaScript is to **modify** or **manipulate** existing
**elements** on a **web page**. To do this, you first need to select the
elements you want to work with. There are several **methods** to select elements
in the DOM.

### 1. Finding Elements by ID

Use method `document.getElementById("chosen-element")` for unique ID.

```htm
<div id="element-below-input"></div>

<script>
  var element = document.getElementById("element-below-input");
</script>
```

### 2. Finding Elements by Tag Name

Use method `document.getElementsByTagName("chosen-tag")` for tag.

```htm
<img src="image1path" alt="image1" />
<img src="image2path" alt="image2" />

<script>
  var images = document.getElementsByTagName("img");
</script>
```

### 3. Finding Elements by Class Name

Use method `document.getElementsByClassName("chosen-class")` for class name.

```htm
<a class="our-link" href="link1">Link1</a>
<a class="our-link" href="link2">Link2</a>

<script>
  var links = document.getElementsByClassName("our-link");
</script>
```

### 4. Finding Elements by CSS Selectors

**CSS selectors** allow you to use any combination of class, ID, tag name, and
more to select elements. Use method
`document.querySelectorAll("chosen-selectors")` for this.

```htm
<a class="link" href="link1">Link1</a>
<a class="link" href="link2">Link2</a>
<span class="link">Made to look like link</span>
<span class="link">Also Made to look like link</span>

<script>
  var dummylinks = document.querySelectorAll("span.link");
</script>
```
