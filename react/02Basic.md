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
