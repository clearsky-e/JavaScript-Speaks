-----Math------

.In javascrip the math object is a built in object, and it is not creted with the help of the new keyword it is already there to use


Method	Description	Example
```
Math.abs(x)	Negative number ko positive banata hai	Math.abs(-10) → 10
Math.round(x) 	Nearest integer pe round karta hai	Math.round(4.7) → 5
Math.floor(x)	Nearest lower integer deta hai	Math.floor(4.9) → 4
Math.ceil(x)	Nearest upper integer deta hai	Math.ceil(4.1) → 5
Math.trunc(x)	Decimal hata kar integer deta hai	Math.trunc(4.9) → 4
Math.pow(x, y)	x ki power y return karta hai	Math.pow(2, 3) → 8
Math.sqrt(x)	Square root nikalta hai	Math.sqrt(16) → 4
Math.cbrt(x)	Cube root nikalta hai	Math.cbrt(27) → 3
Math.max(a, b, c...)	Sabse bada number return karta hai	Math.max(10, 20, 5) → 20
Math.min(a, b, c...)	Sabse chhota number return karta hai	Math.min(10, 20, 5) → 5
Math.random()	0 aur 1 ke beech random number deta hai	Math.random() → 0.5738
```


.Math.random() ye ek method h jo random number deta h, ye hamesha 0 se 1 k bich me random number deta h
``` console.log(Math.random()); ```

here if we want to get the random number between a specific min and max numbers then, we have this formula
```
const min = 10;
const max = 20;
//in this case we are gettign the randome numbers in between the 10 and 20 

console.log(Math.floor(Math.random() *(max-min + 1))+ min)

```
