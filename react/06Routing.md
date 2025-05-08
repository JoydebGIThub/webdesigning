## Q: What is Routing and Router in React?
- **Routing**: Routing allows you to create a single-page web application with **navigation** without the need for a full-page refresh.
- **Router**: React Router is a library for handling routing and enables navigation and rendering of different **components based on the URL**.

## Q: How to implement Routing in React?
### install router:
```cmd
npm install react-router-dom
```

```jsx
import React from "react";
import {Routes, Route, Link} from "react-router-dom";

//Elements or imported componets
const Home = () => <h2>Home</h2>;
const About = () => <h2>About</h2>;
const Contact = () => <h2>Contact</h2>;

Const AppRoute = () =>(
  <div>
    <nav>
      <ul>
        <li><Link to="/">Home</Link></li>
        <li><Link to="/about">About</Link></li>
        <li><Link to="/contact">Contact</Link></li>
      </ul>
    </nav>

    <Routes>
      <Route path="/" element={<Home/>}/>
      <Route path="/about" element={<About/>}/>
      <Route path="/contact" element={<Conact/>}/>
    </Routes>
  </div>
);
export default AppRoute;

const root = ReactDOM.createRoot(
  document.getElementById('root')
);
root.render(
  <Router>
    <AppRoute/>
  </Router>
);
```

## Q: What are the roles of <Routes> and <Route> component in React Routing?
- The <Routes> component is used as the root container for declaring your **collection of routes**
- The <Route> component is used to define a route and specify the component that should render when the **route matches**.
  - For example: in this code if user enter "websitename.com/about" in uri, then matching "About" component will be rendered.
 
## Q: What are Route parameters in React Routing?
- Route parameters in React Router are a way to pass dynamic values(data) to the component **as part of the URL path**
```jsx
{/* userId is the route parameter*/}
<Route path="/user/:userId" component={UserProfile}/>
```

## Q: What is the role of switch component in react routing?
- Switch component ensures that only the **first matching <Route> is rendered** and rest are ignored.
  - Switch is commonly use to handle 404 or "not found" routes

```jsx
import {Switch, Route} from 'react-router-dom';

<Switch>
  <Route path="/users" element={<UserList/>}/>
  <Route path="/users/:userId" element={<UserProfile />}/>
</Switch>
```

## Q: WHat is the role of exact prop in React Routing
- exact prop is used with the <Route> component to **match exactly** to the provided path.
```jsx
{/*Without exact (default behavior)*/}
{/*match "about", "/about/team", "/about/contact"*/}
<Route path="/about" component={About}/>

{/*With exact*/}
{/* only match "about" */}
<Route path="/about" exact component={About}/>
```


















