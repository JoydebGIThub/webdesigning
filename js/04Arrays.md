## Q: What are Arrays in JS? How to get, add, remove elements from arrays?
Ans: An array is a data type that allows you to **store multiple values** in single variable. Structured the data in a batter way.
- Get
  1. indexOf() --> give a index of a **specified element** ```js const array = [1, 2, 4, 5, 6 ]; console.log(array.indexOf(4)); //2```
  2. find() --> find give the **1st element** which satisfies the condition. ```js const array = [1, 2, 4, 5, 6 ]; console.log(array.find(n => n%2===0)); //2```
  3. filter() --> filter the element based on the **conditions**```js const array = [1, 2, 4, 5, 6 ]; console.log(array.filter(n => n%2===0)); //[ 2, 4, 6 ]```
  4. Slice() --> get a **subset of the array** from **start index to end index(end not included)**
```js
const array = [1, 2, 4, 5, 6 ];
console.log(array.slice(1, 4)); //[ 2, 4, 5 ]
console.log(array); //[ 1, 2, 4, 5, 6 ]
```
- Add
  1. push() --> add the element at the **end of the array**. it will **modify the original array** itself. ```js const arr= [1, 2];
console.log(arr); // [ 1, 2 ]
arr.push(3, 5);
console.log(arr); // [ 1, 2, 3, 5 ]```
  2. concat() --> add arrays into **single array**. **Creating a new array** and not modify the original array ```js const arr= [1, 2];
console.log(arr);//[ 1, 2 ]
let arr2 = arr.concat(3, 5);
console.log(arr2);//[ 1, 2, 3, 5 ]
console.log(arr);//[ 1, 2 ]```
  3. unshift() --> add the element at the **1st of the array**
- Remove
  1. pop() --> remove the **last element of the array**
  2. shift() --> remove the **1st element of the array**
  3. splice() --> used to **add, remove or replace** element in an array
```js
// array.splice(startIndex, deleteCount, ...itemsToAdd)
let letter= ['a', 'b', 'c'];
//add
letter.splice(1, 0, 'x', 'y');
console.log(letter);//[ 'a', 'x', 'y', 'b', 'c' ]
//remove
letter.splice(2, 1);
console.log(letter); // [ 'a', 'x', 'b', 'c' ]
//modify
letter.splice(0, 1, 'q');
console.log(letter); //[ 'q', 'x', 'b', 'c' ]
```
- Modify
  1. map() -> modify **each element of the array**. Give a new array ```js let arr1= [1, 2, 3]
let mapArray = arr1.map(e => e*2);
//return a new array
console.log(mapArray);//[ 2, 4, 6 ]
console.log(arr1);//[ 1, 2, 3 ]```
  2. forEach() -> we perform some operation on each element **without createing an new array**. give the individual values. ```js let arr1= [1, 2, 3]
arr1.forEach(e=> console.log(e*2)) // 2 4 6
//Doesnot return anything
console.log(arr1);//[ 1, 2, 3 ]```
- other
  1. join()
  2. length
  3. sort()
  4. reverse()
  5. reduce()
  6. some()
  7. every()
******************************************************************************************
## sort() and reverse()
```js
let arr1= [4, 2, 3]
arr1.sort();
console.log(arr1);//[ 2, 3, 4 ]

let arr2= ['c', 'b', 'a'];
arr2.sort();
console.log(arr2);//[ 'a', 'b', 'c' ]

let arr1= [4, 2, 3]
arr1.reverse();
console.log(arr1);//[ 3, 2, 4 ]

let arr2= ['c', 'a', 'b'];
arr2.reverse();
console.log(arr2);//[ 'b', 'a', 'c' ]
```
*********************************************************************************************
## What is Array Destructuring in JS?
Ans: 
- Array destructuring allows you to extract elements from an array and assign them to **individual variables** in a single statement
- Array destructuring is introduced in **ECMAScript 6 (ES6)**
```js
const fruits = ['apple', 'banana', 'orange'];
//Destructuring
const [first, second, third] = fruits;
console.log(first) //apple
console.log(second) //banana
console.log(third) //orange
```
**********************************************************************************************
## WHat are array-like objects in JS?
Ans: Array-like objects are objects that have indexed elements and a length property, **similar to arrays** but they may not have all the methods of arrays like push(), pop(), other
### Example
- arguments
```js
sum(1, 2, 4);
function sum(){
    console.log(arguments);//[Arguments] { '0': 1, '1': 2, '2': 4 }
    console.log(arguments.length);//3
    console.log(arguments[0]);//1
}
```
- Strings
```js
let string = "Joydeb";
console.log(string.length); // 6
console.log(string[0]); // j
console.log(string.indexOf('y')); // 2
```
- HTML collections
```js
var boxes = document.getElementsByClassName('box');
console.log(boxes[0]);
console.log(boxes.length);
```
*******************************************************************************************
## How to convert an array-like object into an array?
- Array.form()
```js
var arrayLike = {0: 'a', 1: 'b', 2: 'c', length: 3};
console.log(arrayLike); //{ '0': 'a', '1': 'b', '2': 'c', length: 3 }
var array1= Array.from(arrayLike);
console.log(array1); // [ 'a', 'b', 'c' ]
```
- spread syntax
```js
var arrayLike = {0: 'a', 1: 'b', 2: 'c', length: 3};

// Create an iterable object because arrayLike is not iterable
arrayLike[Symbol.iterator] = function* () {
  for (let i = 0; i < this.length; i++) {
    yield this[i];
  }
};
// we need to do the above part because a plain JavaScript object is still not inherently iterable. The spread syntax relies on the presence of the Symbol.iterator method. 1 
//
var array1 = [...arrayLike];
console.log(array1); // [ 'a', 'b', 'c' ]
```
- Array.prototype.slice.call()
```js
var arrayLike = {0: 'a', 1: 'b', 2: 'c', length: 3};
var array3 = Array.prototype.slice.call(arrayLike);
console.log(array3); // [ 'a', 'b', 'c' ]
```
************************************************************************************




