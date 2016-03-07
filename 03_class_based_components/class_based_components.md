- Here we will be refactoring our functional component into a class based component.
- When we write a class based component, we must always define a render method.
- When to use class based component vs functional component
  - Start with a functional component, if you find yourself needing additional functionality, make it a class based component
- Previously, our SearchBar component was a functional component, we will be changing it to a class based component.
- Functional Component
```javascript
import React from 'react';

const SearchBar = () => {
  return <input />;
}
```

To make this a class based component, we will use the ES6 keyword class. We use the keyword extends to extend the functionality of Component from React to our SearchBar component. Our import statement takes advantage of ES6 syntactic sugar by saying
```javascript
import React, {Component} from 'react'
```
This is identical to saying
```javascript
const React = require('react');
const Component = React.Component;
```
Instead of assigning the component to a constant, we use the keywords class and extends.
Class Based Component
```javascript
import React, { Component } from 'react';

class SearchBar extends Component {
  render() {
    return <input />;
  }
}
```
