## HTML Attributes and DOM Properties

HTML elements can have various **attributes** assigned to them, such as `id`,
`class`, `type`, and more. These attributes define **characteristics** and
**behaviors** of elements in an HTML document.

### Attributes vs. Properties

- **Attributes**: These are defined in the HTML markup and specify initial
  values for elements.
- **Properties**: These are part of the DOM objects and represent the current
  state of elements.

### Common Properties

- `classList`: A list of classes assigned to an element. It's an array-like
  object.
- `className`: A string of classes assigned to an element, separated by spaces
  if there are multiple classes.
- `id`: A string representing the ID assigned to an element.
- `innerHTML`: The inner content of the element, including nested elements, in
  string form.

### Common Methods

- `addEventListener`: Listens for a specified event and calls a function when that event occurs. Events can include `click`, `mousedown`, `mouseup`, `focus`, `blur`, etc.
- `getBoundingClientRect`: Returns the height, width, left, and top values of an element relative to the browser.
- `hasAttribute`: Checks if an element has a specific attribute.
- `removeAttribute`: Removes a specified attribute from an element.
- `removeEventListener`: Removes an event listener from an element.
- `scroll`: Scrolls to an element's position.