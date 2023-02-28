# JS_BASIC_SESSION_1

## Introduction
JavaScript is a lightweight, cross-platform, and interpreted compiled programming language which is also known as the scripting language for webpages.
JS is a dynamically typed and a single-threaded language, which means it has only one call stack that is used to execute the program.

## Why we use JS 
We use javascript so that we can make our page interactive , For example ---> You can take any website like amazon , google or anything , content is changing dynamically
It's happening because of javascript

## Applications of JavaScript

Web Development: Adding interactivity and behavior to static sites JavaScript was invented to do this in 1995. By using AngularJS that can be achieved so easily.
    Web Applications: With technology, browsers have improved to the extent that a language was required to create robust web applications. When we explore a map in       Google Maps then we only need to click and drag the mouse. All detailed view is just a click away, and this is possible only because of JavaScript. It uses         Application Programming Interfaces(APIs) that provide extra power to the code. The Electron and React is helpful in this department.
    
Server Applications: With the help of Node.js, JavaScript made its way from client to server and node.js is the most powerful on the server-side.
    
Games: Not only in websites, but JavaScript also helps in creating games for leisure. The combination of JavaScript and HTML 5 makes JavaScript popular in game development as well. It provides the EaseJS library which provides solutions for working with rich graphics.
    
Smartwatches: JavaScript is being used in all possible devices and applications. It provides a library PebbleJS which is used in smartwatch applications. This framework works for applications that require the internet for its functioning.
    
Art: Artists and designers can create whatever they want using JavaScript to draw on HTML 5 canvas, and make the sound more effective also can be used p5.js library.
    
Machine Learning: This JavaScript ml5.js library can be used in web development by using machine learning.

Mobile Applications: JavaScript can also be used to build an application for non-web contexts. The features and uses of JavaScript make it a powerful tool for creating mobile applications. This is a Framework for building web and mobile apps using JavaScript. Using React Native, we can build mobile applications for different operating systems. We do not require to write code for different systems. Write once use it anywhere!

## Dynamic Typing vs Static Typing

Dynamic Typing -> you can change the type of variable at runtime .

```
  let a = "hellow world"
  console.log(a);
  a = 14
  console.log(a);

```

Static Typing - First you have to define varibales the you can perform operations on it. Example - C language.

## How to Execute Javascript ?

JS can executed right inside browser's,  ---> Open console and you can start writing your code here.
Another way of exexuting Javascript is using Node js (is a run time env, you can download this and start executing js using node js).
Or You can insert javascript inside <script></script> tag in html file.

## Variables 

Variables are like container, you can store diffrent data types in it, ex --> array object number etc..

## Rules for Choosing variable name .
```
1. you can use --- letters, underscore(_), degits, $ sign
2. Can not start variable name with numbers --> example ---> let 9Store = 'Helloworld' ---> This will give you error
3. Javascript reserved keywords can not be used as a varibale name , example ---> let var = 5; ---> This will give you error
4. javascript is case senstive language .... 
ex--> let Sum = 5,
      let sum = 210; 
    Both sum and Sum are diffrent ..
```

## Var vs Let Vs Const in Javascript

Var was used before es6 ---> Rule of thumb --- Never use var , it can create bug in you projects. 

```
  1. var is globally scoped varibale
   let and const are block scoped.
   
   {
     var a = 10;
   }
   
   console.log(a) // OP 10

   {
    const  ab = 100;
    let sum = 20;
   }

    console.log(ab,sum) // Uncaught ReferenceError
  

  2. var can be updated and redecalred with in its scope
  3. let can be updated but not re-declared.
  4. const  can neither be updated not be redclared .
  5. var varibales are initilized with undefined where let and const varibale are not initialized.
  6. const must be initilized during declaration unlike let and var.

```

## Data Type In JS 
1. Primitivie (Null, Number,String, symbol, Undefined, Boolean , Big Int)
2. Non Primitive (Objects, Array).

```
Primitivie DT Examples ->
let a = null; 
let b = 3 ;
let c = true;
let d="java";
let e = BigInt("567") + BigInt("3");
let f = Symbol("Description of symbol");
let g = undefined 


Non Primitive -
1. Object - Object values are written as name : value pairs (name and value separated by a colon).
 
Const sampleObj = {
            name:'JS',
            id:123,
            Total:999,
           }

How to access object values ---> 
sampleObj.name or sampleObj['name']


2. Array - An array is a special variable, which can hold more than one value. 

Example-

let store = ['car','bike',20];

```

## Operators in JavaScript

There are different types of JavaScript operators:

    1. Arithmetic Operators
    2. Assignment Operators
    3. Comparison Operators
    4. Logical Operators
    5. Conditional Operators
    6. Type Operators  -> typeof 1

```
1. Arithmetic Operators 

Operator 	Description
    + 	  Addition
    - 	  Subtraction
    * 	  Multiplication
    ** 	  Exponentiation (ES2016) Example -> 2 ** 2 = 4 ; 2 ** 3 = 8
    / 	  Division
    % 	  Modulus (Division Remainder)  Example -> 5 % 2 = 1
    ++ 	  Increment
    -- 	  Decrement



Checkout this link for more examples - https://www.w3schools.com/js/js_operators.asp

```

## JS Strings 

we can use single quotes or double quotes or Template Literal
Example ->

```
let total = 25
let str = "hello world"
let str2 = 'hello world'
let str3 = `your age is ${total}` 

```

## String Methods 

```
JavaScript String Length 
let text = "ABCDEFGHIJKLMNOPQRSTUVWXYZ";
let length = text.length;

Slice Method - > slice() extracts a part of a string and returns the extracted part in a new string.

The method takes 2 parameters: start position, and end position (end not included)

Example -

let text = "Hello World! write your first program";
let part = text.slice(6,11);

console.log(text.slice(6));



Note

JavaScript counts positions from zero.

First position is 0.

Second position is 1.



```


## Assignment

```
1. Create a variable of type string and try to add a number to it ?
2. find the datatype of the string in last question ?
3. Create a const object in js , can you change it to hold a number later ?
4. Try to add a new key to the const object in last question,
5. Write a js program to create a word-meaning dictonary of 5 words ?
6. Write a js program to store name email phone number and marks of a student using Object?
7. Use logical operator to find whether the age of a person lies between 10 and 30 ?
8. Write a js program to find whether a number is odd or even ?

9. Convert a given string to lower case
   example "HELLO WORLD" -> hello world

10 . Your Current balance is 100 Rupees
    Extract Number from above given string.

11. Explore string methods of javascript
```
