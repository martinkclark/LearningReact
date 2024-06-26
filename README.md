# LearningReact

This is a repository for learning React.js , React create SPA (Single Page Application) and React is a library for building user interfaces.

## Day 1 4/3/2024

### Code to create vite project and normal react project

```jsx
//vite project
npx create vite@latest
//normal react project
npx create-react-app my-react-project
```

### What is vite and parcel

Vite is a bundler (bhaut sare file me js likhte hai usko ekk file me convert karta hai)

### What is React

React is a library for building user interfaces
![alt text](image.png) (React-dom for web and React-native for mobile app)

TO build a react project :

## Day 2 5-03-2024

### What is differnce in JS and JSX and why it is necessary to name component file in vite .jsx extension.

Jsx is a syntax extension for javascript. It is used with React componenets. It is not necessary to use .jsx extension for vite file but it is recommended to use it.

### some convetions in vite

1. first letter should be captial in component name
2. while importing a component, it should be also first letter captial
   ex
   import Chai from './Chai.jsx';
3. component name should be name with jsx extension

### Frangments in react

Fragments let you group a list of children without adding extra nodes to the DOM.
//frangments syntax

```jsx
<>
  <h1>hello</h1>
  <h2>world</h2>
</>
```

### React kya krta hai ekk root create krta hai aur uske andar sare component ko render krta hai

, basically wo <App/> component ko render krta hai jo ki ekk js or jsx file hota hai jisme ekk function hota hai jo ki html ko export krta hai.

### How objects are created in javascript

there are two ways to create object in javascript

1. using object literal syntax
2. using object constructor syntax

```jsx
//object literal syntax
let person = {
  name: "john",
  age: 30,
};

//object constructor syntax
let person = new Object();
person.name = "john";
person.age = 30;
```

second method is not recommended because it is slow and singelton object is created in this method. (singelton object is a object which is created only once and used everywhere in the code by creating private constructor and static method to create object of the class so that only one object is created and used everywhere in the code.)

### variables in javascript

A variable can appear to be used before it's declared. This behavior is called hoisting, as it appears that the variable declaration is moved to the top of the function or global code.

### React createElement syntax and example ans order of parameters

```jsx
//example
React.createElement("h1", { className: "greeting" }, "Hello, world!");
```

order of parameters

1. type
2. props or null
3. children (ie. text or other elements)

### How to pass js in jsx

```jsx
//syntax
const name = "Josh Perez";
const element = <h1>Hello, {name}</h1>;
```

{} is used to pass js in jsx
called evaluated expression which is evaluated and then passed to jsx so you can't use directly if else or for loop in it.

### Babel and JSX

We use Babel with React to transpile (ie converts source code from a programming language into an equivalent source code of the same or a different programming language. ) the JSX code into simple React functions that can be understood by browsers. Babel is a JavaScript compiler that can convert markup language into JavaScript.

## Day 3 6-03-2024

### Hooks in react

Hooks are used to sync the variable state with the UI. It is used to update the state of the varible everywere , it is used in the code

syntax of hooks

```jsx
import React, { useState } from "react";
function Example() {
  // Declare a new state variable, which we'll call "count"
  const [count, setCount] = useState(0); //here count is the variable and setCount is the function to update the state of the variable count and 0 is the initial value of the variable count
  return (
    <div>
      <p>You clicked {count} times</p>
      <button onClick={() => setCount(count + 1)}>Click me</button>
    </div>
  );
}
```

useState is a hook which is used to update the state of the variable. It is used to update the state of the variable everywere it is used in the code.

## Day 4 7-03-2024

### Vertual dom

The virtual DOM (VDOM) is a programming concept where an ideal, or “virtual”, representation of a UI is kept in memory and synced with the “real” DOM by a library such as ReactDOM. This process is called reconciliation.
and mapping of the real dom is done with the virtual dom and replacing the only those elements which are in vitual dom and not in real dom.

### reconciliation

Reconciliation is the process through which React updates the DOM. When a component’s state changes, React has to update the component’s rendered view. This process is called reconciliation.

### What is rendering and re rendering and async rendering in react

