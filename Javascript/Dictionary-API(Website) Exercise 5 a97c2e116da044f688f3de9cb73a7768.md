# Dictionary-API(Website) Exercise 5

- You have to pretend to use a word API that will contain an object and you have to print the definition from all the results of that word api.
- You have to take input from an input tag.
- You have to print it in the dom.
- If you are using bootstrap then it's a plus.

### So I make a website that takes a word from the user and shows its definition.

```html
<!doctype html>
<html lang="en">
  <head>
    <!-- Required meta tags -->
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">

    <!-- Bootstrap CSS -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.1.0/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-KyZXEAg3QhqLMpG8r+8fhAXLRk2vvoC2f3B09zVXn8CA5QIVfZOJ3BCsw2P0p/We" crossorigin="anonymous">

    <title>Dictionary</title>
  </head>
  <body>
    <h1>Get Defination of your word</h1>
    <form>
        <div>
            <label for="word">Word:</label>
            <input type="text" id="word" name="word"><br><br>
        </div>
        <button type="submit" class="btn btn-primary" id="fetchBtn">Search</button>
    </form>
    <h2><u>Word defination</u></h2>
    <div id="definition"></div>
    <!-- Optional JavaScript; choose one of the two! -->

    <!-- Option 1: Bootstrap Bundle with Popper -->
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.1.0/dist/js/bootstrap.bundle.min.js" integrity="sha384-U1DAWAznBHeqEIlVSCgzq+c9gqGAJn5c/t99JyeKa9xxaYpSvHU5awsuZVVFIhvj" crossorigin="anonymous"></script>

    <!-- Option 2: Separate Popper and Bootstrap JS -->
    <!--
    <script src="https://cdn.jsdelivr.net/npm/@popperjs/core@2.9.3/dist/umd/popper.min.js" integrity="sha384-eMNCOe7tC1doHpGoWe/6oMVemdAVTMs2xqW4mwXrXsW0L84Iytr2wi5v2QjrP/xp" crossorigin="anonymous"></script>
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.1.0/dist/js/bootstrap.min.js" integrity="sha384-cn7l7gDp0eyniUwwAZgrzD06kc/tftFf19TOAs2zVinnD/C7E91j9yyk5//jjpt/" crossorigin="anonymous"></script>
    -->
    <script src="api.js"></script>
  </body>
</html>
```

```jsx
console.log("Word-Api is working");
let word = document.getElementById('word')
let popBtn = document.getElementById('fetchBtn');
fetchBtn.addEventListener('click',fetchDetails);
function fetchDetails(e){
    console.log("Button is working properly");

    // Get the data from server and show it in the console

// Instantiate an xhr request
const xhr = new XMLHttpRequest();

let str = word.value;
// Opent the object
xhr.open('GET','https://api.dictionaryapi.dev/api/v2/entries/en/' + str,true);
// xhr.getResponseHeader('Conten-type','application/json');

// // What to do on progress
xhr.onprogress = function(){
    console.log('On progress');
}

// Do this shit after geting response from the server
xhr.onload = function(){
    if(this.status === 200){
        // console.log(this.responseText);
        let wordObj = JSON.parse(this.responseText);
        let definition = document.getElementById('definition');
        console.log(wordObj);
        html = ``;
        for(key in wordObj){
            // console.log(wordObj[key]);
            meanings = wordObj[key]
            for(key in meanings){
                // console.log(meanings[key]);
                meaning = meanings[key];
                for(key in meaning){
                    // console.log(meaning[key]);
                    WordDefinitions = meaning[key];
                    for(key in WordDefinitions){
                        // console.log(WordDefinitions[key]);
                        Worddefinition = WordDefinitions[key];
                        for(key in Worddefinition){
                            html = Worddefinition[key].definition;
                            definition.innerHTML = html;
                        }
                    }
                }
            }
        }

    }
    else{
        console.log("Word is not found");
    }
}

// Send the xhr request
xhr.send();

e.preventDefault();
}
```