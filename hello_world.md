# Hello World in React.JS
Follow the steps to install the generator @ [generator-galvanize-react](https://github.com/robhaj/generator-galvanize-react)
Take a look at the index.html file
You'll notice bundle.js being linked in. Webpack bundles our files into one file called bundle.js before build.
Take a look inside the components folder and you'll find an app.js file.
Try changing the text inside the div that is returned from the render function and see how that changes what you see on the screen.
We will be recreating the boilerplate from scratch so you understand what each file is doing.
Delete the src folder
Make a new file called src and add a file called index.js inside.
When we write React code we write individual components. Components are collections of javascript functions that produce HTML.
You can nest components inside each other.
Don't be alarmed at errors, React does a great job of telling you exactly what is not working.
Inside of index.js

```javascript
// Create a new component
const App = function() {
  return <div>Hi!</div>;
}
// Put component on DOM
```
