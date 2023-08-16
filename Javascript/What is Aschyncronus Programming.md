# What is Aschyncronus Programming?

### What is the difference between synchronous and asynchronous programming?

In ***synchronous* programming**, one thing happens at a time. When we call a function that performs a long-running action, it returns a result when the action has finished. This stops the program for the time the action takes. In contrast, ***asynchronous* programming** allows multiple things to happen at the same time. When we start an action, the program continues to run. When the action finishes, the program is informed and gets the result.

Let's compare synchronous and asynchronous programming using an example: a program that fetches two resources from the network and then combines results.

In synchronous programming, where the request function returns only after it has done its work. To perform this task, we make the requests one after the other. Here the drawback is that the second request will be started only when the first has finished. Suppose the time taken by the first request is 12 seconds, and the time taken by the second request is 13 seconds, so the total time taken will be the sum of the two response times.

In asynchronous programming, the functions that perform a slow action take an extra argument, a *callback function*. The action is started, and when it finishes, the callback function is called with the result.

For example, the setTimeout function waits a given number of milliseconds (a second is a thousand milliseconds) and then calls a function.

```jsx
setTimeout(() => console.log("Tick"), 500);
```

Waiting is useful when doing something like updating an animation or checking whether something takes longer than a given amount of time.

Performing multiple asynchronous actions in a row using callbacks means that we have to keep passing new functions to handle the program's continuation after the actions.

### Summary:-

- Asynchronous code does not have to wait; the program can continue to run. The asynchronous programming makes it possible to express waiting for long-running actions without stopping the program during these actions. JavaScript usually implements this style of programming using callbacks.
- Asynchronous programming is made easier by using promises, objects that represent actions that might complete in the future, and async functions, which allow us to write an asynchronous program as if it were synchronous.

```js
console.log("Aschynchronus example");

setTimeout(() => {
    for(let index = 0; index < 4005; index++) {
        const element = index;
        console.log("This is index number" + index);
    }
}, 100);

console.log('done printing');
```