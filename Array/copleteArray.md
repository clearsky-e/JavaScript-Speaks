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
to be continued
