here we will discuss various concepts about the functions 

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
