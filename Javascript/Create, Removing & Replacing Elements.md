# Create, Removing & Replacing Elements

### **createElement():-**
The document.createElement() is a method used to create the HTML element. createElement(). Following is the syntax.
var element = document.createElement("name");
In the above syntax, the name is passed as a parameter. The name specifies the type of the created element. The document.createElement() returns the newly created element.
The following example uses the document.createElement() to create a new <div> element:
let div = document.createElement('div');
There is also another method, which is createTextNode().This method creates a Text Node with the specified text. Use the createElement() method to create an element Node with the specified name.After the Text Node is created, use the element.appendChild() method to append it to an element.
var paragraph = document.createElement("P");
var text = document.createTextNode("This is a paragraph.");

### **appendChild():-**
The appendChild() method is used to create a text node as the node's last child. Appending in JavaScript is a way to insert content to the end of already existing elements. To append in JavaScript, we use the appendChild() method.
**Syntax:**
node.appendChild(node)
**Here is an example:**
var paragraph = document.createElement("P");
var text = document.createTextNode("This is a paragraph.");
paragraph.appendChild(text);

### **Working with Attributes:-**
The attributes are the special words used inside the start tag of an HTML element.JavaScript provides us with several methods for adding, removing, or changing an HTML element's attribute. Following are some methods to set attributes in the HTML elements.

### **setAttribute():-**
The setAttribute() method is used to set an attribute on the specified element.Using this method, a new attribute is added with specified name and value. If the attribute already exists on the element, the value is updated.Here is an example: 
**Example:** 
document.getElementById("myAnchor").setAttribute("href", "https://codewithharry.com");

### **getAttribute():-**
The getAttribute() method is used to get the current value of a attribute on the specified element. If the attribute does not exist on the element, it will return null.Here is an example:
In this example, we will get the value of the target attribute of an <a> element:
var h = document.getElementById("myAnchor").getAttribute("target");

### **hasAttribute():-**
The hasAttribute() method is used to check an element has a specified attribute or not. The syntax is:
let result = element.hasAttribute(name);
In the argument, we specify the name of the attribute that we want to check.
This method returns a Boolean value that indicates if the element has the specified attribute. If the element contains an attribute, it will return true; otherwise, it will return false. Here is an example:
In this example, we find that if the <button> element has an onclick attribute:
var h = document.getElementById("Btn").hasAttribute("onclick");

### **removeAttribute():-**
The removeAttribute() method is used to remove an attribute from the specified element. The difference between this method and the removeAttributeNode() method removes the specified name.
The result will be the same. Also, this method has no return value, while the removeAttributeNode() method returns the removed attribute as an Attr object.

Remove the href attribute from an <a> element:
document.getElementById("myAnchor").removeAttribute("href");

### replaceWith():-
The replaceWith() method replaces this ChildNode in the children list of its parent with a set of Node. Here is an example:

Code:
let element1 = document.getElementById("myid1 ");
let element2 = document.createElement("u");
let content = document.createTextNode("Added Content");
element2.appendChild(content);
element1.replaceWith(element2);

We are getting the element using its id. Then we are creating a new element that creates underlined content and then we add content to the newly created element. In the next step, we are adding the content to element2. And finally we are replacing the old element, with the newly created element(old_elem.replaceWith(new_elem);).

### replaceChild():-
The replaceChild() method replaces a child node with a new node. We can create a new node, or The new node could be an existing node in the document or the new node could be an existing node in the document. In the following example, we will replace an existing node sp2 with the new span element sp1:

Code:
parentDiv.replaceChild(sp1, sp2);

### removeChild():-
This method removes a specified child node of the specified element. It will return the removed node as a Node object, or *null* if the node does not exist. Remember that the ****removed child node is no longer part of the DOM. In the following example, we will find out if a list has any child nodes. If so, remove its second child node.

Code:

let list = document.getElementById("myList");
if (list.hasChildNodes()) {
list.removeChild(list.childNodes[1]);
}