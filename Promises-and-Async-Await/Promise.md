---- Promise ----
Before Promises, JavaScript developers often used callbacks to handle asynchronous tasks.
However, callbacks can lead to "callback hell," which makes your code harder to read and maintain.(you sould know why we use the callback)
Ultimate Goal of Promises:
    - Avoid Callback Hell
    - Write More Readable Code

the promise is also created with the new keyword like this ``` let myPromise = new Promise((resolve, reject)=>...))``` 
and takes two arguments resolve and reject
the Promise could be of these state
Pending: means nothing happen, neither resolved nor reect
Resolve: means the Promise is resolve 
Reject: means the Promise is rejected

these Resolve and reject are the function we define while creating the Promsie and then later we will handle the Promise via using the .then or .catch

```
    let task = new Promise((resolve, reject)=>{
        let success = true; // here it could be like anything data coming from the api or anything else
        setTimeout(()=>{
            if(success){
                resolve("Task is Done");  //define the resolve
            }else{
                reject("Task is rejected");  //define the reject
            }
        },2000);
    })

    task.then((message)=>{
        console.log(message); //Task is Done
    }).catch((error)=>{
        console.log(error);
    })

```


we can handel and use Promises different types



-Promise Chaining
It means nesting the promise within another 
```
let task1 = new Promise((resolve, reject) => {
        let success = true;
        setTimeout(() => {
          if (success) {
            resolve("Task1 is Done");
          } else {
            reject("Task1 is rejected");
          }
        }, 2000);
      });

      task1
        .then((message) => {
          console.log(message); // Task1 is Done, after 2 seconds
          let task2 = new Promise((resolve, reject) => {
            setTimeout(() => {
              let success = false;
              if (success) {
                resolve("Task 2 is done");
              } else {
                reject("Task 2 is Undone");
              }
            }, 2000);
          });

          task2
            .then((message) => {
              console.log(message);
            })
            .catch((error) => {
              console.log(error); //Task2 is Undone, after 2 seconds of task1
            });
        })
        .catch((error) => {
          console.log(error);
        });


```




- Handel all the Promise together
It waits for all the Promise to be done and then show the end result in the end together, but if anyof them is reject and goes to the catch then
it will not print all instead it will show the error message only of that task
```

let task1 = new Promise((resolve, reject) => {
        setTimeout(() => {
          let success = true;
          if (success) {
            resolve("task1 done");
          } else {
            reject("task1 rejected");
          }
        },2000);
      });

      let task2 = new Promise((resolve, reject) => {
        setTimeout(() => {
          let success = true;
          if (success) {
            resolve("task2 done");
          } else {
            reject("task2 rejected");
          }
        }, 3000);
      });

      let task3 = new Promise((resolve, reject) => {
        setTimeout(() => {
          let success = true;
          if (success) {
            resolve("task3 done");
          } else {
            reject("task3 rejected");
          }
        },4000);
      });

      Promise.all([task1, task2, task3])
        .then(function (result) {
          console.log(result); // (3) ['task1 done', 'task2 done', 'task3 done'], after the 4 seconds since till here all the task will be done
        })
        .catch(function (error) {
          console.log(error);
        });


```


- Promise race
this is used when we have more than one Promise, and we just have to check which one is the fist task that is either done or not ,
we just want to find the fiorst, then we se this

```


 let task1 = new Promise((resolve, reject) => {
        setTimeout(() => {
          let success = true;
          if (success) {
            resolve("task1 done");
          } else {
            reject("task1 rejected");
          }
        },2000);
      });

      let task2 = new Promise((resolve, reject) => {
        setTimeout(() => {
          let success = true;
          if (success) {
            resolve("task2 done");
          } else {
            reject("task2 rejected");
          }
        }, 3000);
      });

      let task3 = new Promise((resolve, reject) => {
        setTimeout(() => {
          let success = true;
          if (success) {
            resolve("task3 done");
          } else {
            reject("task3 rejected");
          }
        },500);
      });

      Promise.race([task1, task2, task3])
        .then(function (result) {
          console.log(result);  // task3 done, since it will be done before everyone else since it have done in the 500 miliseconds
        })
        .catch(function (error) {
          console.log(error);
        });




```



