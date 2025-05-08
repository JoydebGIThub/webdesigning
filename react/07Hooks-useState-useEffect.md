## Q: What are React Hooks? What are the Top React Hooks?
- React Hooks are **inbuilt functions** provided by React that allow functional components to use **state and lifecycle features**
- Before Hooks, class components lifecycle methods were used to maintain state in React applications.
- To use react hook first we have to import it from React library.
```jsx
import React, {useState} from "react";
```

### Top React Hooks:
1. useState -> state
2. useEffect -> Side effect
3. useContext -> context
4. useReducer -> Complex state
5. useCallback -> Memorization
6. useMemo -> Performance
7. useRef -> Refs
8. useLayoutEffect -> Synchronous side effects

## Q: WHat is the role of useState() hook and how it works?
```jsx
import React, {useState} from "react";

function UseState(){
  //array destructuring
  const [count, setCount] = useState(0);

  const increment = () =>{
    setCount(count + 1);
    console.log(`count: ${count + 1}`);
  }
}
```

- The useState hook enables functional components to **manage state**.
- useState() working: useState() function accept the initial state value as the parameter and returns an array with two elements:
  1. The first element is the current state value(count in this code)
  2. Second element is the function that is used to update the state(setCount in this code)
- The concept of assign array elements to individual variables is called **array destructuring**

## Q: What is the role of useEffect(). How it works and what is its use?
- The useEffect Hook in React is used to perform **side effect** in functional components.
- For example: data fetching from API, subscriptions or any other operation that needs to be performed after the component has been changed
```jsx
import React, {useEffect} from "react";

function UseEffect(){
  useEffect(()=>{
    const fetchData= asynce() =>{
      const response = await fetch("http://jsonplaceholder.typicode.com/posts/1");
      const result = await response.json();
      console.log("Title: ", result.title());
    };
    fetchData();
  },[])
}
```

- useEffect() is called **after the component renders.**. Example: side effect
- useEffect() function will accept two parameter. (Effect function, dependency array)

## Q: WHat is Dependency Array in useEffect() hook?
- Dependencies array(optional) act as triggers for useEffect to **rerun** meaning if any of dependencies values changes the code inside useEffect() will be executed again.

## Q: WHat is the meaning of the empty array[] in the useEffect()?
- An **empty array[]** indicates that the effect function should only **run once**











