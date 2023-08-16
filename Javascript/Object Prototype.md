# Object Prototype

**Introduction to JavaScript prototype:-**

As we know that all objects in JavaScript are instances of Object. A typical object inherits properties from Object.prototype.The Object.prototype object has many built-in methods and properties such as toString(), valueOf(), etc.All objects see the object prototype object changes through prototype chaining unless the properties and methods subject to those changes are overridden further along the prototype chain. This is a very dangerous mechanism to override or extend object behavior.

JavaScript is a prototype-based language. Whenever we create a function using JavaScript, the JavaScript engine adds a prototype property inside a function. The prototype property is an object where we can attach methods and properties in a prototype object, which enables all the other objects to inherit these methods and properties.

one way to create an object is by using a function constructor.

function MyDetails(name, job, yearOfBirth){
this.name= name;
this.job= job;
this.yearOfBirth= yearOfBirth;
}
console.log(MyDetails.prototype)

Output:-

![Object%20Prototype%209be8348b3507484684ffb82b2ecaaafe/Untitled.png](Object%20Prototype%209be8348b3507484684ffb82b2ecaaafe/Untitled.png)

The prototype object includes many properties and methods. Here is an explanation of a few prototype object methods.

### Methods and Description:

- **hasOwnProperty():** It will return a boolean indicating whether an object contains the specified property as a direct property of that object and not inherited through the prototype chain.
- **isPrototypeOf():** It will return a boolean indicating whether the specified object is in the prototype chain of the object, this method is called upon.
- **propertyIsEnumerable():** It will return a boolean that indicates whether the specified property is enumerable or not.
- **toLocaleString():** It will return the string in the local format.
- **toString():** It will return the string.
- **valueOf() :**It will return the primitive value of the specified object.

### Use of Prototype:-

JavaScript is using the prototype object in two things. First, one is to find properties and methods of an object, and the other is to implement inheritance in JavaScript. Here is an example:

function Student() {
[this.name](http://this.name/) = 'Harsh';
this.gender = 'Male';
}
Student.prototype.sayHi = function(){
console.log("Hello World!");
};
let std = new Student();
std.toString();

In the above code, the JavaScript engine checks whether the toString() method is attached to std or not. If it does not find there, it uses std *proto*_ link, which points to the prototype object of Student function. If it still cannot find it there, then it goes up in the hierarchy and check the prototype object of Object function because all the objects are derived from Object in JavaScript, and look for the toString() method. Thus, it finds the toString() method in the prototype object of Object function and so we can call std.toString().
![[index.jpg]]