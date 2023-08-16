# Data Types Code

console.log("All about data types");

//Primitive Data Type

//String

let Name = "Sudip";

console.log("Data Type is " + (typeof Name));

//Number

let marks = 100;

console.log("Data Type is " + (typeof marks));

//null

let nullVal = null;

console.log("Data Type is " + (typeof nullVal));

//Undefined

let undef = undefined;

console.log("Data Type is " + (typeof undef));

//Reference Data Type

//Array

let numbers = [12,13,14,15];

console.log("Data Type is " + (typeof numbers));

//Object Literals

let StMarks = {

Sudip: 47,

Bhaskar: 50

}

console.log("Data Type is "+ (typeof StMarks));

//Function

function sum(a,b){

let c = a+b;

return c;

}

console.log("Data Type is " + (typeof sum));

//Date

let date = new Date;

console.log("Data Type is " + (typeof date));