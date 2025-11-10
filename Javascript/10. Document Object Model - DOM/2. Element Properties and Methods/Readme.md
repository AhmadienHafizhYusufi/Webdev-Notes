# Element Properties and Methods

**In this lesson, you'll learn about** HTML attributes and DOM properties, which
are essential for understanding how elements are represented and manipulated in
the DOM.

## HTML Attributes and DOM Properties

HTML elements can have various **attributes** assigned to them, such as `id`,
`class`, `type`, and more. These attributes define **characteristics** and
**behaviors** of elements in an HTML document.

## Attributes vs. Properties

- **Attributes**: These are defined in the HTML markup and specify initial
  values for elements.
- **Properties**: These are part of the DOM objects and represent the current
  state of elements.

When a browser processes an **HTML document**, it creates corresponding **DOM
properties** for standard attributes. Some attributes apply to **all elements**,
while others are **specific** to certain elements.

For example, `id` and `class` apply to all elements, while `type` is
**specific** to inputs and buttons.

## Common Properties

- `classList`: A list of classes assigned to an element. It's an array-like
  object.
- `className`: A string of classes assigned to an element, separated by spaces
  if there are multiple classes.
- `id`: A string representing the ID assigned to an element.
- `innerHTML`: The inner content of the element, including nested elements, in
  string form.

## Common Methods

- `addEventListener`: Listens for a specified event and calls a function when
  that event occurs. Events can include `click`, `mousedown`, `mouseup`,
  `focus`, `blur`, etc.
- `getBoundingClientRect`: Returns the height, width, left, and top values of an
  element relative to the browser.
- `hasAttribute`: Checks if an element has a specific attribute.
- `removeAttribute`: Removes a specified attribute from an element.
- `removeEventListener`: Removes an event listener from an element.
- `scroll`: Scrolls to an element's position.

## Example

Here's an example demonstrating the use of some **properties** and **methods**:

```javascript
<div id="div1" class="class1 class2"><span>hello</span></div>
<input id="input" type="text">
<button>Button</button>

<script>
  var element = document.getElementById("div1");

  console.log(element.classList); // ["class1", "class2"]
  console.log(element.className); // "class1 class2"
  console.log(element.id); // "div1"
  console.log(element.innerHTML); // "<span>hello</span>"

  // Example of using a method
  element.addEventListener('click', function() {
    alert('Div clicked!');
  });
</script>
```

## Conclusion

For more detailed information on DOM properties and methods, you can refer to
the [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/API/Element).
The MDN documentation provides comprehensive guides and examples to help you
understand and use these features effectively.

Understanding the **difference between attributes and properties**, as well as
how to use common DOM methods, is crucial for effectively **manipulating** and
**interacting** with HTML elements in JavaScript.
