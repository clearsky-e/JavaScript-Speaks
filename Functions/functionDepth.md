here we will discuss various concepts about the functions 

. Arguments and Parameter
in functions the arguments are the actual value we use when we call a function
```
greet("Alice");  // "Alice" is an argument
```

the parameter are the vales a function receives in its declaaration
```
function greet(name) {  // "name" is a parameter
  console.log("Hello, " + name);
}

```



. function statement
function statement is the function declaration
example: here we have a simple function, this is called teh function statement
```
function abc(){
console.log("hello there this is the function")
}
```


. function expression
when a function is assign to a variable this is called function expression and this fumction could be annonymus or named
```
const greet = function() {
  console.log('Hello!');
};

```


.annonymyus function
An anonymous function is a function that doesn't have a name and is often used directly where it's needed, like in a variable or as a callback.
```
const greet = function() {
  console.log('Hello!');
};
greet(); // Output: Hello!
```
In this example, the function is anonymous because it doesn't have a name, but it's assigned to the variable greet, and you can call it using greet()









. Callback 
the callbacks are the function send to the another functions as a argument
```

function fetchData(callback) {
  setTimeout(() => {
    console.log('Data fetched!');
    callback();  // Calls the callback once data is fetched
  }, 2000);
}

function displayMessage() {
  console.log('Displaying message after fetching data');
}

fetchData(displayMessage);
```

the main purpose of using the callbacks are simple, first they mostly used in the asynchronous programming means when we are fetching the data or doing a task asyncronously, so at this point we just want to send a function as set of all task we want to tell, it should be done in the asynhronous function , that this function should run 

CALLBACK HELL
Callback hell happens when you have too many nested callbacks in asynchronous code, making it difficult to read and maintain.
You can avoid callback hell by using Promises or async/await, which allow you to manage asynchronous code in a more linear and readable way.

















. First-class functions in JavaScript mean that functions which are treated as first-class citizens. This means that functions can be:

  Assigned to variables.
  Passed as arguments to other functions.
  Returned from other functions.
  Stored in data structures like arrays or objects.

A first-class function is just a function that can be used like any other value (such as a number or string).

lets have few examples

Assigned to a variable:
```
const greet = function() {
  console.log('Hello!');
};
greet(); // Output: Hello!
```

Passed as an argument to another function:
```
function callFunction(fn) {
  fn();  // Calls the function passed as an argument
}


callFunction(function() {
  console.log('Hello from the passed function!');
});
// Output: Hello from the passed function!
```


Returned from another function:
```
function getGreeting() {
  return function() {
    console.log('Hello from returned function!');
  };
}

const greet = getGreeting();
greet(); // Output: Hello from returned function!
```
