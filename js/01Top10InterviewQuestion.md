## Q: What are Arrow Function in JS? What is it use?
Ans: Arrow functions, also known as "**fat arrow function**", is a **simpler and shorter** way for defining functions in JS.
```js

//Traditional approach
function add(a, b){
  retrun a+b;
}
console.log(add(5, 6));

//arrow function
const add2 = (a, b) => a+b;
console.log(add2(5, 6));
```
****************************************
## What is Scope in JavaScript?
Ans: Scope determines where variables are defined and where they can be accessed.
```js
//Global- accessbile anywhere
let globalVariable = "global";
greet();
function greet(){
  //Function - accessible inside function only
  let functionVariable = "function";
  if(tree){
    //Block - accessbile inside block only
    let blockVariable= "block";
    console.log(blockVariable);
    console.log(functionVariable);
    console.log(globalVariable);
  }
  console.log(functionVariable);
  console.log(globalVariable);
}
console.log(globalVariable);
```
******************************************************
## Q: What is Hoisting in JS?
Ans: Hoisting is a JS behavior where functions and variable declarations are moved to the "**top**" of their respective scopes during the **compilation** phase. let doesn't support hoisting.
```js
//Function hoisting
myFunction();

function myFunction() {
    console.log("Hello");
}// Output: Hello

//Variable Hoisting
x=10;
console.log(x); // output 10
var x;
```
```js
myFunction(); // it will now give error: Cannot access 'myFunction' before initialization

const myFunction=()=> {
    console.log("Hello");
}

x=10; // it will now give error: Cannot access 'x' before initialization
console.log(x);
let x;
```







