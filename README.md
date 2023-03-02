# JS_Session_2

## Function Introduction
A function is a "subprogram" that can be called by code external (or internal, in the case of recursion) to the function. Like the program itself, a function is composed of a sequence of statements called the function body. Values can be passed to a function as parameters, and the function will return a value.

In JavaScript, functions are first-class objects, because they can be passed to other functions, returned from functions, and assigned to variables and properties. They can also have properties and methods just like any other object. What distinguishes them from other objects is that functions can be called.

## Function Declaration/Defination or statement ?
A function definition (also called a function declaration, or function statement) consists of the function keyword, followed by:
```
The name of the function.
A list of parameters to the function, enclosed in parentheses and separated by commas.
The JavaScript statements that define the function, enclosed in curly brackets, { /* … */ }.

Example - function square (num){
 return num * num
}

```


## What is Function Expression ?
A function expression is very similar to and has almost the same syntax as a function declaration. The main difference between a function expression and a function declaration is the function name, which can be omitted in function expressions to create anonymous functions.
In simple term -> When you store a function inside a variable ,it's callled function expression.

```
const square = function (num) {
    return num * num 
}

// here this part is called Anonymous Function
function (num) {
    return num * num 
} 

Anonymous Function -  Function which have no name, it's used in a place where functions are treated as value. 

```

## How to call function expression ?
We can call this like a normal function ==> square(5);

## Function hoisting ?
```
console.log(square(5)); // 25

function square(n) {
  return n * n;
}
```
This code runs without any error, despite the square() function being called before it's declared. This is because the JavaScript interpreter hoists the entire function declaration to the top of the current scope, so the code above is equivalent to:

```
// All function declarations are effectively at the top of the scope
function square(n) {
  return n * n;
}

console.log(square(5)); // 25
```

Function hoisting only works with function declarations — not with function expressions. The code below will not work.

```
console.log(square); // ReferenceError: Cannot access 'square' before initialization
const square = function (n) {
  return n * n;
};
```

## What are First Class Function ?

A programming language is said to have First-class functions when functions in that language are treated like any other variable. For example, in such a language, a function can be passed as an argument to other functions, can be returned by another function and can be assigned as a value to a variable.

1. Assigning a function to a variable
```
const foo = () => {
  console.log("foobar");
};
foo()
```
2. Passing a function as an argument

```
function sayHello() {
  return "Hello, ";
}
function greeting(helloMessage, name) {
  console.log(helloMessage() + name);
}
// Pass `sayHello` as an argument to `greeting` function
greeting(sayHello, "JavaScript!");
// Hello, JavaScript!
```
3. We can return function from another function

## Function Scope

Variables defined inside a function cannot be accessed from anywhere outside the function, because the variable is defined only in the scope of the function. However, a function can access all variables and functions defined inside the scope in which it is defined.

In other words, a function defined in the global scope can access all variables defined in the global scope. A function defined inside another function can also access all variables defined in its parent function, and any other variables to which the parent function has access.


```
// The following variables are defined in the global scope
const num1 = 20;
const num2 = 3;
const name = "Chamakh";

// This function is defined in the global scope
function multiply() {
  return num1 * num2;
}

multiply(); // Returns 60

// A nested function example
function getScore() {
  const num1 = 2;
  const num2 = 3;

  function add() {
    return `${name} scored ${num1 + num2}`;
  }

  return add();
}

getScore(); // Returns "Chamakh scored 5"

```

## Param vs argument

```
function sum(a,b){  ===> When we receive values inside the function it is called as params
    return a+b;
}

sum(5,4) ===> Arguments
```


## Closures in JS

Functions bundled together with it's lexical scope together makes a closure, 

Lexical Environment = local memory + lexical env of its parent. Hence, Lexical Environement is the local memory along with the lexical environment of its parent.

Lexical: In hierarchy, In order.

Closures are one of the most powerful features of JavaScript. JavaScript allows for the nesting of functions and grants the inner function full access to all the variables and functions defined inside the outer function (and all other variables and functions that the outer function has access to).

However, the outer function does not have access to the variables and functions defined inside the inner function. This provides a sort of encapsulation for the variables of the inner function.

Also, since the inner function has access to the scope of the outer function, the variables and functions defined in the outer function will live longer than the duration of the outer function execution, if the inner function manages to survive beyond the life of the outer function. A closure is created when the inner function is somehow made available to any scope outside the outer function.

```
// The outer function defines a variable called "name"
const pet = function (name) {
  const getName = function () {
    // The inner function has access to the "name" variable of the outer function
    return name;
  };
  return getName; // Return the inner function, thereby exposing it to outer scopes
};
const myPet = pet("Hello JS");

myPet(); // Returns "Hello JS"

```

JavaScript has a lexcial scope environment. If a function needs to access a variable, it first goes to its local memory. When it does not find it there, it goes to the memory of its lexical parent. 
// See Below code, Over here function y along with its lexical scope i.e. (function x) would be called a closure.
```
function x() {
    var a = 7;
    function y() {
      console.log(a);
    }
    return y;
  }
  var z = x();
  console.log(z); // value of z is entire code of function y.
  In above code, When y is returned, not only is the function returned but the entire closure (fun y + its lexical scope) is returned and put inside z. 
  So when z is used somewhere else in program, it still remembers var a inside x()

```

## Assignment

1. Write a function that takes an integer minutes and converts it to seconds.
2. Create a function that takes a number as an argument, increments the number by +1 and returns the result.
3. Create a function that takes an array containing only numbers and return the first element.
4. Create a function that takes a number as its only argument and returns true if it's less than or equal to zero, otherwise return false.
5. What is fat arrow function, Solve above given problems using fat arrow functions , Difference bw fat arrow function and normal function ?
6. Will the below code still forms a closure?
```
function outer() {
  function inner() {
    console.log(a);
  }
  var a = 10;
  return inner;
}
outer()();
 ```
 7. Will inner function have the access to outer function argument?
 ```
function outer(str) {
  let a = 10;
  function inner() {
    console.log(a, str);
  }
  return inner;
}
outer("Hello There")(); 

```

8. In below code, will inner form closure with outest?
```

function outest() {
  var c = 20;
  function outer(str) {
    let a = 10;
    function inner() {
      console.log(a, c, str);
    }
    return inner;
  }
  return outer;
}
outest()("Hello There")();

```

9. Output of below code and explaination?
```
function outest() {
  var c = 20;
  function outer(str) {
    let a = 10;
    function inner() {
      console.log(a, c, str);
    }
    return inner;
  }
  return outer;
}
let a = 100;
outest()("Hello There")();
``
