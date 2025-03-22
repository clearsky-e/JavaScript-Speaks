1. Spread Operator (...)
The spread operator is used to unpack elements from an array or object and spread them out. It allows you to easily copy or combine arrays/objects, or pass arguments to a function.

Example with Arrays:
Copying an array:
```
const arr1 = [1, 2, 3];
const arr2 = [...arr1];  // Spread arr1 into arr2
console.log(arr2);  // Output: [1, 2, 3]
```

The spread operator unpacks all the elements of arr1 and creates a new array arr2 with the same elements.

Combining arrays:
```
const arr1 = [1, 2];
const arr2 = [3, 4];
const combinedArr = [...arr1, ...arr2];  // Spread both arrays into a new one
console.log(combinedArr);  // Output: [1, 2, 3, 4]
```

Example with Objects:
Copying an object:
```
const obj1 = { name: "Alice", age: 25 };
const obj2 = { ...obj1 };  // Spread obj1 into obj2
console.log(obj2);  // Output: { name: 'Alice', age: 25 }
```
The spread operator creates a shallow copy of the object obj1 into obj2.

Merging objects:
```
const obj1 = { name: "Alice" };
const obj2 = { age: 25 };
const mergedObj = { ...obj1, ...obj2 };  // Merge both objects
console.log(mergedObj);  // Output: { name: 'Alice', age: 25 }
```
 

2. Rest Operator (...)
The rest operator is used to collect multiple elements into a single array or object. It is commonly used in function parameters to gather remaining arguments, or to collect extra properties when destructuring.

Example in Function Parameters:
Collecting arguments into an array:
```
function sum(...numbers) {
  return numbers.reduce((acc, num) => acc + num, 0);
}

console.log(sum(1, 2, 3, 4));  // Output: 10
```
Here, ...numbers collects all arguments passed to the sum() function into an array. You can then work with those arguments inside the function.

Example with Destructuring:
Collecting the remaining items:
```
const arr = [1, 2, 3, 4, 5];
const [first, second, ...rest] = arr;  // `rest` collects the remaining elements
console.log(first);  // Output: 1
console.log(second); // Output: 2
console.log(rest);   // Output: [3, 4, 5]
```
In this case, the rest operator ...rest collects all the remaining elements of the array into the rest variable after destructuring the first two elements.

Example with Objects:
Rest operator in object destructuring:
```
const person = { name: "Alice", age: 25, country: "USA" };



const { name, ...rest } = person;  // `rest` collects remaining properties
console.log(name);  // Output: Alice
console.log(rest);  // Output: { age: 25, country: 'USA' }
```
Here, the rest operator ...rest collects all the remaining properties of the object person into the rest object.
 
