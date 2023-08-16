# Digital Clock

This project is made my me :)

index.html

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Digital Clock</title>
</head>
<body style="background-color: black;">
    <center>
    <h1 style="color: rgb(132, 12, 245);font-style: oblique;font-size: 60px;
    margin: auto;height: 40px;">Digital Clock</h1>
    <p id="clock" style="font-size: 50px;color: blue;font-style: oblique;border: 2px solid #c3c3c3;width: 340px;"></p>
    </center>
    <script src="index.js"></script>
</body>
</html>
```

index.js

```jsx
console.log("Digital Clock");
updateTime=()=>{
    setInterval(() => {
    let clock = document.getElementById('clock');
    let date = new Date();
    hour = date.getHours();
    minute = date.getMinutes();
    second = date.getSeconds();
    clock.innerHTML = `${hour}:${minute}:${second}`;
    // console.log(clock);
    },1000);
}
updateTime();
```