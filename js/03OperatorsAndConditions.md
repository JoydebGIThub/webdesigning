## Q: What is operator precedence?
Ans: As per operator precedence, operators with higher precedence are **evaluated first**.
```
B-> Brackets
O-> Order
D-> Division
M-> Multiplication
A-> Addition
S-> Subtraction
```
*****************************************************************************
## Q: What is the difference between unary, binary, ternary operators?
Ans:
- Unary:
```js
let a=5
//Single operand
let b = -a;
console.log(b); // -5

console.log(++a); //6
```
- Binary:
```js
let x=10;
let y=3;

//Two operand
let z= x + y;
console.log(z); //13
```
- Ternary:
```js
//Three operands
let results = condition ? 'Yes' : 'No';
console.log(results); // Yes
```
********************************************************************************
## Q: What is short-circuit evaluation in JS?
Ans: short-circuit evaluation stops the execution as soon as the **result can be determined without evaluating** the remaining **sub-expression**
```js
//AND
let result = false && someFunction();
console.log(result); //false

//OR
let result2= true || someFunction();
console.log(result2);//true
```
***************************************************************************
## Q: What are the type of conditions statements in JS?
1. if/else statements
2. Ternary operator
3. switch statement
***************************************************************************
## Q: What is the difference between spread and Rest operator in JS?
- The spread operator(...) is used to **expand or spread elements** from an iterable(such as an **array, string, or object**) into **individual elements**
```js
//Spread operator
const arr= [1, 2, 4];
console.log(...array); //Output 1 2 4
```
### Use of spread operator:
1. Copying array
```js
const originalArray = [1, 2, 4];
const copyArray = [...originalArray];
console.log(copyArray); // output: [ 1, 2, 4 ]
```
2. Merging Array
```js
const array1=[1, 2, 3];
const array2=[4, 5];
const marge = [...array1, ...array2];
console.log(marge);// [ 1, 2, 3, 4, 5 ]
````  
3. Passing multiple arguments to a function
```js
const numbers = [1, 2, 4, 5, 5];
sum(...numbers);
function sum(a, b, c, d, e){
  console.log(a+b+c+d+e);// 17
}
```
- The rest operator is used in function parameters to collect all **remaining arguments** into an array
```js
display(1, 2, 4, 5, 6);
function display(first, second, ...rest){
  console.log(first); //1
  console.log(second); //2
  console.log(rest); // [ 4, 5, 6 ]
}
```
**************************************************************


















