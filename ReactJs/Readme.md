# The Ultimate React.js Guide for Developers

## What’s in the guide?

Learning JavaScript libraries and frameworks can be overwhelming. There are many
libraries to choose from, and no proper step-by-step guides that’ll teach you
how to use these libraries to their fullest potential.

That’s why, in this guide, you’ll learn the most popular JavaScript library,
used by hundreds of thousands of developers worldwide - `React.js`.

This guide covers the complete `React.js roadmap`, JavaScript prerequisites,
essential `React.js concepts`, and project ideas that you can build & deploy and
put up on your portfolio and get a job.

- Learn the React.js fundamentals
- Understand the JavaScript prerequisites
- Explore essential React.js concepts
- Build projects and deploy them
- Enhance your portfolio and increase job opportunities

## Introduction to React.js

React.js is a front-end JavaScript library for building user interfaces. It was
developed by `Facebook` and is maintained by Facebook and the open-source
community.

React.js is a phenomenal library that is easy to understand, has excellent
cross-platform support, has a fantastic community, and is one of the most loved
libraries out there.

There are also two great React.js competitors: `Vue.js`, `Angular`. These
libraries and frameworks are mainly used to create fast and efficient
`Single Page Applications`.

Although these are great technologies, taking a quick look at `Google Trends`,
we can clearly see that React.js is still in the lead by far.

## JavaScript prerequisites

You might be wondering, what are the prerequisites to learn such a great
JavaScript library?

There’s only one prerequisite and that is - `JavaScript`.

Do not jump straight into React.js without understanding the topics I've
mentioned below.

Before learning React, you should have a good understanding of these
`JavaScript` topics:

- Basic Syntax
- ES6+ features
- Arrow functions
- Template literals
- Array Methods
- Object property shorthand
- Destructuring
- Rest operator
- Spread operator
- Promises
- Async/Await syntax
- Import and export syntax

## React.js Roadmap

### Basic things to learn in React.js

- File & Folder structure
- Components
- JSX
- Props
- State
- Events
- Styling
- Conditional Rendering

### Learn about React.js Hooks - the essential hooks to learn:

- useState
- useEffect
- useRef
- useContext
- useReducer
- useMemo
- useCallback

### Then learn some of the React.js UI Frameworks

- Material UI
- Ant Design
- Chakra UI
- React Bootstrap
- Rebass
- Blueprint
- Semantic UI React

### Learn to use some of the most popular React.js packages

- React Router
- React Query
- Axios
- React Hook Form
- Styled Components
- Storybook
- Framer Motion

### Learn how to manage state with state management tools

- Redux
- MobX
- Hookstate
- Recoil
- Akita

### More things to learn after learning React.js fundamentals

- Next JS
- Gatsby
- TypeScript
- React Native
- Electron

### Important things to learn in Next.js

- File & Folder structure
- Static Site Generation
- Server Side Rendering
- Incremental Static Regeneration
- Dynamic Pages
- CSS / SASS Modules
- Lazy loading Modules
- API Routes

### Learn to test your React.js applications with some of these libraries/frameworks

- Jest
- Testing Library
- Cypress
- Enzyme
- Jasmine
- Mocha

### Learn to deploy your React.js applications

- Netlify
- Vercel
- Firebase
- GitHub Pages
- Heroku
- Render

## React.js Concepts

### Components

React JS is a component-based front-end library, which means that all parts of a
web application are divided into small components.

A component is a small piece of the user interface. Every React.js application
is a `tree of components`.

Components let you split the UI into independent, reusable parts. So when you're
building an application with React, you'll build independent and reusable
components, and then you'll combine them to build a full-fledged web
application.

Let’s take an example to represent what React.js components are:

