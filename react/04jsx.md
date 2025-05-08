## Q: What is the role of JSX in React?
1. JSX stands for **JavaScript XML**.
2. JSX is used by React to write **HTML-like code**.
3. JSX is converted to JavaScript via tools like **Babel**, because Browsers understand JavaScript not JSX.

## Q: What are the advantages of JSX?
1. Improve code readability and writability.
2. Error checking in advance(Type safety)
```jsx
return(
  <div>
    <h1> Hello </h> // this h will show us error immediately, this is called type safety
  </div>
)
```
```js
return React.createElement(
  'div',
  {className: 'App'},
  React.createElement('hddd', null, 'Hello') // this hddd will not show any error
)
```

3. Supporting JavaScript expressions
```jsx
return(
  <div>
    {/*JavaScript expression*/}
    <h1>Hello, {name}!</h1>
    <p>{2+2} sum</p>
  </div>
)
```

4. improved performance
5. Code reusability.

## Q: WHat is Babel?
- Babel in React is used to transpile JSX syntax into regular JavaScript which browser can understand.

## Q: What is the role of Fragment in JSX?
- In React, a fragment is a way to **group multiple children's** element
- Using a Fragment prevents the addition of unnecessary nodes to the DOM
**Seperate element(Error)**
```jsx
return(
  <div></div>
  <div></div>
)
```

**correct way**
```jsx
return(
  <div>
    <div></div>
    <div></div>
  </div>
)
```

**Better way**
```jsx
return(
  <Fragment>
    <div></div>
    <div></div>
  </Fragment>
)
```

**Best way**
```jsx
return(
  <>
    <div></div>
    <div></div>
  </>
)
```

## What is Spread Operator in JSX?
- The spread operator(...) is used to expand or spread an array or object.
```jsx
function App(){
  const props = {name: 'Happy', purpose:'Interview'};

  return(
    <>
      <ChildComponent {...props}/>
    </>
  )
}

function ChildComponent(props){

  return(
    <>
      <div>{props.name}, {props.purpose}</div>
    </>
  )
}
```

## Q: What are the types of Conditional Randering in JSX?
1. if/else statements
```jsx
function MyComponent(){
  if(2>1){
    return "abc";
  }
  else{
    return "xyz";
  }
}
```

2. Ternary operator
```jsx
function MyComponent(){
  return 2>1 ? "abc" : "xyz";
}
```

3. && operator (similar to ternary)
```jsx
function MyComponent(){
  {return 2>1 && "abc"};
}
```

4. Switch statement
```jsx
function MyComponent(){
  const value=2;
  switch(value){
    case 2:
      return 'abc';
    case 1:
      return 'xyz';
    default:
      return null;
  }
}
```

## Q: How do we iterate over a list in JSX? What is map() method?
```jsx
function App(){
  const numbers = [1, 2, 3, 4, 5];

  return(
    <>
      {
        numbers.map((number) => (number * 2))
      }
    </>
  )
}
```
- **map()** method allows you to **iterate** over an array and modify its elements using a callback function

## Q: Can a browser read a JSX file?
- No, browsers cannot directly interpret or understand JSX files
- Buble takes JSX and converts it into equivalent JavaScript code that browsers can understand.

## Q: What is Transplier? What is the difference between Compiler and Transpiler?
- A **Transpiler** is a tool that converts source code from one **high-level programming language(JSX)** to another **heigh-level programming language(JavaScript)**.(Babel)
- A **Compiler** is a tool that converts **high-level programming language(Java)** into a **lower-level language(machine code or bytecode)**.

## Q: Is it possible to use JSX without React?
- Yes, it's possible to use JSX without React by creating your own transpiler like Babel



