----IIFE-----


.IIFE stands for Immediately Invoked Function Expression, and it runs as soon as it is defined
It have a little different syntax
```
       //iife with the arrow function
        (()=>{
            console.log('hello world');
        })();

//here remember that add the ; at the end of this iife since js dont know where to stop the execution context so we use this ; in the end

        //iife with the normal function
        (function(){
            console.log('hello world');
        })();
```

but why to use this iffe, there are couple of reason

. Encapsulation & Data Privacy
with this we cant access the variable inside this function but still can call the function, ex:
```
       const a = 
           (function (){
            let count = 0;
            return {
                increment:function(){
                    count++;
                    console.log(count);
                },
                decrement:function(){
                    count--;
                    console.log(count);
                }
            }


        })();

        a.increment(); //1
        a.increment(); //2
console.log(a.count); // ❌ Undefined (Private Variable)
```


. Avoid Polluting the Global Scope
Variables declared inside an IIFE stay inside and don’t affect the global scope.
```
(function () {
  var message = "Hello, Aakash!";
  console.log(message);
})();
console.log(message); // ❌ Error! message is not defined
```
Benefit: Prevents variable name conflicts.


**There are different tyoes of iife**


1. Anonymous Function IIFE
```
(function () {
  console.log("Anonymous IIFE");
})();

```

2. Named Function IIFE
```
(function myIIFE() {
  console.log("Named IIFE");
})();
```

3. Arrow Function IIFE
```
(() => {
  console.log("Arrow Function IIFE");
})();
```

4. IIFE with Parameters
```
(function (name) {
  console.log("Hello, " + name);
})("Aakash");
```

