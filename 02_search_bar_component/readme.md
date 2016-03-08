- Here we will be adding a search bar component to our app
- In components, add a file called search_bar.js
- Add the following
```javascript
import React from 'react';

const SearchBar = () => {
  return <input />;
}
```
- Since our app component lives elsewhere, we also need to export our component by typing
```javascript
export default SearchBar
```

In index.js, we need to import our SearchBar component
```javascript
import SearchBar from './components/search_bar';
```

We now use the SearchBar component inside the app component by adding `<SearchBar />` to the JSX.
