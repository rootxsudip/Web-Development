# Code

console.log('HTML Selectors');

/*

element selectors:

1. Single element selector

2. Multi-element selector

- /

// 1. Single element selector

let element = document.getElementById('myfirst');

// element = element.className;

// element = element.childNodes;

// element = element.parentNode;

element.style.color = 'purple';

element.innerText = 'Sudip is a good boy'

element.innerHTML = '<b>Sudip is a good boy</b>'

console.log(element.innerText);

let sel = document.querySelector('#myfirst');

sel = document.querySelector('.child');

sel = document.querySelector('div');

sel.style.color = 'green';

console.log(sel);

// 2. Multi element selector

let elems = document.getElementsByClassName('child');

elems = document.getElementsByClassName('container')

elems = document.getElementsByTagName('div')

console.log(elems);

for(let i in elems){

const element = elems[i];

console.log(element);

element.style.color = 'red';

}

// console.log(elems[0].getElementsByClassName('child'));