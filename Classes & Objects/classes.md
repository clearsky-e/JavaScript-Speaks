---- classes ----

In Javascript the classes are the other way to create the objects, the classes are the blueprint to create the objects

syntax
```
class myClass {
method1;
method2;
}

let myobj = new myClass();

```


Example
```

class MyNew {
    start(){
        console.log("this is the start");
        console.log("")
    }
    
    end(){
        console.log("this is the end")
    }
}

let myObj = new MyNew();
myObj.end() // this is the end

```



Constructor
this is the another but very important concept in the Javascriotp related to the Classes and the objects

the constructor are the methods created automatically in the classes, the moment is object is created for any class, we can also manually create the constructor if not created then it
will create the automatically the constructor and they will call also automatically the moment we create the objects

```
class Employee {
        constructor(name){
            
            console.log("the constructor name is ",name );
            
        }
        calTax() {
          console.log("Tax is calculated");
        }
      }
      let vivad = new Employee("bilal");
     //It will automatically print this the constructor name is bilal
```





Inheritance
It means passing down the properties from the parents class to its child class, to inherit the property of teh parent class it uses the keyword "extend"
```
 class Person {
        eat() {
          console.log("I am eating");
        }
      }

      class Employee extends Person {
        work() {
          console.log("I am doing my work");
        }
      }
      let vivad = new Employee();
     vivad.eat() //I am eating
```


