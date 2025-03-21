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

also remember that, for-of only works on iterables (arrays, strings, maps, sets).
but if we have to use the for-of with the objects, then we will use the Object.value() method so that we will get the values only from the object so that it will act as the iterable
```
const obj = {"name":"Aakash", "age":24, "company":"asionex"}

for(let va of Object.values(obj)){
console.log(va);
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
rememebr that forEach is a function that iterates not a proper loop
so here we cant use the break inside this

also the forEach dont return anything it just iterate and perform the callback function
```
const arr = [5, 10, 15];

const newArr = arr.forEach((num) => num * 2);

console.log(newArr); //undefined
```

so if we want to ger back an array then use the other array methods just like map

```
const arr = [5, 10, 15];

const newArr = arr.map((num) => num * 2);

console.log(newArr);  //[10, 20, 30]
```
