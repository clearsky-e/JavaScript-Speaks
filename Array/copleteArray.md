here we will cover the most of the array methods

1. Concat
   this method is used to combine the arrays into a new array
   ```
   const arr = [1, 2, 3, 4,13];

    const arr1 = [5,6,7,8,9]
    
    const ab = arr.concat(arr1);
    console.log(ab);
   ```

2. slice()
   It create the copy of the array as a portion of the original array and return a new array, it does not modify the old array
   syntax
   ```
   array.slice(startIndex, endIndex);
   ```
example
```
const arr = [1, 2, 3, 4,13];

// get only the 3 and 4
const ab = arr.slice(2,4);
console.log(ab); /[3,4]
```
as you can see the slice will take the last index as excluded here


3. splice()
   it is the more advance than slice, with this the array can be replace elements or removing  old elements or adding new elements in the array
syntax
```
array.splice(startIndex, deleteCount, item1, item2, ...);
```
here,
startIndex: The index at which to start changing the array.
deleteCount: The number of elements to remove (if any).
item1, item2, ...: Items to add to the array (optional).
example
```
const arr = [1, 2, 3, 4,13];

// remove 2 and 3 then add the 12, 13,14 there
const ab = arr.splice(1,2,12,13,14);
console.log(ab); // [ 2, 3 ]
console.log(arr); // 
```



4. fill()
   the fill method is used to fill the array with the new value and it accepts the staarting and the end index also, these both start and end index are optional, if not given the start and end index then it will fill the whole array
   syntax
```
array.fill(value, start, end);
```
example
```
let arr = [1, 2, 3, 4, 5];
arr.fill(0, 2, 4);  // Filling index 2 to 4 with 0
console.log(arr);  // Output: [1, 2, 0, 0, 5]

```



5. findIndex()
   it return the index of the first element that satisfy the given callback function, If no element found then it return the -1
syntax
```
array.findIndex(callback);
```
example
```
const arr= [1,2,3,4,5,6]
const getIndex = arr.findIndex((num)=> num>5);
console.log(getIndex," this is the Index of the element which is greater than 5");
```

6. flat()
   with this method if an array have arrays eleemnt inside it, then it will just make the array flatterd means make it like the simple one array and it takes the depth also inside it, means if there are the arrays like the array inside array and tehn one more means there will be three array liek the nested tehn we can give the dpth 3 and then it will mak the array by going the depth till 3, by default it is 1, this method return the new flat array it does not change the old array
   syntax:
```
array.flat(depth);
```
example
```
const arr= [1,[2,3],4,[5,[6,7]]]

const newar = arr.flat()
const newar1 = arr.flat(2)

console.log(newar)   // [ 1, 2, 3, 4, 5, [ 6, 7 ] ]
console.log(newar1);   // [  1, 2, 3, 4, 5, 6, 7]
```


7. reverse()
   It reverse the elements of the array, It does not return a new array, It changes the original array
   example
```
const arr= [1,2,3,4,5,6,7]

arr.reverse();
console.log(arr);
```



to be continue the sort is still pending and tehn ready for te questions and asnwers
