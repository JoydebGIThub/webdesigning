## Q: What is JavaScript? What is the role of JS engine?
Ans: JavaScript is a programming language that is used for converting **static web page(html)** to **interactive and dynamic** web pages.
- JS engine: A JS engine is a program present in **web browsers** that executes JavaScript code.
******************************************************************************************************
## Q: What is Client side and Server side?
Ans: 
- A client (mobile, laption desktop)is a device, application (css, html, js), or software (chrome) component that **requests** and consumes service or resources **from a server** (java, c#, php).
- A server is a device, computer, or software application that **provides** services, resources or functions **to clients**.
******************************************************************************************************
## Q: What is the type of the variable in JS when it is declared without using the var, let, const keywords?
Ans: **var** is the **implicit** type of variable when a variable is declared without var, let or const keywords.
```js
if(true){
  variable = 10;
}
console.log(variable);//10
```
********************************************************************************************************
## Q: What is JSON?
- JSON (JavaScript Object Notation) is a lightweight **data interchange format**.
- JSON consists of **key-value** pairs.
```json
{
  "name": "Joydeb",
  "age": 14,
  "isStudent": false,
  "address": {
    "street": "123 Main ST",
    "city": "Kolkata",
    "country": "India"
  }
}
```
************************************************************************
## What is the use of typeof operator?
- typeof operator is used to determine the **type of each variable**.
- Real application use -> typeof operator can be used to **validate the data** received from external sources (api).
```js
let string = "42";
let number = 42;
console.log(typeof string);//string
console.log(typeof number); //number
```
*************************************************************************














