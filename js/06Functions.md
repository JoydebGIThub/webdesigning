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






