# Code
```
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta http-equiv="X-UA-Compatible" content="IE=edge">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Manipulating DOM</title>
</head>
<body>
<div id="main" class="container">
<ul id="nav">
<li>Home</li>
<li>About</li>
<li>Services</li>
<li>Contact Us</li>
</ul>
</div>
<div class="container">
<p>Another container</p>
</div>
<script>

let main = document.getElementById('main');
console.log(main);
let nav = document.getElementById('nav');
console.log(nav);
nav.innerHTML = "<li>Dynamic Element</li>"
let containers = document.getElementsByClassName('Container');
console.log(containers);
let sel = document.querySelectorAll('#nav>li');
console.log("Selector returns ", sel);

</script>

</body>

</html>