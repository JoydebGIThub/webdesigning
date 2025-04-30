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

Null
------------------------------------------------------------------------
#### There is just a stand on the wall
```js
let value3 = null;
```
**Means there is a valid variable with a value of no data type**

Undefined
------------------------------------------------------------------------
#### There is nothing on the wall
```js
let value4;
```
**Means there is a incomplete variable and not assigned anything**

Difference
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
## What is type coercion in JS?
Ans: Type coersion is the **automatic conversion of values** from one data type to another **during certain operations or comparisons**.
```js
let string = "42";
let number = 42;
let boolean = true;
let nullValue = null;

console.log(string + number); // Output: 4242
console.log(number+boolean); // 42
console.log(string == number); // true
console.log(boolean == 1); // true
console.log(boolean + nullValue); //1
```
### Uses:
1. Type coercion can be used during **String and Number concatination**.
2. Type coercion can be used while using **comparison operators**
*******************************************************************************************
## When to use which type of conditions statements in real application?
- If-else: for complex, different & **multiline execution**
  - Benefit: Cover all scenarios.
- Ternary Operators: for single conditions & "**single value evaluations**"
  - Benefit: Short one line syntax
- Switch case: For same left-side values
  - Benefit: More structured code
******************************************************************************************
## What is the difference between == and ===?
Ans: 
- Loose Equality (**==**): Operator compares two values for equality after **performing type coercion**.
```js
console.log(1 == '1'); // true
console.log(true == 1); // true
```
- Strict Equality (**===**): Operator compares two value for equality **without performing the type coercion**.
```js
console.log(1 === '1'); //false
console.log(true === 1); //false
```
****************************************************************************************
## What is the difference between find() and filter() methods of an Array?
Ans: 
- **find()** method get the **first element** that satisfies a condition.
```js
const arr = [1, 2, 3, 4, 5, 6, 7, 8];
let c = arr.find((num) => num % 2 === 0);
console.log(c); // 2
```
- **filter()** method **get an array of element** means all the elements which saticfies the condition .
```js
const arr = [1, 2, 3, 4, 5, 6, 7, 8];
let c = arr.filter((num) => num % 2 === 0);
console.log(c); // [2, 4, 6, 8]
```
******************************************************************************************
## What is string immutability?
Ans: String in Javascript are considered **immutable** because you **cannot modify** the contents of an existing string directyly.
******************************************************************************************
## What is DOM? What is the difference between HTML and DOM?
Ans: The DOM (Document Object Model) represents the web page as a **tree-like sturcture** that allows Javascript to dynamically access and manipulate the content and structure of a web page
HTML is a markup language for **reading** and **writing** for developer and user. But in reality **memory plays with DOM**
******************************************************************************************
## What is Erro Handling in JS?
Ans: Error handling is the process of **managing errors**.
*****************************************************************************************
## What is asynchronous programming in JS? What is its use?
Ans: 
- Asynchronous programming allows multiple tasks or operations to be **initiated and executed concurrently**
- Asynchronous operations **do not block** the execution of the code.
### Use:
1. Fetching Data from API
2. Downloading Files
3. Uploading Files
4. Animations and Transitions
5. Time taking operations
**JS is single Threaded, but managing the taks we can make it concurrent and parallal**

