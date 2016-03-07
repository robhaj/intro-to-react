- This is an intro to handling events in React
- There are two steps
  - First we declare an event handler, a function that runs whenever the event occurs.
  - Second, pass the event handler to the element we want to monitor for events.
- Here we want to an event to fire whenever a user types into the search bar.
  - Add a method to the SearchBar component called onInputChange.
```javascript
class SearchBar extends Component {
  render() {
    return <input />;
  }

  onInputChange() {
    // code here
  }
}
```
- All HTML elements have an onChange property.
- In our render method, add the onChange property to the input element and set the value to {this.onInputChange}
```javascript
render() {
  return <input onChange={this.onInputChange} />;
}
```
- Our onInputChange method will take the event object as a parameter.
- We can use this event object to get the value of the input.
```javascript
onInputChange(event) {
  console.log(event.target.value)
}
```
This should console log what ever is type into the input.
