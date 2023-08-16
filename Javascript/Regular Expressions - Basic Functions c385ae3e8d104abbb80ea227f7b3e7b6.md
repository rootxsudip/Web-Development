# Regular Expressions - Basic Functions

### What are Regular Expressions?

Regular expressions are the patterns that are used to match character combinations in strings. Regular expressions are a powerful way of doing search and replace in strings. It is a small language that is a part of many programming languages like JavaScript, Python, and Java. Regular expression allows us to check a string of characters like a password for patterns, to see if the set password matches with the pattern defined by that regular expression. In this tutorial, we will create a regular expression by using forward slashes ( / ) to enclose the pattern.

### Syntax:-

/*pattern*/*modifiers*;

```jsx
let str = /Hackerman/i;
```

Here /Hackerman/i is a regular expression. “Hackerman” is a pattern and “i” is a modifier that modifies the search to be case-insensitive. If we write /Hackerman/g, here “g” performs a global match that will find all matches rather than stopping after the first match.

### Regular Expressions Methods:-

**Regular expressions** are used with the RegExp methods like test() and exec() and with the 
string methods match() , replace() , search() , and split() . These methods are explained in detail below with examples.

### exec():-

This method will execute a search for a match in a string. It returns an array of information on match or null on a mismatch. Here is an example:

```jsx
let obj = /H/.exec("Hackerman");
```

### test():-

This method tests for a match in a string. It returns true or false. Here is an example:

```jsx
let str = /man/;
str.test("Hackerman");
```

### match():-

This method will return an array containing all of the matches, including capturing groups, or null if no match is found. Here is an example:

```jsx
  let str = "JavaScipt tutorial from begineer to advance level"; 
  let result = str.match(/ial/);
```

### search():-

This method will tests for a match in a string. It returns the index of the match, or -1 if the search fails. Here is an example:

```jsx
let str = 'Hackerman';
let reg = /hacker/i;
// search if the pattern is in string variable
let result = str.search(reg);
console.log(result);
```

### replace():-

This method will execute a search for a match in a string and replaces the matched substring with a replacement substring. Here is an example:

```jsx
let str = "Superman!";
let result = str.replace("Super", "Hacker");
```

### split():-

This method uses a regular expression or a fixed string to break a string into an array of substrings. Here is an example:

```jsx
const test = /[\s,]+/;
let result6 = 'I am learning JavaScript RegEx!'.split(test);
console.log(result6); // ["I", "am", "learning", "JavaScript", "RegEx!"]
```