## Q: What is React? What is Role of React in software development?
- React is an open source Javascript library
- React is used for building **User Interface(UI)**
- React simplifies the creation of **SPA (Single Page Application)** by using resuable components.
******************************************************************************
## Q: What are the key features of React?
1. Virtual DOM: React utilizes a virtual representation of the DOM, allowing efficient updates by **minimizing direct manipulation of the actual DOM**, resulting in improved performance
2. Component Based Architecture: React structurs used interfaces as modular, reusable components, promoting a more maintainable and scalable approach to building appliaction
3. Reusability & Composition: React enables the creation of resuable components that can be composed together, fostering a modular and efficient development process.
4. JSX (JavaScript XML): JSX is syntax extension for JavaScript used in React, allowing developers to write **HTML-like code** within JS, enhancing readability and maintainability
5. Declarative Syntax: React have a declarative programming style(JSX), where developers **focus on "what" the UI should look like** and React handles the **"how"** behind the scenes. 
6. Community Ecosystem: React benefits from a vibrant and **extensive community**, contributing to a rich ecosystem of libraries, tools and resources, fostering collaborative development and innovation
7. React Hooks: Hooks are functions that enable functional components to **manage state and lifecycle features, providing** a more concise and expressive way to handle component logic
*********************************************************************************
## Q: WHat is DOM? What is the difference between HTML and DOM?
Ans: DOM(Document Object Model) represents the web page as a **tree-like structure** which allows JavaScript to **dynamically access and manipulate* the content and structure of a web page. **Memory** palys with DOM.
******************************************************************************
## Q: WHat is Virtual DOM? Difference between DOM and Virtual DOM?
- React uses a **virtual DOM** to efficiently update the **UI(User Interface)** **without re-render the entire page**, which helps impove performance and make the application more responsive
| **DOM**                                                                 | **Virtual DOM**                                                                      |
|------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| 1. DOM is actual representation of the webpage.                        | Virtual DOM is lightweight copy of the DOM.                                           |
| 2. Re-renders the entire page when updates occur.                      | Re-renders only the changed parts efficiently.                                        |
| 3. Can be slower, especially with frequent updates.                    | Optimized for faster rendering.                                                       |
| 4. Suitable for static websites and simple applications                | Ideal for dynamic and complex single-page applications with frequent updates         |
*****************************************************************************
## Q: What are React Components? WHat are the main elements of it?
Ans: In react, a component is a **reusable building block** for creating user interfaces.
```jsx
//1. Import the React library
import React from "react";

//2. Define a functional Component
function Component(){
  //3. Return JSX to describe the component's UI
  retrun(
    <div>
      <h1>I am a React Reusable Component</h1>
    </div>
  );
}
//4. Export the component to make it available for uses
export default Component;
```
**********************************************************************************
## Q: What is Single Page application(SPA)?
- A single page applications is a web application that have only one **single web page**
- Whenever user do some action on the website then in response content is **dynamically updated** without refreshing or loading a new page
*********************************************************************************
## Q: WHat are 5 Advantages of React?
- Simple to build SPA(by using Components)
- React is cross platform and open source (Free to use)
- Lightweight and very fast (Virtual DOM)
- Large Community and Ecosystem
- Testing is easy
**********************************************************************************
## Q: What is the Disadvantages of React?
Ans: React is not good choice for very small applications.
*******************************************************************************
## Q: What is the role of JSX in React?
1. JSX stands for **JavaScript XML**
2. JSX is used by React ti write **HTML-like code**
3. JSX is converted to JS via tools like **Bable**, beacuse Browsers understand JavaScript not JSX.
*******************************************************************************
## Q: What is the difference between Declarative and Imperative syntax.
- Declarative syntax focuses on **describing the desired result** without specifying the **step-by-step** process
- **JSX** in react is used to write declarative syntax
```jsx
//Declarative syntax using JSX
function App(){
  retrun <h1>Hello</h1>
}
```
- Imperative syntax involves **step by step process** to achieve a particular goal
- **JS** has an imperative syntax
```js
//Imperative systax(non-react) using JS
function App(){
  const element = document.createElement('h1');
  element.textContent = "Hello";
  document.body.appendChild(element);
}
```
********************************************************************************************






