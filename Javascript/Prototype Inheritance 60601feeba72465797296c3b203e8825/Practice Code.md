# Practice Code
```js
const proto = {
slogan: function () {
return `This company is the best`;
},
changeName: function (newName) {
this.name = newName
}
}
```

```js
// This creates harry object
let harry = Object.create(proto);
harry.name = "harry";
harry.role = "Programmer";
// harry.changeName("Harry2")
// console.log(harry)
```

```js
// This also creates harry object
const harry1 = Object.create(proto, {
name: { value: "harry", writable: true },
role: { value: "Programmer" },
});
harry1.changeName("Harry2")
// console.log(harry1)
```

```js
// Employee constructor
function Employee(name, salary, experience) {
this.name = name;
this.salary = salary;
this.experience = experience;
}
```

```js
// Slogan
Employee.prototype.slogan = function () {
return `This company is the best. Regards, ${this.name}`;
}
```

```js
// Create an object from this constructor now
let harryObj = new Employee("Harry", 345099, 87);
console.log(harryObj.slogan())
```

```js
// Programmer
function Programmer(name, salary, experience, language) {
Employee.call(this, name, salary, experience);
this.language = language;
}
```

```js
// Inherit the prototype
Programmer.prototype = Object.create(Employee.prototype);
```

```js
// Manually set the constructor
Programmer.prototype.constructor = Programmer;
```

```js
let rohan = new Programmer("Rohan", 2, 0, "Javascript");
console.log(rohan);
```