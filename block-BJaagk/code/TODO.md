1. Convert the function below into different forms of function expression.

```js
function percentage(marks, total) {
  return (marks * 100) / total;
}

// Your code goes here

var perctange = function percentage(marks, total) {
  return (marks * 100) / total;
};
var perctange = function (marks, total) {
  return (marks * 100) / total;
};
var perctange = (marks, total) => {
  return (marks * 100) / total;
};
var perctange = (marks, total) => (marks * 100) / total;
```

2. Write Function Declaration or Function Expression next to the function.

```js
function percentage(marks, total) {
  return (marks * 100) / total;
}
// Your answer

var perctange = function percentage(marks, total) {
  return (marks * 100) / total;
};
var perctange = function (marks, total) {
  return (marks * 100) / total;
};
```

```js
let percentage = function percentage(marks, total) {
  return (marks * 100) / total;
};

function percentage(marks, total) {
  return (marks * 100) / total;
}
```

```js
let percentage = function (marks, total) {
  return (marks * 100) / total;
};

function percantage(marks, total) {
  return (marks * 100) / total;
}
```

```js
let percentage = (marks, total) => {
  return (marks * 100) / total;
};
function percantage(marks, total) {
  return (marks * 100) / total;
}
```

```js
let percentage = (marks, total) => (marks * 100) / total;
function percantage(marks, total) {
  return (marks * 100) / total;
}
```

3. Why is a function definition an expression in JavaScript? Give one example of function expression.

funcation definantion or declaration means we are defining any new function using keyword function. ANd we all know any function in javascript is first class object. And defining any object is an expression in javascript.

example:
function add(a,b){
return a+b;
}

4. Why is a function call an expression in JavaScript?
   function call always return any value either primitive data type or non pritimive value.

5. Write VALID and INVALID next to each example below with the reason.

```js
function add(a, b) {
  return a + b;
}

let five = add(2, 3); // valid
five = add; // invalid as add is just function reference which is sets of statement
five = five(10, 11); // valid
five = function () {
  return "Hello";
}; // valid
```

6. What is the difference between function definition and function call? Explain with an example.

function definition is defining any function with using function keyword which contain different sets of statement and return.

where function call is calling the function by poassing argument in the function

example:
function definition
function add(a,b){
return a+b;
}

function call:
add(5,6);

7. What is the similarities between function definition and function call?

both are an expression as function defintion is a type of object. where function call will return any value.

8. Is the code below valid or invalid. Explain with reason.

```js
function hello() {
  console.log("Hello World!");
}

hello.user = "Sam"; // valid  as function is type of object so we can treat it as an object
```

9. What is higher order function explain with an example.

higher order function is special type of function which can return a function or also it accept a function as parameter

10. Explain what is callback function. Why you can pass a function inside a function?

Call back function is a function which can be passed in other function i.e. HOF. Because function is an expression or an object so we can pass it as parameter inside a function
