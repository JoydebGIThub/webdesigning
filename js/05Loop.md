## Q: What is the difference between for and for...of loop in JS?
- for loop is slightly more complex having more line of code where as **for ...of** is much simpler and better for iterating arrays
```js
let array = [1, 2, 4];
for(let i=0; i<array.length; i++){
    console.log(array[i]); // 1 2 4
}

for (let i of array){
    console.log(i); // 1 2 4
}
```
********************************************************************
## Q: What is the difference between for...in and for...of loop in JS?
- for...of
  1. for...of loop is used to loop the **values of an object like arrays, strings**
  2. It allows you to access each value **directly** without having to use an index.
```js
let array = [1, 2, 4];
for (let i of array){
    console.log(i); // 1 2 4
}
```
- for...in
  1. for...in loop is used to loop through the **properties of an object**
  2. It allows you to iterate **over the keys of an object** and access the values associated by using **keys as the index**.
```js
const person = {
    name: "joydeb",
    age: 27
}
for(let key in person){
    console.log(person[key]); // Joydeb 27
}
```
*************************************************************************************
## Q: What is forEach method?
Ans: forEach() is a method available on arrays or object that allows you to **iterate over each element** of the array and perform some action on each element
```js
let array = [1, 2, 4];
array.forEach(function(item){
    console.log(item); // 1 2 4
})
const person = {
    name: "joydeb",
    age: 27
}
Object.values(person).forEach(value => {
    console.log(value); // joydeb 27
})
Object.keys(person).forEach(key => {
    console.log(key);// name age
})
```
******************************************************************
## Q: When to use for...of loop and when to use forEach method in application?
- for...of loop is suitable when we need **more control over the loop**, such as using **break or continue** statement inside.
```js
for(let i of array){
  console.log(i);
  if(i === 2){
    break;
  }
}//output: 1 2
```
- forEach method **iterate over each element** of the array and perform some action of each element.
```js
array.forEach(function(item){
  console.log(item);
  if(item === 2){
    break;
  }
}) // error: Illegal break statement
```
*************************************************************************