[Filmpire - React.js Website](https://filmpire.netlify.app/)

This website is entirely built in React.js. So imagine we're building this
website. How would we make it?

Firstly, we’ll split the User Interface into small components like:

- Sidebar
- Search Bar
- Movie
- Single Movie Component
- Movie Name
- Movie Ratings

These components will then be assembled together to form the entire application.

> React components allow for maximum reusability, enabling developers to write
> cleaner code and manage applications more efficiently.

### React Components - Functional vs Class-Based

#### Class-Based Component

In React, there are two types of components: `Functional Components` and
`Class Components`.

Let’s first look at a `Class-Based Component`:

```javascript
import React, { Component } from "react";

class Example extends Component {
  render() {
    return <div>...</div>;
  }
}
```

If you're not familiar with classes, class methods, or what the `extends`
keyword means, don't worry! Class-based components are rarely used anymore.

They’ve been largely replaced by their simpler counterparts,
`Functional Components`.

> Although class components were used in the past, functional components with
> hooks have become the standard because of their simplicity and ease of use.

#### Functional Component

Now, let's take a look at a `Functional Component`:

```javascript
import React from "react";

const Example = () => {
  return <div>...</div>;
};
```

As you can see, functional components are simpler and more concise. They allow
you to build the same UI and manage the application state with hooks, making
them the preferred approach in modern React development.

> If you're starting with React, focus on learning functional components and
> hooks for a better development experience.

That's It! This is a React Component.

You can see how easy it is to create a React component. Here's an example:

```js
return <div>Hello World!</div>;
```

You might be wondering: Why are we writing HTML when returning something?

This tag syntax is neither a string nor HTML.

It is called `JSX` (JavaScript XML).

## JSX - JavaScript XML

JSX is a **syntax extension** to JavaScript. It is used in React to describe
what the UI should look like. While JSX may remind you of a template language,
it comes with the full power of JavaScript.

> Key Concept: JSX
>
> JSX produces React "elements" and forms the core syntax of React, allowing
> developers to define what the UI should look like with a blend of HTML-like
> syntax and JavaScript.

### Example: JSX in Action

Here's an example of JSX:

```js
return (
  <div className="greetings">
    <h1>Hello, {people.name}</h1>
  </div>
);
```

### Differences Between HTML and JSX

JSX is very similar to HTML, but there are some differences. For example:

- In JSX, you write `className` instead of `class`

> Why className?
>
> The word class is a reserved keyword in JavaScript. Since JSX is an extension
> of JavaScript, we use className instead.

### Reserved Keywords in JSX

Similar to how `class` is reserved in JavaScript, there's another reserved
keyword used in HTML: the f`or` attribute in the <label> element.

In JSX, you must use the attribute as `htmlFor` instead of `for`.

### JSX Example: Form with `htmlFor`

```javascript
return (
  <form className="form">
    <label htmlFor="name">Name</label>
    <input type="text" id="name" />
  </form>
);
```

### Single Parent Element Requirement

In JSX, your code must return a **single parent element**. If you don't, the
code will not compile.

You can achieve this by using either `<div>` elements or React `Fragments`.

- React Fragment: `<></>`
- Div: `<div>...</div>`

```javascript
return (
  <>
    <h1>Welcome</h1>
    <p>Thank you for joining us!</p>
  </>
);
```

### Why Use React Fragments?

React Fragments are not mandatory, but they help make the code more readable by
avoiding unnecessary `<div>` wrappers.

> Pro Tip: Cleaner Code
>
> Use React Fragments (<>...</>) to simplify your structure and reduce the
> number of unnecessary DOM elements.

### Using JavaScript in JSX

In JSX, you can directly implement JavaScript expressions by using **curly
brackets**: `{...}`.

This allows seamless integration of logic and dynamic content within your React
components.

#### Example: JavaScript in JSX

```javascript
return (
  <div>
    <h1>Hello, {prop.name}</h1>
    <p>{4 + 6} is ten</p>
  </div>
);
```

## What are Props?

To make our components accept different data, we use `props`. Props are
essentially arguments passed into React components. These arguments are provided
via **HTML attributes**.

### Key Points about Props

- Props is short for `Properties`.
- They are used to pass data from a `parent component` to a `child component`.
- Props are **read-only** and cannot be modified by the receiving component.
- You cannot pass data from a `child component` to a `parent component`.

#### Example: Passing Props

```javascript
function Welcome(props) {
  return <h1>Hello, {props.name}!</h1>;
}

// Using the component
<Welcome name="Adrian" />;
```

> Remember
>
> Props are immutable, which means a component cannot change the values received
> through props. If you need to modify data, use state.

## What is State?

State is a **plain JavaScript object** used by React to represent a piece of
information about the component's **current situation**. Think of it as the
component’s **memory**, where it keeps track of changes over time.

### Key Characteristics of State

- The `state object` is where property values specific to the component are
  stored.
- When the state changes, the component **automatically re-renders**.
- State is **managed within the component** (similar to variables in a
  function).
- State is **private** and cannot be accessed or modified from outside the
  component.
- Unlike `props`, `state` can be modified by the component itself.

#### Example: Using State

```javascript
import React, { useState } from "react";

function Counter() {
  const [count, setCount] = useState(0); // Initializing state

  return (
    <div>
      <p>Current count: {count}</p>
      <button onClick={() => setCount(count + 1)}>Increment</button>
    </div>
  );
}
```

> Pro Tip
>
> Use the useState hook to manage state in functional components. It provides a
> way to create and update state.

### State vs Props

- `State` is managed and updated by the component itself.
- `Props` are passed from a parent component and cannot be modified by the
  receiving component.
- While `state` is mutable, `props` are immutable.

## What are Events?

An `event` is an **action** triggered by the user or a system-generated
interaction. Examples include **mouse clicks, key presses, and other user
interactions**.

### Key Characteristics of Events in React

- React events are named using `camelCase` (e.g., onClick instead of onclick).
- With `JSX`, you pass a **function** as the event handler instead of a string.
- Handling events in React is similar to handling events in the DOM but follows
  React's syntax conventions.

#### Example: Adding an Event Handler

```javascript
const handleClick = () => {
  console.log("Button clicked!");
};

return <button onClick={handleClick}>Explore More</button>;
```

- Always use `functions` for event handlers to ensure proper behavior.
- Inline event handlers work, but defining them as separate functions makes your
  code cleaner and more reusable.

### How React Differs from HTML

- HTML:

```html
<button onclick="handleClick()">Click</button>
```

- React:

```javascript
<button onClick={handleClick}>Click</button>
```

## What are React.js Hooks?

`Hooks` were introduced in **React 16.8** to provide a cleaner way to use state
and other React features, such as lifecycle methods, within **functional
components**.

### Key Features of Hooks

- Hooks allow you to use `state` and `lifecycle methods` in **functional
  components**.
- They eliminate the need for `classes`, simplifying code and making it easier
  to manage.
- With hooks, you can consistently use `functions` without switching to classes,
  higher-order components, or render props.
- You can even create `custom hooks` to share stateful behavior between
  components.

### Why Use Hooks?

- Hooks make your code cleaner and easier to understand.
- They are widely adopted in modern React development.
- Custom hooks enable reusability of logic, reducing redundancy across
  components.

#### Example: A Simple Hook

```javascript
import React, { useState } from "react";

const Counter = () => {
  const [count, setCount] = useState(0); // Using the useState Hook

  return (
    <div>
      <p>Count: {count}</p>
      <button onClick={() => setCount(count + 1)}>Increment</button>
    </div>
  );
};

export default Counter;
```

- Always call hooks at the **top level** of your components (not inside loops,
  conditions, or nested functions).
- Follow the **Rules of Hooks** to avoid unexpected behavior.
