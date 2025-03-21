----Loops----

the basic loops are these 3 for, while and do-while
and here we are gonna learn the for-in , for-of and forEach

. for-in, this is the loop specially made for the objects and it iterates on the objesct key
```
 const myObj = {
      'name':"Aakash",
      'age': 24,
      }
      //using the for-in loop
      for(let key in myObj){
        console.log("key: ",key, "and the value is: ", myObj[key])
      }
```



.for-of, this loop is basically made for the data which are in the type of iterable like the arrays, map, string and etc.
```
      const name = "Aakash Singh";
      const myArray = [1,4,3,2]

      for (let va of myArray){
      console.log("this is the value", va)
      }

      for (let va of name){
      console.log("value of string: ",va);
      }

```


.forEach, thsi is specially made for the array and it accept the callack function which will be applied on the each element, 
in this callback we wwill send the element of the array and the index also
```
      const arr = [2, 3, 4, 5, 61, 1];
      arr.forEach(function (a, index) {
        let b;
        b = a * a;
        console.log("element ",a, "at index ",index, "and the square is ",b);
      });

```
