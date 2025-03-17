-------NUMBERS-----------
. In javascript we have only the Number type to store the numbers and other int type data, like the int , float and big int etcc. not like other language they have differnt types to store 
the int and float and number , but in javascript all numbers will be stored in the Number data type
when we do this 
```
let a = 10; //it means we define a variable with the 10 value , here 10 is premitive datatype(means javascript initially define the 10 as a premitive datatype, but wehn we try to find the
              type of this variable it gives the number and if we try to perform any operation on it then also we have to use the number )
```
so we can say the numbers in the javascript are nothing but the primitive values
but the Number is an built in object in the javascript
```
let a = 123; //it is a premitive type
console.log(typeof a); //number
```
if we create a number using the new keyword like this
```
let a = new Number(10);
let b = 10;
console.log(typeof a); //object
console.log(a==b) //true
console.log(a===b) //false
```

. NaN, stands for the Not a Number in javascript, mwnas in JS we got this output "NaN", when the javascript expacts the number but get something else
for example:
```
console.log(1 * "Heloo there") //NaN
```

. We have few methods in the javascript with the Numbers like 
```
let a = 10;
console.log(a.toFixed(2)); //10.00
console.log(Number.isNaN(a)); //false
console.log(Number.isInteger(a)); //true



