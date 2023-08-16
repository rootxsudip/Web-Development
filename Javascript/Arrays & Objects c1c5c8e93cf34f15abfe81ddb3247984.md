# Arrays & Objects

The object class represents one of JavaScript’s data types. It is used to store various keyed collections and more complex entities. Objects can be created using the Object() constructor. we have two types of values used in JavaScript- primitive and reference. To be more simple, either we create objects or primitive data types. The primitive data types are as follows-

let myVar = 34;
              let myVar2 = "string";
              let myVar3 = true;
              let myVar4 = null;
              let myVar5 = undefined;

Apart from primitive data types, all the others are objects. Let us now see how to define objects. If we write as follows-

let employee = {
name: "Sudip",
salary: 10,
passion: "Hacking",
"Hobby 1": "Programming",

"Hobby 2": "Gym",
}
console.log(employee);

[Code](Arrays%20&%20Objects%20c1c5c8e93cf34f15abfe81ddb3247984/Code%203e0fb02987a0467c93d6765b5e8eeaef.md)

# Array Methods
There are many array methods some are below:

#### Filter method:
It's filter the array according to  our logical condition and return items which are satisfied with the condition .
```
let arr = [
    {name: "Cycle", price: 50},
    {name: "Bike", price: 150},
    {name: "Car", price: 500}
    ]
let filteredItems = arr.filter((item) => {
        return item.price > 100
})
console.log(filteredItems)
```
Output: [{ name: "Bike", price: 150 },{ name: "Car", price: 500 }]

#### Map method:
It creates a new array with the results of calling the provided function on each item on the array.
```
let sq = ((item)=>{
    return item*item
    })
let arr = [1,2,3,4,5]
arrSq = arr.map(sq)
console.log(arrSq)
```
Output:  [ 1, 4, 9, 16, 25 ]

#### Find method:
It creates a new array with the first one item of the result which returns true after calling the provided function on each item on the array.
```
let even = ((item)=>{
    return item%2==0
    })
let arr = [1,2,3,4,5]
arrEven = arr.find(even)
console.log(arrEven)
```
Output: 2

#### forEach method:
It executes a provided function once for each array element. 
```
let arr = [
    {name: "Cycle", price: 50},
    {name: "Bike", price: 150},
    {name: "Car", price: 500}
    ]
arr.forEach((item)=>{
    console.log(item.name)
})
```
Output: Cycle Bike Car

#### Some method:
It returns true if, in the array, it finds an element for which the provided function returns true; otherwise it returns false. It doesn't modify the array.
```
let arr = [
    {name: "Cycle", price: 50},
    {name: "Bike", price: 150},
    {name: "Car", price: 500}
    ]
let hasInexpensiveItems = arr.some((item)=>{
    return item.price >= 100
})
console.log(hasInexpensiveItems)
```
Output: true

#### Every method:
It returns true if, in the array, it finds all elements for which the provided function returns true; otherwise it returns false. It doesn't modify the array.
```
let arr = [
    {name: "Cycle", price: 50},
    {name: "Bike", price: 150},
    {name: "Car", price: 500}
    ]
let hasInexpensiveItems = arr.some((item)=>{
    return item.price <= 1000
})
console.log(hasInexpensiveItems)
```
Output: true

#### Reduce method:
It executes a user-supplied "reducer" callback function on each element of the array, in order, passing in the return value from the calculation on the preceding element. The final result of running the reducer across all elements of the array is a single value. 
```
let arr = [
    {name: "Cycle", price: 50},
    {name: "Bike", price: 150},
    {name: "Car", price: 500}
    ]
let total = arr.reduce((current_total,item)=>{
    return item.price + current_total
},0)
console.log(total)
```
Output: 700

#### Includes method:
It checks if the provided item is in the array or not.
```
let arr = [1,2,3,4,5]
let result = arr.includes(2)
console.log(result)
```
Output: true