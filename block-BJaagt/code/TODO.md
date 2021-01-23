Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

Example:

```js
function hello() {
  var username = "Arya";
}
console.log(useranme); // output
```

In above code we are looking for the variable named `usename`. There is no variable named `username` in the global scope. The variable is inside the function named `hello` and we can't access the variable defined inside a function from outside.

The above code will throw an error `Reference Error username is not defined`.

2. Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

```js
{
  const username = 'Arya';
}
console.log(useranme); // outpu

In the above code we are looking for the variable username which is defined inside a block using const.
Since username is defined inside block it will create scope and variable defined using const cannot accessible outside block
The above code will throw an error `Reference Error username is not defined`


```

3. Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

```js
if (true) {
  let username = "Arya";
}
console.log(useranme); // output
```

In the above code we are looking for the variable username which is defined inside a block using let.
Since username is defined inside block it will create scope and variable defined using let cannot accessible outside block
The above code will throw an error `Reference Error username is not defined`

4. Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

```js
if (true) {
  var username = "Arya";
}
console.log(useranme); // "Arya"
```

variable defined using keyword var can be accessible outside block. So it will give output

5. Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

```js
let username = "John";
if (true) {
  var username = "Arya";
}
console.log(useranme); // error
```

Inside if statement username is defined using var keyword and for var it doesnt create scope inside block
So it will thriow an error as username is already defined

Uncaught SyntaxError: Identifier 'username' has already been declared

6. Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

```js
let username = "John";
if (true) {
  let username = "Arya";
}
console.log(useranme); // "John"
```

both username is in two different scope one is in global scope nd other is in block scope. And variable defined using let have block scope so it wont be accessible

7. Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

```js
let username = "John";
function sayHello() {
  let username = "Arya";
}
sayHello();
console.log(useranme); // John
```

8. Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

```js
for (var i = 0; i < 10; i++) {
  console.log(i, "First"); // 0 1 2 3 4 5 6 7 8 9
}
console.log(i, "Second"); // 10, second
```

variable defined using var doesnt have local scope so it can be accesible outside the block 9. Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

```js
for (let i = 0; i < 10; i++) {
  console.log(i, "First"); // output
}
console.log(i, "Second"); // output
```

0 "First"
1 "First"
2 "First"
3 "First"
4 "First"
5 "First"
6 "First"
7 "First"
8 "First"
9 "First"
VM124:4 Uncaught ReferenceError: i is not defined
at <anonymous>:4:13

    i is defined using let so it wont be accessible outside the block
