----this----

.In javascript 'this' keyword is nothing but an environment where the code is running, and it contain the value depends on how we call it and where it is being called.
just go through some rules and example you will understand



. When we use 'this' at the top then it referes to the global object
```
console.log(this) //Window {window: Window, self: Window, document: document, name: '', location: Location, …}
```



.In a Function if we call it then also it is pointing to the global 
```
…
   function myFunction() {
            console.log(this);  //Window {window: Window, self: Window, document: document, name: '', location: Location, }
        }
        myFunction();
```
but if the function is inside a object then this will point to the object
```
 const obj = {
            name: 'sakib',
            print: function(){
                console.log(this); // {name: 'sakib', print: ƒ}
                console.log(this.name) // sakib
            }
        }
        obj.print(); 
```



. this keyword do not work same in the arraow function, here it will point to the outer parent 
```
const person = {
    name: "Aakash",
    greet: () => {
        console.log(this.name); // undefined
        console.log(this);      // Window {window: Window, self: Window, document: document, name: '', location: Location, …}
                                // since the window object do not have the name key it is showing the udefinded, so if we want to access the keys in this condition then we shuld use the normal arrow function
    }
};
person.greet(); 
````



.lets understand the constructor function in js, 
if a function is cerated and then a new instance is created of that function means we have created a constructor
the constructor are used to create the instance and give some initial values to the instance
please see this example we have
```
function Hello() {
  console.log("hello there"); //hello there
}
const a = new Hello();
```
this is very basic example of the constructor, here we create the instance of the function Hello with the new keyword but this is useless constructor as it does
not contain any value and not setting anything the main purpose of the constructor is to set the values of that instance


now see this example
```
function Person(name, age) {
        this.name = name;
        this.age = age;
        this.greet = function() {
          console.log(
            `Hello Dear ${name} and your age: ${age} is perfect for being a person`
          );
        };
      }

      const A = new Person("Sughrev", 228);
      const B = new Person("Jamvant", 332);

        A.greet();  //Hello Dear Sughrev and your age: 228 is perfect for being a person
        B.greet();  //Hello Dear Jamvant and your age: 332 is perfect for being a person
```
okay first, if we dont use the this keyword here then it wont work the same as it doing right now, since this keyword points to the current instance in the case of cunstructor and 
avery variable to access it in the constructor function we have to use the this keyword with all the variables
