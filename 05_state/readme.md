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
- All javascript classes have a special function called constructor. It is the first and only called automatically whenever a new instance of the class is created.
- This function is reserved for setting up our class.
- Component itself, has its own constructor function.
  - When we define a method that is already defined on the parent class (Component), we can call that parent method by calling super()
  - We then set our state object's initial value.

```javascript
class SearchBar extends Component {
  constructor(props) {
    super(props);

    this.state = { term: ''};
  }
  render() {
    return <input onChange={event => setState({term: event.target.value})} />
  }
}
```
