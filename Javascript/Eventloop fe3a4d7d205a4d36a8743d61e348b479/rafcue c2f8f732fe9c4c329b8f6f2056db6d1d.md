# rafcue

Rafcue updates just before the browser renders upon hardware specs.

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Raf Counter</title>
</head>
<body>
    <button id="btn">Start st counter</button>
    <button id="btn2">Start raf counter</button>
    <button id="btn3">Start both counter</button>
    <div>setTimeout Counter: <span id="st">0</span></div>
    <div>requestAnimationFrame Counter: <span id="raf">0</span></div>
    <script>
        function stCounter(i){
            st.innerText = i
            setTimeout(()=> stCounter(i+1),0)
        }
        function rafCounter(i){
            raf.innerText = i
            requestAnimationFrame(()=> rafCounter(i+1),0)
        }
        btn.addEventListener('click',()=>stCounter(0),false)
        btn2.addEventListener('click',()=>rafCounter(0),false)
        btn3.addEventListener('click',()=>{
            stCounter(0)
            rafCounter(0)
        },
            false)
    </script>
</body>
</html>
```