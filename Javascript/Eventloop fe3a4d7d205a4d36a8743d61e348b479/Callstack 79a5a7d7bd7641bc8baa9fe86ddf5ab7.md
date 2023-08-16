# Callstack

### What is callstack?

→ A callstack is a interpreter mechanism to store function calls, track it,execute it correctly and remove the calls from the last to first call execution from the stack.

- If the stack more space that it had assigned to it, it results in a stack overflow error.

```jsx
function greeting() {
   sayHi(); //add this as 2nd in callstack list
}
function sayHi() {
   return "Hi!";
}
// Invoke the `greeting` function
greeting(); //add this as 1st in callstack list

```

The above code will run then store the greeting() function in the call stack list → execute it →

sayHi() function will added to the callstack list → execute it line by line → call stack list become

full → It removes sayHi() function[2] and then removes sayHi() function(1) → call stack list cleared

In summary, then, we start with an empty Call Stack. Whenever we invoke a function, it is automatically added to the Call Stack. Once the function has executed all of its code, it is automatically removed from the Call Stack. Ultimately, the Stack is empty again.

Reference:

[https://developer.mozilla.org/en-US/docs/Glossary/Call_stack](https://developer.mozilla.org/en-US/docs/Glossary/Call_stack)