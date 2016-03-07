What is it?
- open-source JavaScript library
- provides a view for data rendered as HTML.
- typically rendered using components that contain additional components
- 9th most starred project of all time on GitHub

Notable features
- One-way data flow
  - Properties, a set of immutable values, are passed to a component's renderer as properties in its HTML tag. 
  - A component cannot directly modify any properties passed to it, but can be passed callback functions that do modify values.
  - This mechanism's promise is expressed as "properties flow down and actions flow up".
  - For example, a shopping cart component might include multiple product line components. Rendering a product line uses only the properties passed to it and cannot affect the shopping cart's total due. However, the product line could be passed a callback function as a property which would be called when a 'delete this product' button was pushed and that callback function could affect the total due.
- Virtual DOM
  - React creates an in-memory data structure cache, computes the resulting differences, and then updates the browser's displayed DOM efficiently.
  - This allows the programmer to write code as if the entire page is rendered on each change while the React libraries only render subcomponents that actually change.
  - For example, a shopping cart component would be written to render the entire shopping cart on any change of data. If a product line subcomponent had no changes to the properties, a cached rendering would be used.
  - This means the relatively slow full update to the browser's DOM would be avoided. Alternately, if the product line quantity had changed, the product line subcomponent would be rendered; the resulting HTML might differ in only one node, and only that node would be updated in the DOM.
- JSX
  - A JavaScript extension syntax allowing easy quoting of HTML and using HTML tag syntax to render subcomponents.
  - React components are typically written in JSX.
  - HTML syntax is turned into JavaScript calls of the React library. Developers may also write in pure JavaScript.
