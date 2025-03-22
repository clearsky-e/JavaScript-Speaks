----Modifying the Array---

We can modify the array with the help of this shft, unshift and push, pop method






1. shift() and unshift()
Both of these methods modify the beginning of an array.

shift(): Removes the first element of an array and returns that element. It mutates the array.
Syntax:
```
array.shift();
```
Example:
```
const arr = [1, 2, 3, 4];
const firstElement = arr.shift();  // Removes 1
console.log(firstElement);  // Output: 1
console.log(arr);  // Output: [2, 3, 4]

```


unshift(): Adds one or more elements to the beginning of an array and returns the new array length.

Syntax:
```
array.unshift(element1, element2, ...);
```

Example:
```
const arr = [2, 3, 4];
const newLength = arr.unshift(1);  // Adds 1 at the beginning
console.log(arr);  // Output: [1, 2, 3, 4]
console.log(newLength);  // Output: 4
```


2. push() and pop()
These methods modify the end of an array.

push(): Adds one or more elements to the end of an array and returns the new array length.

Syntax:
```
array.push(element1, element2, ...);
```

Example:
```
const arr = [1, 2, 3];
const newLength = arr.push(4, 5);  // Adds 4 and 5 at the end
console.log(arr);  // Output: [1, 2, 3, 4, 5]
console.log(newLength);  // Output: 5
```


pop(): Removes the last element of an array and returns that element. It mutates the array.

Syntax:
```
array.pop();
```

Example:
```
const arr = [1, 2, 3, 4];
const lastElement = arr.pop();  // Removes 4
console.log(lastElement);  // Output: 4
console.log(arr);  // Output: [1, 2, 3]
