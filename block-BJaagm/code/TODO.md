1. What does thread of execution means in JavaScript?

It means how javascript engine execute any code in sequence like one by one.

2. Where the JavaScript code gets executed?

in javascript engine

3. What does context means in Global Execution Context?

Global execution context is an envrionemnt where all the codes get exceuted by js engine.

4. When do you create a global execution context.

It get created whenever we run any peice of code JS engine will create a global execution context

5. Execution context consists of what all things?

It contain two parts one is memory where all the decalartion happen and it stores variable data and function. In other part execution takes place like any operation.

6. What are the different types of execution context?
   There are two types of execution : Global execution context and function execution context.

Global execution will be created once any code will be execute it may contain variable declration, function declration or operation.

But when any function get executed it create function execution context

7. When global and function execution context gets created?

whenever any code get executed n javascript engine

8. Function execution gets created during function execution or while declaring a function.

it will be executed during function execution

9. Create a execution context diagram of the following code on your notebook. Take a screenshot/photo and store it in the folder named `img`. Use `![](./img/image-name.png)` to display it here.

```js
var user = "Arya";

function sayHello() {
  return `Hello ${user}`;
}

var userMsg = sayHello(user);
```

<!-- Put your image here -->

![](1st.jpg)

```js
var marks = 400;
var total = 500;

function getPercentage(amount, totalAmount) {
  return (amount * 100) / totalAmount;
}

var percentageMarks = getPercentage(marks, total);
var percentageProfit = getPercentage(400, 200);
```

<!-- Put your image here -->

![](2nd.jpg)

```js
var age = 21;

function customeMessage(userAge) {
  if (userAge > 18) {
    return `You are an adult`;
  } else {
    return `You are a kid`;
  }
}

var whoAmI = customeMessage(age);
var whoAmIAgain = customeMessage(12);
```

<!-- Put your image here -->

![](3rd.jpg)
