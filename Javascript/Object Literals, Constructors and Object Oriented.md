# Object Literals, Constructors and Object Oriented

The basic idea of object-oriented programming is that objects are used to model real-world things that we want to represent inside our programs. We can also describe OOP as the OOP provides a simple way to access functionality that would otherwise be hard or impossible to make use of.

### What are objects?

Objects contain related code and data, representing information about the thing we are trying to model, and the functionality that we want it to have. Object data is stored neatly inside an object package, making it easy to structure and access.

JavaScript is a powerful programming language that supports Object-Oriented programming(OOP). In JavaScript, objects created using object literal are singletons. This means when we made a change in an object, it affects the object in the entire script. Whereas if an object is created using the constructor function, then the change will not affect the object throughout the script.

// constructor function
function MyCar(){};
// literal notation
var myCar = {};

**Objects created using object literal:-**

Since these are singletons, a change to an object affects the object's entire script. A change in one instance will affect all the instances of the object. Object literal is a comma-separated list of name value pairs inside the curly braces. The object literals encapsulate the data. This minimizes the use of global variables, which can cause problems when combining the code.

var myCar = {
make: 'Ford',
model: 'Mustang',
year: 2000
};

**Objects created using the constructor function:-**

The object that is defined with a **function constructor lets** us have multiple instances of that object. If the change is made to one instance, it will not affect other instances. As we know that the constructor is essentially a function that acts as a blueprint for creating objects. A convention for declaring constructors is always to capitalize its function name.

function MyCar (make,model,year){
this.make = make;
this.model= model;
this.year = year;
}

// creating objects
let car1 = new MyCar(“Ford”, “Mustang”, 2000);

### "new" keyword:-

To create a new object instance, we use the **"new"** keyword to create an object based on a constructor. Adding the "new" keyword is a crucial step when creating an object from a constructor. The new keyword creates a new empty object. It binds property or function, which is declared with this keyword to the new object.

[Code](Hacking%2054cdd1878c1940c3a585abeff2f3dc81/Pwn%20Web%20628ccafad89a438097d411029e11be72/Web%20Development%20b79dc89ef8b14ff1951974c9abd8f931/JavaScript%2020e84adae71b41f9a0ceaf0c93ff310a/Object%20Literals,%20Constructors%20and%20Object%20Oriented%200fcb85e66f6c4eb88472a159be7562e7/Code.md)