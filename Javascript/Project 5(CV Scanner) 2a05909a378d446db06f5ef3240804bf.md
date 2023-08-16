# Project 5(CV Scanner)

index.html

```jsx
<!doctype html>
<html lang="en">
  <head>
    <!-- Required meta tags -->
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">

    <!-- Bootstrap CSS -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.1.0/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-KyZXEAg3QhqLMpG8r+8fhAXLRk2vvoC2f3B09zVXn8CA5QIVfZOJ3BCsw2P0p/We" crossorigin="anonymous">

    <title>Cv Scanner</title>
  </head>
  <body>
      <div class="container">
        <div class="row">
            <div class="col-md-6 mx-auto text-center">
                <h1 class="my-3">Candidate Applicatios for Pentesting Job</h1>
                <div id="image"></div>
                <br>
                <div id="profile"></div>
                <br>
                <button class="btn btn-primary btn-block" id="next">Next</button>
            </div>
      </div>
    </div>
    <!-- Optional JavaScript; choose one of the two! -->

    <!-- Option 1: Bootstrap Bundle with Popper -->
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.1.0/dist/js/bootstrap.bundle.min.js" integrity="sha384-U1DAWAznBHeqEIlVSCgzq+c9gqGAJn5c/t99JyeKa9xxaYpSvHU5awsuZVVFIhvj" crossorigin="anonymous"></script>
    <script src="index.js"></script>

    <!-- Option 2: Separate Popper and Bootstrap JS -->
    <!--
    <script src="https://cdn.jsdelivr.net/npm/@popperjs/core@2.9.3/dist/umd/popper.min.js" integrity="sha384-eMNCOe7tC1doHpGoWe/6oMVemdAVTMs2xqW4mwXrXsW0L84Iytr2wi5v2QjrP/xp" crossorigin="anonymous"></script>
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.1.0/dist/js/bootstrap.min.js" integrity="sha384-cn7l7gDp0eyniUwwAZgrzD06kc/tftFf19TOAs2zVinnD/C7E91j9yyk5//jjpt/" crossorigin="anonymous"></script>
    -->
  </body>
</html>
```

index.js

```jsx
console.log("Cv Scanner");
// Data
const data = [
    {
        name: 'Akash Hamal',
        age: 20,
        city: 'Bihar',
        languages: 'Python and JS',
        Speciality: 'Web Pentesting',
        image: 'https://randomuser.me/api/portraits/men/5.jpg'
    },
    {
        name: 'Sid Joshi',
        age: 23,
        city: 'Delhi',
        languages: 'C, C++, Rust, Go, PHP and JS',
        Speciality: 'Web Pentesting,Source Code Review',
        image: 'https://randomuser.me/api/portraits/men/51.jpg'
    },
    {
        name: 'Sourav Das',
        age: 21,
        city: 'Kolkata',
        languages: 'Go, PHP and JS',
        Speciality: 'Web Pentesting',
        image: 'https://randomuser.me/api/portraits/men/4.jpg'
    },
    {
        name: 'Nirmal Thapa',
        age: 28,
        city: 'Kathmandu',
        languages: 'Go, Python, JS and PHP',
        Speciality: 'Web Pentesting',
        image: 'https://randomuser.me/api/portraits/men/52.jpg'
    },
    {
        name: 'Sunil Yadav',
        age: 24,
        city: 'Dehradun',
        languages: 'Python, Java and JS',
        Speciality: 'Pentesting',
        image: 'https://randomuser.me/api/portraits/men/53.jpg'
    }
]

// CV Iterator
cvIterator=(profiles)=>{
    let nextIndex = 0;
    return{
        next: ()=>{
            return nextIndex < profiles.length ?
            {value: profiles[nextIndex++], done: false} :
            {done: true}
        }
    };
}

const candidates = cvIterator(data);

// Button listen for next button
let button = document.getElementById("next");
button.addEventListener('click',nextCV);
function nextCV(){
    let currentCandidate = candidates.next().value;
    let image = document.getElementById("image")
    if(currentCandidate != undefined){
        image.innerHTML = `<img src='${currentCandidate.image}'>`
        profile.innerHTML = `<ul class="list-group">
        <li class="list-group-item">Name: ${currentCandidate.name}</li>
        <li class="list-group-item">${currentCandidate.age} years old</li>
        <li class="list-group-item">Lives in ${currentCandidate.city}</li>
        <li class="list-group-item">Primarily works on ${currentCandidate.language}</li>
        <li class="list-group-item">Speciality: ${currentCandidate.Speciality}</li>
      </ul>`
    }
    else{
        alert("No more candidates");
        window.location.reload();
    }
}
nextCV();
```