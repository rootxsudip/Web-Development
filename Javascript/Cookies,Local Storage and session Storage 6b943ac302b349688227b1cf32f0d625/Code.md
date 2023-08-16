# Code

console.log('All Local and Session Storage');

//Array in Local Storage

let impArray = ['lassun', 'adrak', 'pyaz'];

//Add a key value inside local storage

localStorage.setItem('Name', 'Sudip');

localStorage.setItem('Name2', 'Tanmoy');

localStorage.setItem('Sabzi', JSON.stringify(impArray)); //Stringify is used to store array

//Clears the entire local storage

// localStorage.clear();

//Clear a particular key-value pair

// localStorage.removeItem('Name')

//Retrive a item from the local storage

let name = localStorage.getItem('Name');

sabziNames = JSON.parse(localStorage.getItem('Sabzi'));

console.log(name);

console.log(sabziNames);

//Add a key value inside session storage

sessionStorage.setItem('SessionName', 'Sudip');

sessionStorage.setItem('SessionName2', 'Tanmoy');

sessionStorage.setItem('sessionSabzi', JSON.stringify(impArray));