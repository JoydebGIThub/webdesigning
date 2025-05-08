## Q: What is NPM? What is the role of node_modules folder?
- NPM (Node Package Manager) is used to manage the **dependencies** for your React project, including the **React library** itself.
- node_modules folder contains all the dependencies of the project, including the React libraries.

## Q: What is the role of public folder in React
- Public folder contains **static assets** that are served directly to the user's browser, such as images, fonts and the index.html file.

## Q: What is the role of src folder in React?
- src folder is used to **store all the source code** of the application which is then responsible for the **dynamic changes in your web application**

## Q: What is the role of index.html page in React?
- index.html file is the main HTML file(SPA) in React application.
- Here the div with "id=root" will be replaced by the component inside **index.js/main.jsx file**.

## Q: WHat is the role of index.js file and ReactDOM in React?
- ReactDOM is a JavaScript library that renders components to the DOM or browser
- The index.js file is the JavaScript file that replaces the root element of the index.html file with the newly rendered components.

## Q: What is the role of App.js file in React?
1. App.js file contain the **root component(App)** of React application.
2. App component is like a **container** for other components.
3. App.js defines the structure, layout and routing in the application.

## Q: What is the role of function and return inside App.js
- The function keyword is used to **define a JavaScript function** that represents your React component.
- function is like a placeholder which contains all the code or logic of component.
- The function takes in props as its argument (if needed) and returns JSX

- **retrun** is used to return the element from the function

## Q: can we have function without a return inside App.js?
- Yes, a function without a return statement is possible
```jsx
const FunctionWithoutReturn = () =>{
  console.log("No Return");
};
export default FunctionWithoutReturn;
```
- In that case, the component will not render anything in UI.
- The common use case is for **logging** purpose

## Q: WHat is the role of export default inside App.js?
- Export statement is used to make a component available for **import** using import statement in other files.

## Q: Does the file name and the component name must be same in React?
- **No**, the file name and the component name don't have to be the same.
- However, it is recommended to keep them same for easier to organize and understand the code.












