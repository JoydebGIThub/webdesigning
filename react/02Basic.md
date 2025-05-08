## Q: What is Arrow Function Expression in JSX?
Ans: The arrow function expression syntax is a concise way of defining functions.
- Regular Function declaration
```jsx
function App(props){
  return <h1>{props.name}</h1>
}
export default App
```
- Arrow Function expression
```jsx
const App= (props) => {
  return <h1>{props.name}</h1>
};
export default App
```


## Q: What are the Main Files in a React project?
1. index.html: Single page for React application
2. components/component1.js: Your application components.
3. App.js: Main component or container or Root component.
4. App.test.js(Optional): Used for writing tests for App.js file.
5. index.css(Optional): This is a global CSS file that serves as the main stylesheet for the entire application.
6. index.js: Entry point for JavaScript. Renders the main React component(App) into the root DOM elements

## Q: How React App Load and display the components in the browser?
- 1st user hit the browser and request send to the "**index.html**"
- With the help of react librarys **index.js** file is loaded in the browser
- **index.js** file communicate/render the **App.js** internally.

## Q: WHat is the difference between React and Angular?
- Similaraties: React and Angular are used to create **single page UI** application using components

| **React**                                                              | **Angular**                                                                           |
|------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| 1. React is a JavaScript library                                       | Angular is a complete framework                                                       |
| 2. React uses a virtual DOM which makes it faster.                     | Angular uses a real DOM                                                               |
| 3. React is smaller in size and **lightweight** and therefore faster sometimes| Angular is bigger because it is a complete framework                           |
| 4. React depends on external libraries for many complex features, so developer has to write many lines of code for complex functionalities| Since Angular is a complete framework, therefore it provide **build-in support** for features like routing, form, validation, and HTTP requests. |
| 5. React is **simple to learn** and more popular than Angular.         | Angular is slightly difficult to learn as it has Typescript, OOPS concept and many more thing|

## Q: What are the 5 other JS frameworks other than React?
1. Anuglar
2. Vue.js
3. AngularJs
4. Backbone.js
5. Ember.js

## Q: Whether React is a Framework or a library? What is the difference?
**Library**: Developers import the libraries at the top and then used its functions in components.
- React is commonly referred to as a JavaScript library.

**Framework**: Developers need to follow a specific structure or pattern defined by the framework.
- Angular is a framework.

## Q: How React provides Reusability and Composition?
- React provides reusability and composition through its **component-based architecture**
- **Reusability**: Once you create a component, you can **re-use** it in different parts of your application or even in multiple project.
- **Composition**: Composition is creating new and big components by **combining existing small components**. Its advantage is, change to one small component will not impact other components

## Q: What are state, stateless, stateful and state management terms?
- **state**: refers to the current data of the component.
```jsx
let count = 0; //initial state
```
- **Stateful or State management**: measn when a user performs some actions on the UI, then the React application should be able to **update and re-render that data or state** on the UI.
```jsx
const [count, setCount] = useState(0);
const increment = () =>{
  setCount(prevCount => prevCount+1);
  console.log(`Count: ${count}`);
};

```
- **Stateless**: means when a user performs action doesnot effect the UI
```jsx
const increment = () =>{
  count += 1;//state updated
  console.log(`Count: ${count}`);
};
```

## Q: What are Props in JSX?
- props(properties) are a way to **pass data** from a parent to child component
```jsx
return(
<>
  <ChildComponent name="Happy" purpose="Interview" />
</>
)
```
```jsx
function ChildComponent(props){
  retrun(
    <div> {props.name}, {props.purpose}</div>
)
}
```






