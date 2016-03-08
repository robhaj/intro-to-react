# Hello World in React.JS
Follow the steps to install the generator @ [generator-galvanize-react](https://github.com/robhaj/generator-galvanize-react)
- Take a look at the index.html file, you'll notice bundle.js being linked in.
  - Webpack bundles our files into one file called bundle.js before build.
- Take a look inside the components folder and you'll find an app.js file.
- When we write React code we write individual components.
  - Components are collections of javascript functions that produce HTML.
  - You can nest components inside each other.
- Don't be alarmed at errors, React does a great job of telling you exactly what is not working.
- We will be recreating the boilerplate from scratch so you understand what each file is doing.
  - Delete the src folder
  - Make a new folder called src and add a file called index.js inside.
  - Inside of index.js

```javascript
import React from 'react';
import ReactDOM from 'react-dom';

const App = () => {
  return <div> Hello World! </div>;
}

ReactDOM.render(<App />, document.querySelector('.container'))
```

Run `npm start` and you should see 'Hello World' on the page.


## Breaking it down

```javascript
var React = require('react');
var ReactDOM = require('react-dom');
```
`Const` is also ES6 syntax. It is a variable who's value doesn't change once set, or it is constant.
The `=>` is also ES6.
Instead of
```javascript
const App = function() {
  return <div> Hello World! </div>
}
```
We can write
```javascript

const App = () => {
  return <div> Hello World!< /div>
}
```
The keyword function is removed, the parentheses containing parameters stays and we add a fat arrow in between the parentheses and the function body.