Rendering is the process of generating the UI (User Interface) of a React application based on the current state and props of its components (simply, A fancy word to say converting react code to visual layout). Re-rendering occurs whenever a component's state or props change, causing React to update the UI to reflect these changes. Async re-rendering means consider a situtation when rendering process is still going on but before it completes, some asynchronous operation (such as a data fetch, callback from an event, etc.)
causes the component to re-render before the first render completes.
Async re-rendeing occurs due to non-blocking nature of javascript and how react renders the component. It may somteimes leads to unexpected behaviour or problems in the application.
That's why React's strict mode runs the component twice to check for any unexpected behaviour or problems in the application and to avoid async re-rendering.

### What is concept of batch in react

Batching is the process of putting multiple updates into a single update. It is used to avoid the multiple re-rendering of the component. It is used to update the state of the variable only once in the component.

### How react able to create SPA(Single Page Application)

React is able to create SPA because of its virtual dom and reconciliation process. It is able to create the single page application by mapping the virtual dom with the real dom and replacing the only those elements which are in vitual dom and not in real dom.

### What is createRoot in react and how it is related to virtual dom and rendering in react

createRoot is used to create a root for the virtual dom and it is used to render the virtual dom to the real dom.

## Day 5 8-03-2024

### Tailwind CSS and how to install it in vite project

See Tailwind website for installation of tailwind in vite project

### What is props and how to pass props in react

Props is a special keyword in React that stands for properties and is used for passing data from one component to another.

Props are used to pass the data from HTML tag in main.jsx to the component (ex app.jsx or customMade.jsx).


Example :

```jsx
//main.jsx
import React from "react";
import ReactDOM from "react-dom";
import App from "./App.jsx";
ReactDOM.render(<App name="Chai" />);

//App.jsx
import React from "react";
function App(props) {
  return (
    <div>
      <h1>Hello, {props.name}</h1>
    </div>
  );
}
```

In this example, name is passed from main.jsx to App.jsx using props.

## Day 6 9-03-2024

### Created Project of changing bg color with button

### What is Hover, active and focus in tailwind css

Hover, active and focus are the classes in tailwind css which are used to change the color of the element when it is hovered, clicked or focused. Hover means when the mouse is hovered on the element, active means when the element is clicked(upto the time when button is pressed and stope when button released) and focus means when the element is focused or after clicked.

## Day 7 10-03-2024 - (Created Password generator project)

### Functions and refference of function in javascript example

### Arrow function

Arrow functions have a few key differences from traditional function expressions:

Concise Syntax:

Arrow functions have a more concise syntax compared to traditional functions, especially for simple one-liner functions.
Lexical this Binding:

Arrow functions do not bind their own this value. Instead, they inherit this from the surrounding lexical context (the enclosing scope).
This behavior is particularly useful when working with callbacks or event handlers, as it eliminates the need to manually bind this or use workarounds like storing this in a variable (const self = this;).
No arguments Object:

Arrow functions do not have their own arguments object. If you need access to function arguments, you should use the rest parameters syntax (...args) instead.
No new.target Binding:

Arrow functions do not have their own new.target binding. This means they cannot be used as constructor functions with the new keyword.
[link for more](https://www.freecodecamp.org/news/the-difference-between-arrow-functions-and-normal-functions/)  

### event object in javascript

The event object is always passed to the event handler as the first parameter. The event object is a built-in object in JavaScript that contains information about the event, particularly the element that the event occurred on (target) and the type of event that occurred.

### useEffect in react and how to use it

useEffect is a hook which is used to run the code after the component is rendered. It is used to run the code after the component is rendered and it is used to run the code after the component is updated.

//sytax

```jsx
useEffect(() => {
  //code to run after the component is rendered
}, []);
```
### useref in react and how to use it

useRef is a hook which is used to create a reference of the element. It is used to create a reference of the element and it is used to access the element in the code. 

//syntax

```jsx
const inputRef = useRef();
```
//example

```jsx
import React, { useRef } from "react";
function App() {
  const inputRef = useRef();
  return (
    <div>
      <input type="text" ref={inputRef} />
      <button onClick={() => inputRef.current.focus()}>Focus</button>
    </div>
  );
}
```

In this example, inputRef is used to create a reference of the input element and inputRef.current.focus() is used to focus the input element which means the cursor is placed in the input element.

### usecallback in react and how to use it

useCallback is a hook which is used to create a memoized callback. It is used to create a memoized callback and it is used to avoid the re-rendering of the component.

//syntax

```jsx
const memoizedCallback = useCallback(() => {
  //code to run
}, []);
```

### Why functions run twice in react

Its because your app component is a wrap in StrictMode.

```jsx
<React.StrictMode>
  <App />
</React.StrictMode>,
```

StrictMode is a tool for highlighting potential problems in an application. Like Fragment, StrictMode does not render any extra DOM elements. It is used to check for the unexpected behaviour or problems in the application and to avoid the async re-rendering.

### Why arrow function is used for event handler in react and not normal function , Or when to use arrow function and when to use normal function in react ?

## Day 8 13-03-2024 (Currency Convertor Project)

### Lifecycle of react elements

Lifecycle of react elements is the process of creating, updating and destroying the react elements. It is used to create the react elements, update the react elements and destroy the react elements. 

1. Mounting (i.e creating the react elements and inserting them into the DOM )
2. Updating (i.e updating the react elements and re-rendering them in the DOM )
3. Unmounting (i.e destroying the react elements and removing them from the DOM )x

### Arrow function and This

// syntax
```js
function name_of_function(){}
//arrow function analog

const name_of_function = () => {}

```
//difference

```js
() => {
  console.log(this)
}
//this will always return the empty object

function temp()
{
  console.log(this);
}
  //this always return the all global object under the scope of in which this function exists

```
### Restrictions on hooks in react

1. Hooks can't be called inside the loops, conditions or nested functions.
2. Hooks can't be nested inside the other hooks.
3. Hooks can't be called from the regular javascript functions.

### Fetch API in javascript

The Fetch API provides a JavaScript interface for accessing and manipulating parts of the HTTP pipeline, such as requests and responses. It also provides a global fetch() method that provides an easy, logical way to fetch resources asynchronously across the network. It is a asynchronous function which is used to fetch the data from the server.

.then() is used to handle the response of the fetch api. it is a promise which is used to handle the response of the fetch api. (promise : A promise is an object representing the eventual completion or failure of an asynchronous operation. In simple words, it is a placeholder for the result of an asynchronous operation which is not yet available but will be available in the future and may be available or not in the future in the form of resolved or rejected.)

//syntax

```js
fetch('url')
  .then(response => response.json())
  .then(data => console.log(data));
```

## Day 9 19-03-2024 (React router and project on that concepts)

### Some Technical terms in react router

#### -> What is Routing

Routing refers to the process of determining what content to display based on the URL of a web page. It is used to navigate from one page to another page in the web application.

#### -> Client Side Routing


Client-side routing refers to the process of managing navigation within a web application entirely on the client side, without needing to make requests to the server for each new page or URL. In traditional web applications, when a user navigates to a new page or URL, the browser sends a request to the server, which responds by sending back a new HTML page. This process involves reloading the entire page, resulting in a noticeable delay and a less fluid user experience.
React do client side routing by using react-router-dom package.

### Why react-router-dom come into pictures

Here's why React Router comes into the picture and how it solves the related problems:

- Client-Side Routing: React applications often handle navigation and rendering on the client side without reloading the entire page. React Router enables developers to manage client-side routing in a declarative way, allowing them to define how the UI should change in response to different URLs.

- URL-Based Navigation: With React Router, developers can define routes for different URLs and specify which components to render when those URLs are matched. This makes it easy to create complex, multi-page user interfaces while still maintaining the single-page application paradigm.

- Nested Routing: React Router supports nested routing, allowing developers to define routes within routes. This is useful for creating modular and reusable components that can be composed together to build complex UIs.

- Dynamic Routing: React Router supports dynamic routing, where routes can be generated based on data or user input. This is useful for applications with dynamic content or when the number of routes is not known in advance.

- History Management: React Router provides tools for managing browser history, including support for browser history API and features like programmatic navigation, redirection, and URL parameter parsing.

React Router is called a "router" because it manages the routing of the application, determining which components to render based on the current URL. It essentially acts as a traffic controller, directing users to different parts of the application based on their navigation actions. The term "router" is borrowed from traditional web development, where routers are used to direct network traffic between different parts of a network. Similarly, in the context of web applications, routers direct user traffic between different parts of the application based on the URL.

### So how the client side routing happen and how does server come to know about url change

In SPA the entire application is loaded once initially, and subsequent navigation between different views or pages within the application happens dynamically within the same page without full page reloads. In a typical client-side routing scenario, where a React single-page application (SPA) is being used, the server doesn't directly detect URL changes because the server is typically responsible for serving the initial HTML, CSS, and JavaScript files required to bootstrap the application. Once the initial files are loaded, subsequent navigation within the application is handled entirely on the client side, without needing to communicate with the server for each URL change. So , When a user navigates to a different URL within the SPA, the client-side routing logic (e.g., React Router) updates the browser's URL using JavaScript's history API, and it also updates the view based on the URL route. However, this navigation process doesn't involve making a new request to the server for each URL change, as the necessary resources have already been loaded when the SPA was initially loaded.


### How to use react-router-dom in react

```npm install react-router-dom```

### Event handler and Event listener difference

An event in JavaScript is an action that occurs when the user interacts with a web page. Events can be triggered by the user, such as clicking a button, or by the browser, such as when a page loads.

There are two ways to handle events in JavaScript:

1. Event Handlers: To use an event handler, use one of the EventHandler properties of an object. Here is an example of using one called onclick.
```js
const button = document.querySelector(".btn")

button.onclick = () => {
  console.log("Button clicked.");
};
```
The onclick event handler is triggered when a user clicks on a button. As a result, "Button clicked." is output into the console.

2. Event Listeners: The other option to handling events is by using event listeners. An event listener is something you assign to an object. As the name suggests, the event listener listens for events and gets triggered when an event occurs.

Let’s repeat the previous example by assigning an event listener to a button to listen for clicks.

```js
const button = document.querySelector(".btn")

button.addEventListener("click", () => {
  console.log("Button clicked.");
})
```

Key Differences Between Event Handlers and Event Listeners

1. Event handlers are properties of an object, while event listeners are methods.

2. Event handlers can only be assigned to one event at a time, while event listeners can be assigned to multiple events.
example : 
```js
const button = document.querySelector(".btn")

button.onclick = () => {
  console.log("Button clicked.");
};

button.onclick = () => {
  console.log("Button clicked again.");
};
```

In this example, the second onclick event handler overwrites the first one. As a result, only "Button clicked again." is output into the console.

```js

const button = document.querySelector(".btn")

button.addEventListener("click", () => {
  console.log("Button clicked.");
})

button.addEventListener("click", () => {
  console.log("Button clicked again.");
})
```

In this example, both event listeners are triggered when the button is clicked. As a result, "Button clicked." and "Button clicked again." are output into the console.

3. Event Handlers: Removing event handlers can be tricky and may require setting the event handler to null.
addEventListener: Provides a straightforward method, removeEventListener, to remove specific event listeners when they are no longer needed, example : 
```js
const button = document.querySelector(".btn")

const handleClick = () => {
  console.log("Button clicked.");
}

button.addEventListener("click", handleClick)

button.removeEventListener("click", handleClick)
```


### React Router Dom 

- DOM (Document Object Model)  History API is a set of methods and properties provided by modern web browsers that allow JavaScript to interact with the browser's history stack. It enables developers to manipulate the browser's history, navigate between different pages, and manage the session history (the list of visited pages).

- CreateBrowserRouter : This is the recommended router for all React Router web projects. It uses the DOM History API to update the URL and manage the history stack.

## Day 10 21-03-2024 (Context Api and its concept)

### Problem of prop drilling in react

Prop drilling is a common problem in React applications where props are passed down through multiple levels of components since React components are organized in a hierarchical structure, where parent components can pass data to their child components using props .Which leads to increase in the complexity of the code and makes it difficult to manage the state of the variable.
### And there are Many ways to solve this problem using : 
- Context API(Which is mainly built for react and not exist for other libraries) 
- Redux library(Whis is a standalone library So, React user use Rect-Redux and other version of react also exist called Redux Toolkit (RTK) ) .
- Zustand library(Which is a standalone library) Which is also used for state management in react (State is fancy term for variable or data structre).
- Mobx library(Which is a standalone library) is also used for state management in react. 
- Recoil library(Which is a standalone library) is also used for state management in react.

This problem is not new it also exists in libraries before react like Angular js, vue js, backbone js .

And we will study context api because it is inbuilt in react and not need to install any library for that and not exists in other libraries like angular js, vue js , backbone js.

### What is Context API 

Context provides a way to pass data through the component tree without having to pass props down manually at every level.





