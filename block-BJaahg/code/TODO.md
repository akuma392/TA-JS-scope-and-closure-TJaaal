## Understanding Scope and the difference between var, let and const

Watch this video before doing the exercise: https://www.youtube.com/watch?v=XgSjoHgy3Rk

1. Guess the output:

```js
let firstName = 'Arya';
const lastName = 'Stark';
var knownAs = 'no one';

console.log(
  window.firstName,
  window.lastName
  window.knownAs
);

//  window.firstName, output undefined
  // window.lastName output undefined
  // window.knownAs output "no one"
```

2. Guess the output:

```js
let firstName = "Arya";
const lastName = "Stark";
var knownAs = "no one";

function fullName(a, b) {
  return a + b;
}

console.log(window.fullName(firstName, lastName)); //AryaStark
```

3. Make a Execution Context Diagram for the following JS and write the output.

```js
fucntion addOne(num){
  return num + 1;
}
var one = addOne(0);
var two = addOne(1);
console.log(one, two);//1 2
```

![](./img/3rd.jpg)

4. Make a Execution Context Diagram for the following JS and write the output.

```js
var one = addOne(0);
function addOne(num) {
  return num + 1;
}
var two = addOne(1);
console.log(one, two); // 1 2
```

![](./img/4th.jpg)

5. Make a Execution Context Diagram for the following JS and write the output.

```js
console.log(addOne(0)); //1
function addOne(num) {
  return num + 1;
}
var two = addOne(1);
console.log(two); //2
```

![](./img/5th.jpg)

6. Make a Execution Context Diagram for the following JS and write the output.

```js
var one = addOne(0);
const addOne = (num) => {
  return num + 1;
};
var two = addOne(1);
console.log(two);
```

it will throw an error :Uncaught ReferenceError: Cannot access 'addOne' before initialization
at <anonymous>:1:13
as addone is still in decalartion phase when execution starts for one
![](./img/6th.jpg)

7. Make a Execution Context Diagram for the following JS and write the output.

```js
console.log(addOne(0));
const addOne = (num) => {
  return num + 1;
};
var two = addOne(1);
console.log(two);
```

it will throw an error :Uncaught ReferenceError: Cannot access 'addOne' before initialization
at <anonymous>:1:13
as addone is still in decalartion phase when execution starts for one
![](./img/6th.jpg)

8. What will be the output of the following

```js
function isAwesome() {
  var awesome;
  if (false) {
    awesome = true;
  }
  console.log(awesome);
}
isAwesome(); //undefined
```

9. What will be the output of the following

```js
function isAwesome() {
  let awesome;
  if (true) {
    awesome = true;
  }
  console.log(awesome);
}
isAwesome(); //true
```

10. What will be the output of the following

```js
function isAwesome() {
  let awesome;
  if (false) {
    awesome = true;
  }
  console.log(awesome);
}
isAwesome(); //undefined
```

11. What will be the output of the following

```js
let firstName = "Arya";
const lastName = "Stark";
var knownAs = "no one";

function fullName(a, b) {
  return a + b;
}
const name = fullName(firstName, lastName);
console.log(name); //AryaStark
```

12. Guess the output of the code below with a reason.

```js
function sayHello() {
  let name = "Arya Stark";
}
sayHello(); //undefined as no return statement

console.log(name); // undefined
```

13. Guess the output of the code below with a reason.

```js
if (true) {
  var name = "Arya Stark";
}
console.log(name); // ARya Stark
```

14. Guess the output of the code below with a reason.

```js
if (true) {
  let name = "Arya Stark";
}
console.log(name); // "Arya Stark"
```

15. Guess the output of the code below with a reason.

```js
for (var i = 0; i < 20; i++) {
  //
}
console.log(i); //20 loop will run till 0 to 19 once it will come out i will be incremented and since it is defined using var so it can be accessible.
```

16. Guess the output of the code below with a reason.

```js
for (let i = 0; i < 20; i++) {
  //
}
console.log(i); // error "i" is not defined as let create block scope
```

