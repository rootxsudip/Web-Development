# Code

console.log("All about Strings");

let name01 = "Sudip";

let greet = "Good Morning"

// console.log(greet + ' ' + name01);

// console.log(`${greet} ${name01}`); //This is the use of template literal

//Methods

let html = "<h1>This is header</h1>"+

"<p>This is a paragraph</p>";

console.log(html);

console.log(html.length);

console.log(html.toLowerCase());

console.log(html.toUpperCase());

console.log(html.indexOf('<'));

console.log(html.lastIndexOf('<'));

console.log(html.charAt(1));

console.log(html.endsWith('abcdef'));

console.log(html.includes('<p>Another para</p>'));

console.log(html.substring(0,4));

console.log(html.slice(0,4));

console.log(html.split('>'));

console.log(html.replace('This', 'It'));

document.body.innerHTML = html;