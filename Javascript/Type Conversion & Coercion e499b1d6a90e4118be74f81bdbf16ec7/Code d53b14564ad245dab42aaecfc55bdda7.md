# Code

//Type Conversion

//Number to String

let num1 = String(1337);

let num2 = (18).toString();

let num3 = (20.4589).toFixed();

let num4 = parseFloat(34.0878);

// let num4 = 34.0878;

console.log(num1 + ' is', typeof(num1));

console.log(num2 + ' is', typeof(num2));

console.log(num3 + ' is', typeof(num3));

console.log(num4 + ' is', typeof(num4));

//Boolean to String and number

let bool1 = true;

let bool2 = String(true);

let bool3 = (true).toString();

let bool4 = Number(true);

console.log(bool1 + ' is', typeof(bool1));

console.log(bool2 + ' is', typeof(bool1));

console.log(bool3 + ' is', typeof(bool3));

console.log(bool4 + ' is', typeof(bool4));

//Array to String and number

let arr1 = [1,2,3,4,5];

let arr2 = String([1,2,3,4,5]);

let arr3 = ([1,2,3,4,5]).toString();

let arr4 = Number([1,2,3,4,5]);

console.log(arr1 + ' is', typeof(arr1));

console.log(arr2 + ' is', typeof(arr2));

console.log(arr3 + ' is', typeof(arr3));

console.log(arr4 + ' is', typeof(arr4));

//Type Coercion

let num01 = "1337";

let num02 = 1337;

console.log(num01 + num02);