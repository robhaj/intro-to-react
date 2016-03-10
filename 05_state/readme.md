## State

- State is one of the most confusing concepts to grasp but is probably the most important.
- State is a plain javascript object that is used to record and react to user events.
- Each class based component that we define has its own state object.
- Anytime the component's state object is changed, the component is re-rendered, along with all of its children (nested components).

## Getting Started
- We need to initialize the state object for our SearchBar component.
```javascript
class SearchBar extends Component {
  constructor(props) {
    super(props);

    this.state = { term: ''};
  }
  render() {
    return <input onChange={event => console.log(event.target.value)} />
  }
}
```
- This is how we initialize state in class based components. Functional components do not have state.
- All javascript classes have a special function called constructor. It is the first and only function called automatically whenever a new instance of the class is created.
- This function is reserved for setting up our class component.
- Since Component itself, has its own constructor function, we have to call the parent method on the parent class.
  - When we define a method that is already defined on the parent class (Component), we can call that parent method by calling `super()``
  - We then set our state object's initial value.
  - The only time we call `this.state` and set it equal to an object, is in our constructor function.
  - Any other time we need to manipulate state we use `this.setState`

```javascript
import React, { Component } from 'react';

class SearchBar extends Component {
  constructor(props) {
    super(props);

    this.state = { term: ''};
  }

  render() {
    return (
      <div>
        <input
          value= {this.state.term}
          onChange={event => setState({term: event.target.value})} />
        Value of the input: {this.state.term}
      </div>
    );
  }
}

export default SearchBar;
```
