# DOM Introduction

**In this lesson, you'll learn about** the Document Object Model (**DOM**),
which is a crucial concept for **interacting with web pages** using JavaScript.
The DOM provides a structured representation of a document, allowing you to
**access** and **manipulate** its content and structure.

## Introduction

The Document Object Model (DOM) is a standard for **accessing** and
**interacting** with documents over the internet. It represents the
**structure** of a **document** and provides a way for programming languages
like JavaScript to **understand** and **modify** it.

## What is the DOM?

- **Structure Representation**: The DOM represents how a document is structured,
  allowing for easy access and modification.
- **Language Agnostic**: While the DOM is not a programming language itself, it
  provides a standard interface for languages like JavaScript to interact with
  documents.
- **HTML Focus**: In this lesson, we'll focus on the HTML DOM, which defines how
  an HTML page is structured and can be modified.

## HTML DOM

The HTML DOM is a tree of nested HTML elements that **define the structure** of
a web page. It specifies:

- **Structure**: How an HTML page is organized.
- **Modification**: How elements can be added, removed, or changed.
- **Properties and Styles**: Attributes and styles that can be applied to
  elements.
- **Standards**: The version of the standard to be followed and valid elements
  for structuring a page.

## Core and Specific DOMs

- **Core DOM**: Defines the basic structure for all documents.
- **Specific DOMs**: Extend the core DOM to support specific document types,
  such as HTML and XML.

## Accessing the DOM

DOM elements can be **accessed** and **modified** using various **methods**.
Here's a simple example to demonstrate how you can **interact** with the DOM:

### Example: Alert on Document Load

You can use the `onload` event to trigger an action once the DOM is fully
loaded:

```javascript
<body onload="window.alert('Document loaded')"></body>
```

### Example: Adding Content Dynamically

Here's how you can **add content** to the DOM dynamically once it is loaded. In
this example, we'll display today's date:

```javascript
<html>
  <head>
    <script>
      window.onload = function() {
        const heading = document.createElement("h1");
        const date = document.createTextNode(new Date().toString());
        heading.appendChild(date);
        document.body.appendChild(heading);
      }
    </script>
  </head>
  <body>
  </body>
</html>
```

## Using JavaScript with the DOM

In the examples above, we use JavaScript to interact with the DOM using methods
like `createElement`, `createTextNode`, and `appendChild`.

We also use DOM events like `onload` to perform actions when specific events
occur. Commonly used events include `click`, `focus`, and `blur`.

Understanding the DOM is essential for web development, as it allows you to
create interactive and dynamic web pages by manipulating the structure and
content of HTML documents.
