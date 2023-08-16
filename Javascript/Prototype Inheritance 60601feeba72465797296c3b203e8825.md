# Prototype Inheritance

JavaScript object properties and methods can be shared through generalized objects that can be cloned and extended. This sharing is known as prototypical inheritance.

Every object in JavaScript has an internal property called prototype. Here is an empty object i.e., let a = {}. In this way, we normally create an object but note that another way to accomplish this is with the object constructor: let a = new Object()

### Inheritance:-

Inheritance lets the objects share each other's properties. In other words, Inheritance is the process by which one object can be based on another.

### Prototype Inheritance:

When we try to access a property or any object's method, the JavaScript will first search on the object itself, and then it will search the object's prototype if not found. If, after checking both the object and its prototype still no match is found, JavaScript will check the linked object prototype and continue searching until the end of the prototype chain is reached. Object Prototype is at the end of the prototype chain. All the objects inherit the properties and methods of Object. When we try to search beyond the end of the chain, results in null. There are different ways to create an object in JavaScript.

- Object literal
- Function constructor
- The create() method

### Object.create():-

The **Object.create()** method using an existing object as the prototype, creates a new object. The syntax is:

Object.create(proto, [propertiesObject])

Example:-

```js
const myDetail= {
isHuman: true,
printIntro: function() {
console.log(My name is ${this.name}. Am I human? ${this.isHuman});
}};
const myself = Object.create(myDetail);
myself.name = 'Harry'; // "name" is a property set on "me", but not on "person"
myself.printIntro();
// expected output: "My name is Harry. Am I human? true"
```

To create inheritance between function constructors, call the parent constructor using call or link the prototype of the child constructor to the parent constructor prototype.

### Using call to chain constructors for an object:-

The call() allows the method or function belonging to one object to be assigned and called for another object. This method provides a new value of this to the method or function. With call(), we can write a method once and then inherit it in another object without rewriting the new object's method.

For example, the constructor for the Factory object is defined with two parameters: name and location. Other functions, Food, invoke Factory, passing this, name, and location. Factory initializes the property's name and location; the specialized functions define the category.

```js
function Factory (name, location) {
this.name = name;
this.location = location;
}
function Food(name, location) {
Factory.call(this, name, location);
this.category = 'food';
}
const myFood = new Food('Nestle', 'UK' );
```

### Manually set the constructor:-

The **constructor** property is used to return a reference to the object constructor function that created the instance object. We mostly use this property to define a **function-constructor** function by calling it with **a new** and **prototype-inherits chain**. Here is a simple example of how to set the constructor manually:

```js
function Factory() {
/* ... */
}
Factory.prototype.FactoryMethod = function FactoryMethod() {}
function Product1() {
Factory.call(this)
}
Product1.prototype.constructor = Product1
```

[Practice Code](Hacking%2054cdd1878c1940c3a585abeff2f3dc81/Pwn%20Web%20628ccafad89a438097d411029e11be72/Web%20Development%20b79dc89ef8b14ff1951974c9abd8f931/JavaScript%2020e84adae71b41f9a0ceaf0c93ff310a/Prototype%20Inheritance%2060601feeba72465797296c3b203e8825/Practice%20Code.md)