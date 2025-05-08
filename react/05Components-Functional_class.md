## Q: WHat are React Components? WHat are the main elements of it?
- In React, a component is a **reusable building block** for creating user interfaces.

## Q: What are the Types of React components? What are Functional Components?
- There are 2 types of components:
  - Functional Components.
  - Class Components.
- Functinal components are declared as a **JavaScript function**.
- They are **stateless component**, but with the help of hooks, they can now manage state also.

## Q: How do we pass data between functional components in React?
- **props(properties)** are a way to pass data from a parent component to a child component.

## Q: What is Prop Drilling in React?
- **Prop drilling** is the process of **passing down props** through **multiple layers of components**.

## Q: Why to Avoid Prop Drilling? In how many ways can avoid Prop Drilling?
### Why to avoid prop drilling?
1. **Maintenance**: Prop drilling can make code harder to maintain as changes in data flow require updates across multiple components.
2. **Complexity**: It increases code complexity and reduces code readablity.
3. **debugging**: Debugging becomes challenging when props need to be traced through numerous components.

### 5 ways to avoid prop drilling:
1. Using Context API
2. Using Redux
3. Using Component Composition
4. Using Callback Functions
5. Using Custom Hooks

## Q: What are Class Components in React?
```jsx
import React, {Component} from 'react';

class AppClass extends Component{
  render(){
    return <h1>Interview Happy</h1>;
  }
}

export default AppClass;
```
- class components are defined using **JavaScript class**
- They are **stateful components** by using the lifecycle methods
- The **render method** in class component is responsible for returning JSX.

## Q: How to pass data between class components in React?
- **this.props** can be used in child component to access properties/ data passed from parent component.
```jsx
class ParentComponent extends Component{
  render(){
    const dataToSend = "Hello from Parent!";
    return(
      <div>
        <ChildComponent message = {dataToSend}/>
      </div>
    )
  }
}

class ChildComponent extends Component{
  render(){
    return(
      <div>
        <p>Message: {this.props.message}</p>
      </div>
    )
  }
}
```

## Q: What is the role of this keyword in class components?
- this keyword is used to refer to the **instance of the class**.

## Q: What are the 5 differences btw Functional and Class components?
| **Functional Component**     |  **Class Component**       |
|------------------------------|----------------------------|
|1. Defined as a JS function   | Defined as a JS(ES6) class |
|2. Originally stateless but can now maintain state using hooks| Can manage local state with this.state |
|3. It doesnot have lifecycle method| It has lifecycle method|
|4. more readable & concise| Verbose(complex)|
|5. It doesn't have this keyword| It has this keyword|
|6. It doesn't have render method| It has the render method|







