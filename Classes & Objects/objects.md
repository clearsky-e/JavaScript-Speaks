---- Object ----

In Javascript the objects stores the methods and properties in the key and value pair
in JS there is a special property called the prototype
this prototype contain the lot of different methods that can be used to apply on the object
we can set the prototype useing the 
```
__proto__
//it have the 2 underscore with it 
```
example
```
        const Employee = {
            tax:function calTax(){
                console.log("Tax is calculated");
            }
        }

      const newEmp = {
          name:"Arjun"
      }

      newEmp.__proto__ = Employee

      console.log(newEmp);
//here now with this a calTax metod will be available in the newEmp too as a prototype method

```

if the method in the prototype and the method in the object have the same name then the priority will be given to the method in the object


