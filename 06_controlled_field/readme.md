## Controlled Fields

- A controlled field is a form element, like an input, who's value is set by the state, not the other way around.
- Right now, whenever our input changes, it causes our state to be updated.
- The input changing tells the state 'hey, you need to change!'
- In an ideal situation, the state should tell the input what the value should be.
- Add another property called value to the input field.
- Set the value equal to `{this.state.term}`

```javascript
import React, {Component} from 'react';

class SearchBar extends Component {
  constructor(props) {
    super(props);

    this.state = { term: ''};
  }

  render() {
    return (
      <div>
        <input
          value={this.state.term}
          onChange={event => this.setState({term : event.target.value })} />
      </div>
    );
  }
}
```
- When we tell the input it's value is provided by this.state.term, it's now a controlled component.
  - Controlled components have their value set by state, it only ever changes when the state changes.
- Before we had the input telling the state it needs to changes.
  - Here, the input changes, it tells the state here's the new value.
- `this.setState` causes the component to re-render, and when it re-renders, the value of the input is set to the new value of `this.state.term`
- Here is a walkthrough of what is happening.
  1. Our app starts up and renders and instance of SearchBar.
  1. In SearchBar, a new instance is created, the constructor is called and this.state is initialized with term equal to an empty string.
  1. The component renders, the value of the input is set to retrieve its value from this.state.term
    - its initial value is an empty string
    - once a user enters some text, the state is updated to the changed text value.
    - at this time the value of the input has not changed. the event handle
    - Whenever `setState` is called our component is re-rendered.
  1. The render function is called again
  1. The value of the input is updated to receive the new value of this.state.term
  1. Finally the component finishes rendering, and the new value of the input is on the screen.

## WrapUp
- Now, when a user types something, they are not changing the input value, they are updating the state which causes the component to re render with the new value.
- In react, this how we treat data.
  - We don't have an imperative flow of data, we have a more declarative syntax.
- Controlled components is one of the most confusing and most important concepts of state.
