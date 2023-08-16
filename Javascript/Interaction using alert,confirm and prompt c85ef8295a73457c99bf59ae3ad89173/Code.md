# Code
```
<!DOCTYPE html>

<html lang="en">

<head>

<meta charset="UTF-8">

<meta http-equiv="X-UA-Compatible" content="IE=edge">

<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Interaction using alert,confirm and prompt</title>

</head>

<body>

<div class="container">This is a page</div>

<script>

// Alert in-browser does not return anything

// alert("This is a message")

// let name = prompt("What is your name?");

// console.log(name);

// Quick quiz

// let age = prompt("What is your age?");

// if (age>=18){

//     console.log("You are allowed inside the club");

// }

// else{

//     console.log("You are not allowed inside the club");

// }

// Confirm in JS

let deleteAcc = confirm("Do you really want to delete the account?");

if(deleteAcc){

// Code to delete the account

console.log("You account has been deleted");

}

else{

// Code to cancel deletion the account

console.log("You account has been not deleted");

}

</script>

</body>

</html>
```