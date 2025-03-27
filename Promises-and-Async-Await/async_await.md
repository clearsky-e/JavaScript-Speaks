---- async and await ----

The async await is the more cleaner and simple way to write and handel the async code, before this we used callback
then we have this Promise and now we have async and awai

- async: it is used to define a function that always return a Promise. Inside this function we can use the await only
- await: it is used to wait the program for the async functin for the reject or the resole

  example without async await
```
function fetchData() {
  return new Promise((resolve, reject) => {
    setTimeout(() => {
      resolve("Data fetched");
    }, 2000);
  });
}

fetchData().then((data) => {
  console.log(data); // "Data fetched"
});

```


example with the async await
```
async function returnData(){
return new Promise((resolve,reject)=>{
setTimeout(()=>{
console.log("data returne");
},2000)
})

async function getData(){
console.log("this is the starting");
const myData = await returnData();
console.log("hey there this is the end");
}

getData();

```

the async and await is very straight forward and easy
here the await always should be used inside the async function and inside the async function if we have the await then it means the execution of
the program will stop there for the specific function only, and execute the other things which are outside of the program, and the moment 
the await got the data back or the error whatever it will complete the program.
