# Promises Basics, Promise.then() & Promise.catch()

### What is a Promise?

A promise in JavaScript is similar to promises we do in real life. When we make a promise, it is a guarantee that in future, we are going to do something. A promise has two possible outcomes: it will be kept when the time comes, or it will not. Similarly, in JavaScript, when we define a promise, either it will be resolved when the time comes, or it will get rejected. According to [MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise), “the Promise object represents the eventual completion (or failure) of an asynchronous operation and its resulting value.”

A promise has three states:

- **pending**: It is the initial state.
- **Fulfilled**: It indicates that the promised operation was successful.
- **Rejected**: It indicates that the promised operation was unsuccessful.

![Untitled](Promises%20Basics,%20Promise%20then()%20&%20Promise%20catch()%208907b48339de4a7fb92356d7c98091fa/Untitled.png)

The constructor syntax for a promise object is:

```js
let myPromise = new Promise(function(resolve, reject) {
// code here
});
```

When a new Promise is created, the function passed into it runs automatically. It contains the producing code which produces the result. Its arguments resolve and reject. Here is an example of a simple promise.

```js
var promise = new Promise(function(resolve, reject) { 
  const x = "geeksforgeeks"; 
  const y = "geeksforgeeks";
  if(x === y) { 
    resolve(); 
  } else { 
    reject(); 
  } }); 
promise.then(function(){ 
console.log('Success, You are a GEEK');}).catch(function () { 
console.log('Some error has occurred');});
```

- A promise is created using a constructor that takes a call back function with two arguments resolve and reject in line 1. If the task is successful(x===y), the promise is resolved. If the task is unsuccessful(x is not equal to y), then the promise is rejected. The then() method is called if the promise is resolved, and the catch() method is called when the promise is rejected or if an error occurred during the code execution.
- Promises are the ideal choice for asynchronous programming. Promises can handle multiple asynchronous operations easily and are better at error handling as compared to callbacks and events.

### Benefits of Promises:-

1. It improves the code readability.
2. It is better in the handling of asynchronous operations.
3. It has a better flow of control definition in asynchronous logic.
4. It is better in error handling.

Another Example:

```js
// Promise: Best video on promises
// -resolve
// -reject
// -pending

function func1() {
    return new Promise(function (resolve, reject) {
        setTimeout(() => {
            const error = true;
            if (!error) {
                console.log('Function: Your promise has been resolved')
                resolve();
            }
            else {
                console.log('Function: Your promise has not been resolved')
                reject('Sorry not fulfilled');
            }
        }, 2000);
    })
}

func1().then(function(){
    console.log("Harry: Thanks for resolving")
}).catch(function(error){
    console.log("Harry: Very bad bro. Reason: " + error)
})
```

Another example
```js
loadscript = (src) =>{
    return new Promise(function (resolve,reject){
        let script = document.createElement('script')
        script.src = src
        script.onload = () => resolve(script)
        script.onerror = () => reject(new Error(`Script loaded error for ${src}`))
        document.head.append(script)
    })
}

let promise = loadscript("https://cdnjs.cloudflare.com/ajax/libs/lodash.js/4.17.11/lodash.js")

promise.then(
    script => alert(`${script.src} is loaded`),
    error => alert(`Error: ${error.message}`)
)
```