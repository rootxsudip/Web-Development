# Code
index.html
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div id="my_box">
        <h3>Hello World</h3>
      </div>
      <button id="start">Start</button>
      <button id="stop">Stop</button>      
    <script src="script.js"></script>
</body>
</html>
```
script.js
```
let nIntervalId;
changeColor = () => {
    if(!nIntervalId){
        nIntervalId = setInterval(flashtext,1000)
    }
}
flashtext = ()=> {
    const box = document.body.querySelector('#my_box')
    box.className = box.className === "go" ? "stop" : "go";
}
stopTextColor = ()=>{
    clearInterval(nIntervalId)
    nIntervalId=null
}

document.getElementById('start').addEventListener('click',changeColor)
document.getElementById('stop').addEventListener('click',stopTextColor)
```
style.css
```
.go {
    color: green
}

.stop {
    color: red;
}
```