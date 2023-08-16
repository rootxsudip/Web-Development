# Regular Expressions - Metacharacters

### Metacharacters in Regular Expressions:-

Metacharacters are the building blocks of regular expressions. Characters in Regular expression are understood to be either a metacharacter with a special meaning or a regular character with a 
literal meaning. Following are some common metacharacters in regular expressions.

[Metacharacters](Regular%20Expressions%20-%20Metacharacters%2041ff4331002e48769ade67df7d9c38c9/Metacharacters%2026913e48c0564a8f8733022734262f83.md)

- Do a global search for "m.d" in a string:

```jsx
let reg = /m.d/g;
let str = "He's mad!"; //matches
```

- Do a global search for at least one "e":

```jsx
let reg = /o+/g;
let str = "Codeeeee!";//matches
```

- Do a global search for a "5", followed by zero or more "0" characters:

```jsx
let reg = /50*/g;
let str = "5, 500 or 5000?"; //matches
```

- Do a global search for "javaScript" at the end of a string:

```jsx
let reg = /javaScript$/g;
let str = "Welcome to the tutorial of javaScript"; //matches
```

- Do a global search for "javaScript" at the beginning of a string:

```jsx
let reg = /^javaScript/g;
let str = "javaScript supports OOP";//matches
```

- Do a global search for "javaScript" at the beginning of a string:

```jsx
let reg = /^javaScript/g;
let str = "javaScript supports OOP";//matches
```

- Do a global search for "code" followed by " harry":

```jsx
let reg = /code(?= harry)/g;
let str = "code with harry"; //matches
```

- Do a global, case insensitive search for "code" not followed by "JavaScript":

```jsx
let reg = /code(?! JavaScript/gi;
let str = "Code JavaScript"; //does not match
```