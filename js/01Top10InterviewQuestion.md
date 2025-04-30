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
*******************************************************************************
## Q: What are variables? What is the difference between var, let, and const?
Ans: Variables are used to **store** data.
#### Example:
```js
var count = 10;
```
### The Scope of var, let, count:
- var -> function
- let -> block
- const -> block
#### using var
```js
function(){
  if(true){
    var count = 10;
    console.log(count); // output: 10
  }
  console.log(count); // output: 10
}
```
**var creates a function-scoped variable**
#### using let
```js
function(){
  if(true){
    let count = 10;
    console.log(count); // output: 10
  }
  console.log(count); // Output: uncaught , Error: undefined
}
```
**let creates a block-scoped variable**
#### using const
```js
const z=10;
z=20;
//This will result
//in an error
console.log(z);
```
**const can be assigned only once, and its value cannot be changed afterwards.**
*****************************************************************************
## Q: What is the difference between primitive and non-primitive data types?
Ans: **Primitive** and **Non-Primitive** are the categories of data types.
- The actual data types from Primitive:
1. Numbers
2. Strings
3. Booleans
4. Undifined
5. null
- The actual data types from Non-primitive:
1. Object
2. Array
3. Function
4. Date
5. RegExp
### Fundamental difference:
- Primitive data types can hold only **single** value.
- Primitive data types are **immutable**, meaning their value, once assigned, cannot be changed.
```js
//Number
let age = 25; // a new
age = 30; // a new variable is created for the js
// means the memory address of 25 and 30 is diffrent
```
- Non-primitive data can hold **multiple** value.
- They are **mutable** and their values can be changed.
```js
//Array
let oddNumber = [1, 3, 5]
//object
let persion = {
  name: "Joydeb",
  age: 27
}
```
*************************************************************
## What is the difference between null and undefined in JS?
#### A stand on the wall with also a paper holder
```js
let value1 = 0;
```
**Means there is a valid variable with also a value of data type number**
#### A stand on the wall with also a paper holder
```js
let value1 = '';
```
**Means there is a valid variable with also a value of data type string**
.
------------------------------------------------------------------------
#### There is just a stand on the wall
```js
let value3 = null;
```
**Means there is a valid variable with a value of no data type**
.
------------------------------------------------------------------------
#### There is nothing on the wall
```js
let value4;
```
**Means there is a incomplete variable and not assigned anything**
.
------------------------------------------------------------------------
- **Undifined**: When a varibale is declared but has '**not been assigned a value**', it is automatically initialized with **undefined**.
- Undifined can be used when you don't have the value **right now**, but you will get it after some logic or operation.
```js
let undefinedVariable; // no value assigned
console.log(undefinedVariable); // Output: undefined
```
- **null**: null variable are intentionally assigned the "**null value**".
- Null can be used, when you are **sure you do not have any value** for the particular variable.
```js
let nullVariable = null; // null assigned
console.log(nullVariable); //Output: null
```
*******************************************************************************************





