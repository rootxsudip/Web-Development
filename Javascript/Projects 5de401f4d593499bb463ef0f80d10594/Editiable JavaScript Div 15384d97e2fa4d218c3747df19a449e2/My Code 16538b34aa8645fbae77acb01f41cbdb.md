# My Code

console.log('Editable Heading in Div');

document.write('<div><h1 class=heading2>Editable Text</h1></div>');

document.querySelector('.heading2').addEventListener('click', function(c){

let inp = prompt('Enter you heading');

document.querySelector('.heading2').innerHTML = inp;

})