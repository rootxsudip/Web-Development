# Callback function

### What is a Callback?

*A callback is a function that is executed after another function has finished executing.* As we have studied earlier that functions are objects. Functions can take functions as arguments and can be returned by other functions. Functions that take another function as an argument are called higher-order functions*. So, the callback function can also be defined as any function that is passed as an argument is called a **callback function**.*

### Why do we need Callbacks?

As we know, instead of waiting for a response, JavaScript will keep executing while listening for other events. Here is an example:

```jsx
function fun1(){
   console.log(“Hackerman”);
 }
function fun2(){
   console.log(“JavaScript Tutorial”);
 }
fun1();
fun2();
```

The function fun1 is executed first, and the function fun2 is executed second. JavaScript runs code from top to bottom. However, there are some cases that code must run after something else happens and also not using a top-down approach.

Callbacks are used to make sure that a function is not going to execute before a task is completed but will execute right after the task has been completed. It helps us develop asynchronous JavaScript code and keeps us safe from future errors.

In JavaScript, the way to create a callback function is to pass it as a parameter to another function, and then to call it back right after something has happened or some task is completed.

### How to create a Callback:-

Suppose we want to log a message to the console but it should be there after 5 seconds.

```jsx
function myMessage (str) {
setTimeout(() => {
// script to download the picture here
console.log(`This message executed after 5 seconds`);
}, 5000);
}
```

There is a built-in method called **“setTimeout”**, which calls a function after a given period of time. So here, the myMessage function is being called after 5 seconds. **(1 second = 1000 milliseconds)**.
 In other words, the myMessage function is being called after something happened (after 5 seconds passed for this example), but not before. So, the myMessage function is an example of a callback function.

Here is an example of callback functions in JavaScript:

```jsx
function addition(x, y , callback){
setTimeout(() => {
document.write(`The sum of ${x} and ${y} is ${x+y}.`); 
callback(); 
 }, 5000); } 
 // display() function is called just after the ending of addition() function
function display(){ 
document.write('Numbers added!'); 
 } 
 // Calling addition() function
addition(5,5,display);
```

Here are the two functions – addition(x, y, callback) and display(). Here addition() is called after 5 seconds with the display() function, i.e. passed in as the third argument to the addition function along with two numbers x and y. As a result, the addition() is invoked with 1, 2, and the display() which is the callback. The addition() prints the addition of the two numbers(x+y), and as soon as that is done, the callback function is executed.

```jsx
The sum of 5 and 5 is 10.
Numbers added!
```

[index.html](Callback%20function%208f4198baba7a4b1486e62e3629c05daf/index%20html%20d826360cf0114b27acc9c3c242e3faa4.md)

[callback.js](Callback%20function%208f4198baba7a4b1486e62e3629c05daf/callback%20js%20875409c9af9f43ac98c9807ee59567fe.md)