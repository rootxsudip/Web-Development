# Children, Parent & Traversing the dom

**DOM Nodes Diagram:**

![https://api.codewithharry.com/media/videoSeriesFiles/courseFiles/javascript-tutorials-in-hindi-15/base64.png](https://api.codewithharry.com/media/videoSeriesFiles/courseFiles/javascript-tutorials-in-hindi-15/base64.png)

We can traverse the DOM in three directions, downwards, upwards and sideways. Each type of traversal uses a different method.

## **Traversing Downwards:**

There are two methods to traverse downwards, the first one is querySelector and the second one is children.

**querySelector or querySelectorAll:-**

To traverse downwards from a specific element, we can use querySelector( ) or querySelectorAll( ). The querySelector() returns the first element within the document that matches the specified selector whereas the querySelectorAll() returns the NodeList representing a list of the document's elements that match the specified group of selectors.

Code:
```
<div class="add">
<h2 class="add__title">title</h2>
</div>
const component = document.querySelector('.add')
console.log(component)

Output:

<div class="add">..</div>
```

**children:-**
The property that lets you select direct descendants is called children. It selects elements that are immediately nested in another element. The children return a HTML Collection that updates when children's elements are changed.

Code:
const items= document.querySelector('.myclass')
const l_Items = items.children
console.log(l_Items)

Output:
![Children,%20Parent%20&%20Traversing%20the%20dom%20189ab9e4fcd649f596d3c35f945f4f2e/Untitled.png](Children,%20Parent%20&%20Traversing%20the%20dom%20189ab9e4fcd649f596d3c35f945f4f2e/Untitled.png)

To return the first and last child of a node, use the firstChild and lastChild property.The node can be of any node type, including text node, comment node, and element node.Similarly, firstElementChild and lastElementChild return the first and last child Element node, and the childNodes return a live NodeList of all child nodes of any node type of a specified node.

**Selecting a specific child:-**

While traversing the DOM, we can select the nth-item in the list from both NodeLists and HTML Collections. For this, we use the index of the element. Similarly, we do in the case of the array to select a specific element.

Code:

const mylist = document.querySelectorAll('li')
const firstItem = mylist[0]
const secondItem = mylist[1]
console.log(firstItem)
console.log(secondItem)

Output:

![Children,%20Parent%20&%20Traversing%20the%20dom%20189ab9e4fcd649f596d3c35f945f4f2e/Untitled%201.png](Children,%20Parent%20&%20Traversing%20the%20dom%20189ab9e4fcd649f596d3c35f945f4f2e/Untitled%201.png)

## **Traversing upwards:-**
There is one method to traverse upwards: parentElement

**parentElement:-**
The property that let us select the parent element is known as parentElement.The parentElement returns *null* if the parent node is not an element node. Following is the example

Code:
const mylist = document.querySelectorAll('li')
const firstItem = mylist[0]
const secondItem = mylist[1]
console.log(firstItem.parentElement)
console.log(secondItem.parentElement)

Output:
![Children,%20Parent%20&%20Traversing%20the%20dom%20189ab9e4fcd649f596d3c35f945f4f2e/Untitled%202.png](Children,%20Parent%20&%20Traversing%20the%20dom%20189ab9e4fcd649f596d3c35f945f4f2e/Untitled%202.png)

## Traversing sideways:-
There are two methods to traverse sideways. One of them is nextElementSibling, and the other one is previousElementSibling.

**nextElementSibling:-**
To select the next element, we use the nextElementSibling.The difference between this property and nextSibling is that nextSibling returns the next sibling node as an element node, a text node, or a comment node, while nextElementSibling returns the next sibling node as an element node and ignores the text and comment nodes.

Code:
const item1 = document.querySelector('li')
const item2 = item1.nextElementSibling
console.log(item2)

![Children,%20Parent%20&%20Traversing%20the%20dom%20189ab9e4fcd649f596d3c35f945f4f2e/Untitled%203.png](Children,%20Parent%20&%20Traversing%20the%20dom%20189ab9e4fcd649f596d3c35f945f4f2e/Untitled%203.png)

### **previousElementSibling:-**
To select the previous element, we use previousElementSibling. The difference between this property and previousSibling, is that previousSibling returns the previous sibling node as an element node, a text node, or a comment node, while previousElementSibling returns the previous sibling node as an element node and ignores the text and comment nodes.

**Code:**

const item5 = document.querySelectorAll('li')[1]
const item6 = item5.previousElementSibling
console.log(item6)

**Output:**

![Children,%20Parent%20&%20Traversing%20the%20dom%20189ab9e4fcd649f596d3c35f945f4f2e/Untitled%204.png](Children,%20Parent%20&%20Traversing%20the%20dom%20189ab9e4fcd649f596d3c35f945f4f2e/Untitled%204.png)

### **Node Type:-**

The **nodeType** property is an integer that identifies what the node is. It differentiates different kinds of nodes from each other, such as elements, text, and comments. The syntax is:

var type = node.nodeType;

[Untitled](Children,%20Parent%20&%20Traversing%20the%20dom%20189ab9e4fcd649f596d3c35f945f4f2e/Untitled%20Database%208b0ba86b9a584a6a95f48065a2efb50b.md)

[Code](Hacking%2054cdd1878c1940c3a585abeff2f3dc81/Pwn%20Web%20628ccafad89a438097d411029e11be72/Web%20Development%20b79dc89ef8b14ff1951974c9abd8f931/JavaScript%2020e84adae71b41f9a0ceaf0c93ff310a/Children,%20Parent%20&%20Traversing%20the%20dom%20189ab9e4fcd649f596d3c35f945f4f2e/Code.md)