# Code
```
<!DOCTYPE html>

<html lang="en">

<head>

<meta charset="UTF-8">

<meta http-equiv="X-UA-Compatible" content="IE=edge">

<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Loops</title>

</head>

<body>

<div class="container">

This is all about loops

</div>

<script>

console.log("Loops\n\n")

let os = ["Kali", "Parrot", "Black Arch", "Serenity"];

// for (let index = 0; index < os.length; index++) {

//     console.log(os[index]);

// }

//  os.forEach(function f(element){

//         console.log(element);

//     });

// for (element of os){

//     console.log(element);

// }

let person = {

name: "Sudip",

salary: 2,

hobby: "haxoring"

}

// Use this loop to iterate over objects in Javascript

for(key in person){

console.log(`The ${key} of the person is ${person[key]}`);

};

// While loop in js

let i = 0;

while(i<5){

console.log(`${i} is less than 5`);

i++;

}

// Do While loop in js

let j = 18;

do{

console.log(`${j} is greater than 4`);

j++;

}while(j<4);

</script>

</body>

</html>