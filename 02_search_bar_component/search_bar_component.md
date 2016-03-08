- Here we will be adding a search bar component to our app
- In components, add a file called search_bar.js
- Add the following
```javascript
import React from 'react';

const SearchBar = () => {
  return <input />;
}
```
- We also need to export our component by typing
```javascript
export default SearchBar
```
In index.js, we need to import our SearchBar component
```javascript
import SearchBar from './components/search_bar';
```
Here we changed
```javascript
<div> Hello World! </div>
```
to
```javascript
<input />;
```
This just changes the HTML that is rendered from Hello World inside a div tag, to an input tag.
We then export our component, import it in our other file, and include it inside our App component
