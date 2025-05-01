## Q: What are Functions in JS? What are the types of function?
Ans: A function is a **reusable block of code** that performs a specific task.
```js
function add(a, b){
    return a+b;
}
result= add(3, 5);
console.log(result)//8
```
```js
function display(){
    a = 9;
    console.log(a); // 9
}
let a;
display();
//let a;// Cannot access 'a' before initialization
```
### Types of Functions:
1. Named Function
2. Anonymous Function
3. Function Expression
4. Arrow Function
5. IIFE
6. Callback Function
7. Higher-order function
*****************************************************************************************
## Q: WHat is the difference between named and anonymous functions? WHen to use what in the application?
- Named function: have a **name identifier**
- Use named function for **big and complex** logics,
- Use when you want to **reuse** one function at multiple places
```js
//Named function
//Function declaration
function add(a , b){
    return a+b;
}

console.log(add(6, 7)); // 13
```
- Anonymous function: Anonymous function **do not have a name identifier** and cannot be referenced directly by name.
- Use anonymous function for **small logic**
- Use when want to use a function in a **single place**
```js
console.log(function(a, b){
    return a*b;
}(4, 5)); // 20

console.log(function(a, b){
    return a*b;
}); // [Function (anonymous)]
```
**************************************************************
## Q: What in function expression in JS?
Ans: A function expression is way to define a function by **assigning it to a variable**
### Anonymous function expression
```js
//Anonymous function expression
const add = function(a , b){
    return a+b;
}
console.log(add(5, 6));//11
```
### Named function expression
```js
//Named function expression
const add = function sum(a , b){
    return a+b;
}
console.log(add(5, 6));//11
```
****************************************************************
## Q: What are Arrow Functions in js? what is it use?
Ans: Arrow functions, also known as **fat arrow** function, is a **simpler and sorter** way for defining functions in JS.
```js
//Arrow function 
const add = (a, b) => a+b;
console.log(add(5, 6));//11
const add2 = (a, b) => {
    return a + b;
}
console.log(add2(5, 6)); // 11
const add3 =  (a , b) => {(a+b)};
console.log(add3(5, 6)); // undefined
console.log((a , b) => a + b (5, 7));//[Function (anonymous)]
```
*********************************************************************************
## Q: WHat is Callback function? WHat is it use?
Ans: A callback function is a function that is **passed as an argument to another function**.
```js
function add(a , b){
    return a+b;
}

function display(x, y, operation){ // this display is called Higher-order function, operation is a callback function
    let result = operation(x, y);
    console.log(result);
}

display(4, 5, add);
```
***************************************************************************************
## Q: What is Higher-order function in JS?
Ans: A higher-order function:
- Take one or more functions as **arguments**(callback function)
```js
//Take one or more functions as arugument
function hof(func){
    func();
}
hof(sayHello); // Hello

function sayHello(){
    console.log("Hello");
}
```
- **Return** a function as a result.
```js
//Retrun a function as a result
function createAdder(number){
    return function(value){
        return value + number; //  2 + 5
    };
}
const addFive = createAdder(5);
console.log(addFive(2)); // 7
console.log(createAdder(5)(3)); // 8
```
**************************************************************
## Q: WHat is the difference between arguments and parameters?
- Parameters are the **placeholders** defined in the function declaration.
```js
// a and b are parameters
function add(a, b){
    console.log(a+b);
}
```
- Arguments are the **actual values passed** to a function when it is invoked or called.
```js
add(6, 7);
// 6 and 7 are arguments
```
******************************************************
## How many ways you can pass arguments to a function?
- Positional arguments
```js
function add(a, b){
    console.log(a+b);
}
add(6, 7);
```
- Named Arguments
```js
const person = {
    name: "Happy",
    role: "Developer"
};
function greet(person){
    console.log(person.name + " "+ person.role);
}

greet(person);// Happy Developer
```
- Arguments Object
```js
sum(1, 2, 4);
function sum(){
    console.log(arguments[0]); // 1
    console.log(arguments); // [Arguments] { '0': 1, '1': 2, '2': 4 }
    console.log(arguments.length); // 3
}
```
*************************************************************************************************
## How do you use default parameters in a function?
Ans: In js, default parameters allow you to specify **default values** for function paramenters.
```js
function greet(name ="Joydeb"){
    console.log("Hello "+ name)
}
greet();//Hello Joydeb
greet("Joy");//Hello Joy
```
********************************************************************************************
## What is the use of event handling in JS?
Ans: Event handling is the process of **responding to user actions** in a web
```js
<button id="myButton">Click me</button>;

const button = document.getElementById('myButton');
button.addEventListener('click', function(){
    alert('Button clicked');
});
```
**The addEventListener method of JS allows an event name and the function you want to perform on the event**
### Lists of event listener:
1. click Event: ```js addEventListener('click', handler)```
2. Mouseover Event: ```js addEventListener('mouseover', handler)```
3. keydown Event: ```js addEventListener('keydown', handler)```
4. keyup Event: ```js addEventListener('keyup', handler)```
5. Submit Event: ```js addEventListener('submit', handler)```
6. Focus Event: ```js addEventListener('focus', handler)```
7. Blur Event: ```js addEventListener('blur', handler)```
8. change Event: ```js addEventListener('change', handler)```
9. Load Event: ```js addEventListener('load', handler)```
10. Resize Event: ```js addEventListener('resize', handler)```
****************************************************************************************************
## Q: What are First-Class function in JS?
Ans: A programming language is said to have **First-class** functions if functions in that language are treated like **Other variables**
### Functions treated like variables:
1. Assignable:
```js
//Assigning function like a variable
const myFunction = function(){
    console.log("Interview! Happy");
}
myFunction(); // Interview! Happy
```
2. Passable as Argument
```js
function double(number){
    return number * 2;
}
//call back function pass as argument like variable
function performance(double, value){
    return double(value);
}
console.log(performance(double, 5)); //10
```
3. Retrunable as values:
```js
// A function retrun another function
function createSimpleFunction(){
    retrun function(){
        console.log("retrun from a function")
    }
}
const simpleFunction = createSimpleFunction();
simpleFunction(); // retrun from a function

```
*************************************************************************************
## Q: What is pure and impure functions in JS?
- Pure: A pure function that always produce the **same output for the same input**
- pure functions cannot modify the **state**
- Pure functions cannot have **side effect**
```js
//pure function

function add(a, b){
    return a+b;
}
console.log(add(5, 3)); //8
console.log(add(5, 3)); //8
console.log(add(5, 3)); //8
```
- Impure: An impure dunction can produce **different outputs for the same input**
- Impure functions can modify the state.
- Impure fucntions can have side effect
```js
//impur function
let total =0;
function addToTotal(value){
    total +=value;
    return total;
}
console.log(addToTotal(5));//5
console.log(addToTotal(5));//10
console.log(addToTotal(5));//15
```
*****************************************************************************
## Q: What is function currying in JS?
Ans: Currying in Javascript transforms a function with multiple arguments into a "**nested series of functions**", each taking a single argument.
```js
//Regular function
function add(a,b){
    return a+b;
}

// Curried version of multiply function
function curriedMultiply(a){
    return function(b){
        return a+b;
    };
}
```
- Advantage: **Reusability, modularity, and specialization**. Big, complex function with multiple arguments can be ***brocken down* into small, reusable functions with fewer arguments.
*************************************************************************************************************
## Q: What are call, apply and bind methods in JS?
- call, apply, and bind are three methods in JavaScript that are used to work with functions and **control how they are invoked** and what context they operate in.
- These methods provide a way to manipulate the **this value** and pass arguments to functions.
```js
//Defining a function that uses the "this" context and an argument
function sayHello(message){
    console.log(`${message}, ${this.name}! `);
}
const person = {name: "Happy"};
```
1. call - using the **call** method to invoke the function with a specific context and argument
```js
sayHello.call(person, 'Hello'); // Hello Happy!
```
2. apply - using the **apply** method to invoke the function with a specific context and an array of arguments
```js
sayHello.apply(person, ['Hi']); // Hi Happy!
```
3. bind - using the **bind** method to create a new function with specific context (not invoking it immediately)
```js
const greetPerson = sayHello.bind(person);
greetPerson('Greetings'); // Greetings, Happy!

```
