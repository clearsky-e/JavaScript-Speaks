---- Higher Order Function ----

the higher order functions are the functions which does either of the following
    . takes the function as the argument
    . return the function as the result

exmaple
```
function fun1(){
      console.log("hello this is the fun1")
      }

      function two(work){
      work();
      }

      two(fun1)

```


most famous and prebuild js higher order functions are thses

.map function , it apply a callback function on the each element of the array and then return a new array
in this function it can take the element and the index of the array
syntax:
```
arr.map((currentValue, index, array) => { /* ... */ });
```
example:
```
const ar = [1,2,3,4,5,6]

newa = ar.map((el)=>{
    return el*el;
})

console.log(newa);
```



.filter, this is the function applied on the array here, it helps to filter out the array based on a specific condition given in the callback function
syntax:
```
arr.filter((currentValue, index, array) => { /* ... */ });
```

example
```
const ar = [1,2,3,4,5,6,7,8,9,10]

// get the array of the odd elements only
newa = ar.filter((el,index)=>{
    return el%2!=0;
})

console.log(newa); //[ 1, 3, 5, 7, 9 ]
```


.reduce,  this is the another method wehre it will perform the calculation defined in the callback function and then reduce the whole array into the single value
syntax
```
arr.reduce((accumulator, currentValue, index, array) => { /* ... */ }, initialValue);
// so here we can give the initial value or it will take the first element of the array as the initaial value
```
example
```
const ar = [1,2,3,4,5,6,7,8,9,10]

// sums uo the array
newa = ar.reduce((prev,el,index)=>{
    return prev+el;
},0)

console.log(newa); //55
```




.find, this finds the element and return the first element fromm teh array if that matches the given condition in the callback and if the no element is found with the given condition 
then it return the undefined
syntax:
```
array.find(callback(element, index, array), thisArg);
```
example
```
const ar = [1,2,3,4,5,6,7,8,9,10]

// find the number greater than 5
newa = ar.find((el,index)=>{
    return el>5;
},0)

console.log(newa);
```
here us see we have this thisArg also, it means if we want to use the this keyword here so where to look for this , it simply means we can give the object here so that 
when the time we will use the this keyword then the this keyword will simply look at this object example
```
const obj = {
  value: 10,
};

const arr = [1, 2, 3, 4,13];

const result = arr.find(function (num) {
  
  return num > this.value;  // `this` will refer to `obj`
}, obj);  // Here, we explicitly set `thisArg` to `obj`

console.log(result);  //13, since 13 is the bigger than 10 

```

we dont use that much this thisarg so which is why it is optionsal too






. some(), this is the method that return the true or false based on the codiion that is defined in the callback function,
if any of the element matched the condtion provided in the callback then it just return true else false
syntax
```
array.some(callback(element, index, array), thisArg);
```

example
```

const arr = [1, 2, 3, 4,13];

const result = arr.some(function (num) {
  
  return num>18;
});  

console.log(result);   // false
```



.every, it is the mostly same as the some but it checks the every element of the array , means if every element of the array if it matches with the given condition then only it will 
return true else false
syntax
```
array.every(callback(element, index, array), thisArg);
```


example
```
const arr = [1, 2, 3, 4,13];

const result = arr.every(function (num) {
  
  return num>10;
});  

console.log(result);   //false
```




