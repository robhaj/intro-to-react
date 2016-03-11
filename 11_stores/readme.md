## Stores

- The Store is the object that brings them together. The store has the following responsibilities:
  - Holds application state;
  - Allows access to state via getState();
  - Allows state to be updated via dispatch(action);
  - Registers listeners via subscribe(listener);
  - Handles unregistering of listeners via the function returned by subscribe(listener).

In the previous sections, we defined the actions that represent the facts about “what happened” and the reducers that update the state according to those actions.
