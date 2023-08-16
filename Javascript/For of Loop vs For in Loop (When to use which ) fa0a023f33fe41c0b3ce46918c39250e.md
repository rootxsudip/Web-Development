# For.. of Loop vs For.. in Loop (When to use which?)

### for loop:-

It is the most basic loop in every programming language. The for loop syntax takes three parameters; a variable declaration, an expression that will evaluate before each iteration, and the expression to be evaluated at the end of each iteration. Here is the syntax of for loop:

```jsx
for (initialization; condition; final expression) {
    // code to be executed
}
```

For example, the for loop will console.log each item in an array.

```jsx
const myarray = ['abcd', 'efgh', 'i', 'eeb12'];
for (let i = 0; i < myarray.length; i++) {
console.log(array[i]);
} // Result: abcd,efgh,I,eeb12
```

### The for..in loop:-

**The for..in loop** is an iteration method for iterating over "enumerable" properties of an object. This loop applies to all objects that have these properties. Here enumerable means an array or object or strings. If we are using a for…in loop over an object, it will give us the value to each key in the object. Here is the syntax of the **for..in loop:**

```jsx
for (variable in enumerable) {
        // do stuff
}
```

Here is an example to loop through and console.log all the values in the object,

```jsx
const obj = {
        first: 134,
        second: 255,
        third: 367,
        fourth: 433
}
for (const key in obj) {
        console.log( obj[key] )
} // Result: 134, 255, 367, 433
```

For…in loops do not have any specific order for execution. If we want the guarantee order on an object. Then specify the index in the objects or put the keys in an array. As we know, a character in a string has an index. Therefore, similar to Arrays, the indexes are enumerable properties that happen to be integers. Here is an example of a for..in loop with strings:

`const str = 'Lets Code';
for (let index in str) {
console.log(str[index])
} //Result: L, e, t, s C, o, d, e`

### For…Of Loop:-

To iterate over objects like arrays and strings, we can use the for...of statement. This statement is a newer feature of ECMAScript 6. The **for..of** loop does not work with objects because they are not "iterable". This iteration method is a more reliable way of looping through an Array in sequence. In this example of a for...of loop, we will print each item in the array to the console.

```jsx
let students = [ "Mark", "Harry", "Joe" ];
// Print out each type of shark
for (let std of students) {
   console.log(std);
} //Result: Mark, Harry, Joe
```

### Comparison:-

In the following table, we are comparing for..in loop and for..of loop.

[Untitled](For%20of%20Loop%20vs%20For%20in%20Loop%20(When%20to%20use%20which%20)%20fa0a023f33fe41c0b3ce46918c39250e/Untitled%20Database%209faa1917c9ce40a3b77414a0d145fbf7.md)

### Which loop should we use? and When?

Each type of loop is useful in a different scenario:

- If indexes are needed while accessing an array of indexes-related logical stuff are there, the for loop is a good choice.
- If there is a need to access keys/properties regardless of the sequence, use *a for-in* loop.
- If there is a need to iterate through items of an iterable, then the *for-of* loop is the right choice.