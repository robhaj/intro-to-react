## Refactoring Functional to Class-based
- We are refactoring our functional app component to be class-based
- We want to use state here because there is some data that will change over time and we want to persist that data.
- Our list of videos will change over time
  - Right now its 5 videos but when users enter in a search input we want to have the new videos render
  - This is a perfect use of state.
- Let's define our constructor functional.
  - Like before, we pass in props to our constructor, and in the constructor function body we call `super()` on props.
 - We then initialize our state, and set it equal to an object.
 - In our state object, let's add a key of videos and set it equal to an empty array.

- Our app component i
- When it is first rendered, it does a search for surfboards and sets the state to the video data that is returned.

## Video list
- This component could probably be a functional component, since I can't think of any use for state.
- Define a VideoList component and just have it return a ul element.
- This list is a visual component, so lets add some classes to leverage bootstrap's built in styling classes.
- We know have a functional video list component, and it renders a list of videos.
- Our video list component receives props which contains an array of videos.
- Let's loop over our array
  - Instead of using JS built in `for()` loops, we will be using the built-in iterator `.map`
  - [Map](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map)