17. Guess the output and the reason behind that.

```js
function sample() {
  if (true) {
    var username = "John Snow";
  }
  console.log(username);
}
sample(); // "John Snow" , var create only function scope so it can be accessed outside the block
```

18. Guess the output and the reason behind that.

```js
function sample() {
  if (true) {
    let username = "John Snow";
  }
  console.log(username);
}
sample(); //error username is not defined as it isdefined inside the block
```

19. Guess the output and the reason behind that.

```js
function sample() {
  var username = 'Arya Stark';
  if (true) {
    var username = 'John Snow';
    console.log(username);
  }
  console.log(username, 'second');
}
sample();//John Snow

John Snow ,"second"
```

20. Guess the output and the reason behind that.

```js
function sample() {
  let username = "Arya Stark";
  if (true) {
    let username = "John Snow";
    console.log(username, "first");
  }
  console.log(username, "second");
}
sample(); // John Snow first

// Arya STark second
```

var create only function scope where let create block & function scope

21. Guess the output and the reason behind that.

```js
function sample(...args) {
  for (let i = 0; i < args.length; i++) {
    let message = `Hello I am ${args[i]}`;
    console.log(message);
  }
}

sample("First", "Second", "Third");
// Hello I am first
//Hello I am second
//Hello I am Third
```

by using ...args it will store all the input in the new array

22. Guess the output and the reason behind that.

```js
function sample(...args) {
  for (let i = 0; i < args.length; i++) {
    const message = `Hello I am ${args[i]}`;
    console.log(message);
  }
}

sample("First", "Second", "Third"); //
// Hello I am first
//Hello I am second
//Hello I am Third
```

23. Guess the output and the reason behind that.

```js
if (true) {
  const myFunc = function () {
    console.log(username, "Second");
  };
  console.log(username, "First");
  let username = "Hello World!";
  myFunc();
}
```

// cannot access the username before intialising it. It will throw an error.

24. Guess the output and the reason behind that.

```js
function outer() {
  let movie = "Mad Max: Fury Road";
  function inner() {
    console.log(`I love this movie called ${movie.toUpperCase()}`);
  }
  inner();
}

outer(); //I love this movie called MAD MAX: FURY ROAD

// when inner function will execute it will carry the movie variable as closure
```

25. Guess the output and the reason behind that.

```js
function outer() {
  let movie = "Mad Max: Fury Road";
  function inner() {
    let movie = "Before Sunrise";
    console.log(`I love this movie called ${movie.toUpperCase()}`);
  }
  inner();
}

outer(); //I love this movie called BEFORE SUNRISE
// when inner function will get execute it will try to find in its memory and its already there so it wont go further to check closure
```

26. Guess the output and the reason behind that.

```js
function outer() {
  let movie = "Mad Max: Fury Road";
  function inner() {
    let movie = "Before Sunrise";
    function extraInner() {
      let movie = "Gone Girl";
      console.log(`I love this movie called ${movie.toUpperCase()}`);
    }
    extraInner();
  }
  inner();
}
outer(); // "I love this movie called "GONE GIRL""
// when extrainner function will execute it will check its memory and it will find gone girl text and it will print.
```

30. Using reduce find the final value when the initial value passed is `100`. You have to pass the output of one function into the input of next function in the array `allFunctions` starts with `addOne` ends with `half`.

```js
const addOne = (num) => {
  return num + 1;
};
const subTwo = (num) => {
  return num - 2;
};
const multiplyThree = (num) => {
  return num * 3;
};
const half = (num) => {
  return num / 2;
};

let allFunctions = [addOne, subTwo, multiplyThree, addOne, multiplyThree, half];

function reduce(acc, ...cv) {
  for (let i of cv) {
    acc = cv(acc);
  }
  return acc;
}

reduce(100, allFunctions);

let result = allFunctions.reduce((acc, cv) => {
  acc = cv(acc);
  return acc;
}, 100);
console.log(result); //447
// Answer is: 447
```
