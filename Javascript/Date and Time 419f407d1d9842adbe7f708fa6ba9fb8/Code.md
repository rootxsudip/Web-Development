# Code
```
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta http-equiv="X-UA-Compatible" content="IE=edge">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Data and Time</title>
<style>
.container{
background-color: blanchedalmond ;
font-size: 23px;
padding: 34px;
margin: 4px;
text-align: center;
}

#time{
font-weight: bold;
}

</style>
</head>
<body>
<div class="container">
Current time is <span id="time"></span>
</div>
<script>
let now = new Date();
console.log(now);
let dt = new Date(1000);
console.log(dt);
// let newDate = new Date("2025-09-30");
// console.log(newDate);
// let newDate = new Date(year, month, date, hours, minutes, seconds, milliseconds);
let newDate = new Date(3020, 4, 6, 9, 3, 2, 34);
console.log(newDate);
let yr = newDate.getFullYear();
console.log("The year is ", yr);
let dat = newDate.getDate();
console.log("The date is ", dat);
let month = newDate.getMonth();
console.log("This year is ", month);
let hours = newDate.getHours();
console.log("This hours is ", hours);
newDate.setDate(8);
newDate.setMinutes(29);
console.log(newDate)
setInterval(updateTime, 1000);
function updateTime() {
time.innerHTML = new Date();
}

</script>

</body>

</html>