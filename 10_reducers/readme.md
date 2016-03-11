## Reducers

- Reducers

  - Actions describe the fact that something happened, but don’t specify how the application’s state changes in response. This is the job of a reducer.

### Designing the State Shape

- In Redux, all application state is stored as a single object. It’s a good idea to think of its shape before writing any code. What’s the minimal representation of your app’s state as an object?

- For our todo app, we want to store two different things:

  - The currently selected visibility filter;
  - The actual list of todos.

### Handling Actions

- Now that we’ve decided what our state object looks like, we’re ready to write a reducer for it. The reducer is a pure function that takes the previous state and an action, and returns the next state.

- It’s called a reducer because it’s the type of function you would pass to Array.prototype.reduce(reducer, ?initialValue).
- It’s very important that the reducer stays pure.

- Things you should never do inside a reducer:

  - Mutate its arguments
  - Perform side effects like API calls and routing transitions;
  - Calling non-pure functions, e.g. Date.now() or Math.random().

  We don’t mutate the state. We create a copy with Object.assign(). Object.assign(state, { visibilityFilter: action.filter }) is also wrong: it will mutate the first argument. You must supply an empty object as the first parameter. You can also enable the object spread operator proposal to write { ...state, ...newState } instead.

  We return the previous state in the default case. It’s important to return the previous state for any unknown action.

- Object.assign() is a part of ES6, but is not implemented by most browsers yet. You’ll need to either use a polyfill, a Babel plugin, or a helper from another library like _.assign().

- Note that todos also accepts state—but it’s an array! Now todoApp just gives it the slice of the state to manage, and todos knows how to update just that slice. This is called reducer composition, and it’s the fundamental pattern of building Redux apps.
