# Error Handling & Try Catch

### Types of Errors:-

There can two types of errors:

- **Syntax Error**: This is the error in the syntax. For example, if we write console.log('JS');, the above program throws a syntax error. The spelling of the log is a mistake in the above code.
- **Runtime Error**: The runtime error occurs during the execution of the program. For example, calling an invalid function or a variable.

Now, let's see how we can handle these exceptions.

### What is Try Catch in JavaScript?

Just like other programming languages, JavaScript also has exception handling capabilities. JavaScript implements the try-catch statements as well as the throw operator to handle exceptions. Here is the basic syntax for try…catch:

```jsx
try{//some code that has an error
}
catch (e) {
//this will run if the code in the try block errors}
```

With these statements, in JavaScript, we can also add a throw or a finally clause. Let us see what role they play.

- **throw:** This is a block of code nested within the try statement and allows the programmer to write their own error that they want to handle.
- **finally:** This block of code runs once all the other statements have run.

### try/throw/catch:-

The throw operator generates an error. We can define and throw their own custom errors. When the throw statement is executed, the statements present after it does not execute. The control will directly pass to the catch block. In the following example, we create our own error ("This is a new error") in the throw block. Then try the code which throws an error that should be caught by the catch block.

```jsx
try{
  throw new Error ('This is a new error')
}
catch(error){
  console.log(error)
  console.log("End of try-catch block")
}
```

### try/catch/throw/finally:-

Finally is an optional block of statements that is executed after the execution of try and catch statements. It does not matter that any exception is thrown or not, finally block code will definitely execute if it is present. In this example, we will see how to use the finally statement with the other three statements. In this example, we do not show the entire error. We just logged that the error has been handled in the catch block.

```jsx
try{
  console.log("This statement works")
  throw new Error('This statement throws an error')
}
catch(error){
  console.log("Error has been handled")
}
finally{
  console.log("Everything has been handled")
}
```

```jsx
console.log("Error Handling and catch handling");

// Pretend this is coming from a server as response
let a = "Hackerman";
a = undefined;
if (a !=undefined){
    throw new Error('This is not undefined');
}
else{
    console.log('This is undefined');
}

try {
    null.console
    console.log("We are inside try block");
    
    functionHarry();
    
} catch(error) {
    console.log(error)
    console.log("Are you okay?");
    console.log(error.name);
    console.log(error.message);
    
} finally {
    console.log("Finally we will run this")
}
```