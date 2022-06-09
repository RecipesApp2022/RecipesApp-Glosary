# Recipes App Glossary

First Header  | Second Header
------------- | -------------
01  | What is React?
02  | What are the major features of React?
03  | What is JSX?
04  | How to create components in React?
05  | 
06  | 
07  | 
08  | 
09  | 
10  | 
11  | 
12  | 
13  | 
14  | 
15  | 
16  | 
17  | 
18  |
19  | 
20  | 
21 | 
22  | 
23  | 
24  | 
25  | 
26  | 
27  | 
28  | 
29  |
30  | 
31  | 
32  | 
33  | 
34  | 
35  | 
36  | 
37  | 
38  | 
39  | 
40  |
41  | 
42  | 
43  | 
44  | 
45  | 
46  | 
47  | 
48  | 
49  | 
50  | 
51  |
52  | 
53  | 
55  | 
56  | 
57  | 
58  | 
59  | 
60  | 
61  | 
62  | 
63  |
63  | 
64  | 
65  | 
66  | 
67  | 
68  | 
69  | 
70  | 
71  | 
72  | 
73  |
74  | 
75  | 
76  | 
77  | 
78  | 
79  | 
80  | 
81  | 
82  | 
83  | 
84  |
85  | 
86  | 
87  | 
89  | 
90  | 
91  | 
92  | 
93  | 
94  | 
95  | 
96  |
97  | 
98  | 
99  |
100  |
101  | 
102  | 
103  | 
104  | 
105  | 
106  | 
107  | 
108  | 
109  | 
110  | 
111  | 
112  | 
113  | 
114  | 
115  | 
116  | 
117  | 
118  |
119  | 
120  | 
121 | 
122  | 
123  | 
124  | 
125  | 
126  | 
127  | 
128  | 
129  |
130  | 



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


## What is state in React?

State of a component is an object that holds some information that may change over the lifetime of the component. We should always try to make our state as simple as possible and minimize the number of stateful components.

Let's create a user component with message state,

´´´bass

class User extends React.Component {
  constructor(props) {
    super(props)

    this.state = {
      message: 'Welcome to React world'
    }
  }

  render() {
    return (
      <div>
        <h1{this.state.message}/h1>
      </div>
    )
  }
}
´´´

[Subir](#top)
