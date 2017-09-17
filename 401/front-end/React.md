# React

## Resources
* [Connecting your React Components with Redux: Daily JS](https://medium.com/dailyjs/quick-redux-tips-for-connecting-your-react-components-e08da72f5b3)
* [React Docs](https://facebook.github.io/react/docs/hello-world.html)

## React Basics
* virtual Dom
* Immutable Data
* Components
    * Lifecycle methods
* State
    * Source of truth
* Testing
    * Snapshot, Jest

## React/Redux
* **connect**
    * Common mistake is to connect your top level components to the store
    * Why is this bad?
        * **Page** consists of Profile, Feedlist, Image, if Page is connected to the store, ALL of these components will always be updated even if only one is modified. 
        * Connect Profile, Feedlist and Image to the store to create their own slice of **state**.
    * **connect at the lower levels to avoid unnecessary rerenders**
* [Avoiding Deeply Nested Component Trees](https://medium.com/@RubenOostinga/avoiding-deeply-nested-component-trees-973edb632991)
    * "In essence your component has multiple responsibilities. Next to its regular task of showing UI it is also passing data to its children. When we avoid this we can follow the single responsibility principle! A component is either passing data to child components OR it is rendering data to the screen."
    * Pass components down, not data
        * Using child components, make container components that are reusable

