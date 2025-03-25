1. SetTimeout
   It is used to delay the function and then runs it only for once. It takes the time in the miliseconds, it will runs the function automatically
```
setTimeout(() =>{
            console.log('hello there');
            
},2000)
```
Sometimes a condition also could get occur in which we might want to stop the setTimeout before it runs the function, so for that reason we use the clearTimeout
the setTimeout return the timeout id, with this we can stop the setTimeout
```
        const timeId = setTimeout(() =>{
            console.log('hello there');
            
        },3000)
        clearTimeout(timeId)

```



2. setInterval
   It is used to perform a function repeatedly after a specific time
```
setInterval(function() {
  console.log("Hello!");
}, 2000); // 2000ms = 2 seconds

```

to stop this, we can use the id it returns
```
let intervalId = setInterval(function() {
  console.log("This keeps running every 2 seconds!");
}, 2000);

// Stop it after 5 seconds
setTimeout(function() {
  clearInterval(intervalId); // This stops the interval
  console.log("Interval stopped!");
}, 5000); // After 5 seconds


```
