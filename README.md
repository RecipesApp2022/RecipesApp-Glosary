# Recipes App Glossary

First Header  | Second Header
------------- | -------------
01  | What is React?
02  | What are the major features of React?
03  | What is JSX?
04  | How to create components in React?
05  | When to use a Class Component over a Function Component?
06  | What is the difference between HTML and React event handling?
07  | Content Cell
08  | Content Cell
09  | Content Cell
10  | Content Cell
11  | Content Cell
12  | Content Cell
13  | Content Cell
14  | Content Cell
15  | Content Cell
16  | Content Cell
17  | Content Cell
18  | Content Cell
19  | Content Cell
20  | Content Cell



## What is React?

React is an open-source front-end JavaScript library that is used for building user interfaces, especially for single-page applications. It is used for handling view layer for web and mobile apps. React was created by Jordan Walke, a software engineer working for Facebook. React was first deployed on Facebook's News Feed in 2011 and on Instagram in 2012.

[Subir](#top)

## What are the major features of React?

The major features of React are:

It uses VirtualDOM instead of RealDOM considering that RealDOM manipulations are expensive.
Supports server-side rendering.
Follows Unidirectional data flow or data binding.
Uses reusable/composable UI components to develop the view.

[Subir](#top)


## What is JSX?

JSX is a XML-like syntax extension to ECMAScript (the acronym stands for JavaScript XML). Basically it just provides syntactic sugar for the React.createElement() function, giving us expressiveness of JavaScript along with HTML like template syntax.

In the example below text inside h1
tag is returned as JavaScript function to the render function.

[Subir](#top)

## How to create components in React?

There are two possible ways to create a component.

Function Components: This is the simplest way to create a component. Those are pure JavaScript functions that accept props object as the first parameter and return React elements:
  
```bass
function Greeting({ message }) {
  return <h1>{`Hello, ${message}`}</h1>

}
Class Components: You can also use ES6 class to define a component. The above function component can be written as:

class Greeting extends React.Component {
  render() {
    return <h1>{`Hello, ${this.props.message}`}</h1>
  }
}
  
```
  
[Subir](#top)


## When to use a Class Component over a Function Component?

If the component needs state or lifecycle methods then use class component otherwise use function component. However, from React 16.8 with the addition of Hooks, you could use state , lifecycle methods and other features that were only available in class component right in your function component. *So, it is always recommended to use Function components, unless you need a React functionality whose Function component equivalent is not present yet, like Error Boundaries *

[Subir](#top)

## What is the difference between HTML and React event handling?

Below are some of the main differences between HTML and React event handling,

In HTML, the event name usually represents in lowercase as a convention:

```bass 
<button onclick='activateLasers()'>
Whereas in React it follows camelCase convention:

<button onClick={activateLasers}>
In HTML, you can return false to prevent default behavior:

<a href='#' onclick='console.log("The link was clicked."); return false;' />
Whereas in React you must call preventDefault() explicitly:

function handleClick(event) {
  event.preventDefault()
  console.log('The link was clicked.')
}
  
```
In HTML, you need to invoke the function by appending () Whereas in react you should not append () with the function name. (refer "activateLasers" function in the first point for example)

[Subir](#top



