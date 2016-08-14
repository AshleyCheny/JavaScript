# JavaScript
* Browser: Chrome/Firefox
* Text Editor: Sublime Text2/Brackets

## 1. Lynda.com - [JavaScript Essential Training](https://www.lynda.com/MyPlaylist/Watch/6752886/87513?autoplay=true)

### 1). Introduction of JavaScript
* How does JavaScript work with HTML and CSS?
```go
Client-Side programming Language
Only works in a Web Browser
Can not access to database
```
### 2). Core JavaScript Syntax
* JavaScript is CASE SENSITIVE
* JavaScript comment: two formard slashes// multi lines/*   */
* When the JavaScript run? in the head/body-inline JavaScript

### 3). Types and Objects
* Variables are containers(e.g.,var year;) no need to specify the variable types
* `Array` in JavaScript is dynamic.
* JavaScript `numbers` are 64-bit floating point numbers.
* Not a Number(NaN), isNaN()
* `string` methods: split(),indexOf(), slice(), substring(), substr().../string comparison(case sensitive)
* `date` object month/week/hour is zero-based, date comparison
* * An `object` has properties and methods. Check the properties and methods for objects  througth Reference.
* create a method for an object
```javascript
//create two objects
var player1 = { name: "Fred", score: 100000, rank:1 };
var player2 = { name: "Ashley", score: 203030, rank:1 };

function playerDetails(){
//display infomation about each player
console.log(this.name + " has a rank of " + this.rank + " and a score of " + this.score);
}

//assig method
player1.logDetails = playerDetails;
player2.logDetails = playerDetails;

//call logDetails method
player1.logDetails();
player2.logDetails();

```
### 4). `DOM`(Document Object Model)
```go
What is the document? --> web page
What are the objects? --> things, pieces
What is the model? --> tree structure, a standard we can use
so, DOM is not a language, it is an idea, an convention
it is an agreed-upon terminology that will let us describe and interact with any web page.
```
```go
What we can do with DOM?
Get the title text
Get the second paragraph
Get the third link in the menu and set its CSS to display:none
Change the background color of all paragraphs with a class of "important"
Get all the <li> elements in the last unordered list
Find the image with an id of "logo" and move it 40 pixels to the right
Change a link so it performs a JavaScript function when clicked
Create a new unordered list and insert between first and second paragraphs
```
```go
DOM is a way to reach into the page from the script and the way the page can reach into the script 
A TREE STRUCTURE OF A WEB PAGE
HTML(Elements/Attributes/Text) --> DOM(tree structure + methods) --> JavaScript
```
```html
<!--`tree structure of a web page`: tree `nodes`-->
<!--Elment, Attribute and Text nodes-->
<ul id="optionList">
  <li>This is the first option</li>
  <li>This is the second</li>
  <li>This is the third</li>
</ul>
```
```javascript
//access DOM elements
var myElement = document.getElementById("someId");//myElment is a HANDLE right into the document. can use it to reach the element's parent or child elements.
document.getElementByTagName("li");//return an array
```
```javascript
//change DOM elements
//change or add an attribute, add new elemnts inside a div or inside a list?
myElement.getAttribute("align");
myElement.setAttribute("align","left");
myElemnt.innerHTML;//An element text content or a bunch of codes inside an element.
```
```javascript
//Creating DOM elements
var myNewElement = document.createElement("li");//create nodes first
myElement.appendChild(myNewElement);//append the node to its parent's node
var myText = document.createTextNode("New list item text"); //same here, create node first
myNewElement.appendChild(myText);//or myNewElement.innerHTML = "New list item text";

var myNewElement = document.createElement("li");
var secondItem = myElement.getElementByTagName("li")[1];
myElement.insertBefore(myNewElement, secondItem);
```

### 5). Events and Event Listeners
```go
What is an event?
```
```go
click a button
scroll the screen
click a form field
...
```
* Event Names
```go
onload
onclick
onmouseover
onblur
onfocus
...
```
* Event Handler
```go
write functions to handle or listen to events when they happen
```
```javascript
//method1: write event handler in html
<button onclick="alert('Hello World');">
Run Some JavaScript
</button>
```
```javascript
//method2: element.event
myelement.onclick = function(){
  // event handler code here
};//semicolon at the end of the block to end the statement
```
```javascript
//method3: using a method called addEventListener passing three parameters
//addEventListener(event, functionname, true/false)
document.addEventListener('click', myFunction, false);
document.addEventListener('click', anotherFunction, false);//benefit of method3
document.removeEventListener('click', anotherFunction, false);
```
```javascript
//working with onclick, onload

```
```javascript
//working with onblur and onfocus

```
```javascript
//working with timers: setTimeout(function, time), setInterval(function, time)
function simpleMessage(){
  alert("This is just an alert box");
}
setTimeout(simpleMessage, 5000);

//change images every 5ms
var myImage = document.getElementById("mainImage");

var imageArray = ["images/overlook.jpg", "images/winery.jpg", "images/lunch.jpg",
"_images/bigSur.jpg"];
var imageIndex = 0;

function changeImage(){
  myImage.setAttribute("src",imageArray[imageIndex]);
  imageIndex++;
  if(imageIndex >= imageArrary.length){
    imageIndex = 0;
  }
}

var intervalHandle = setInterval(changeImage, 5000);

//to clear interval
myImage.onclick = function(){
  clearInterval(intervalHandle);
```
### 6) Debugging JavaScript
* Common JavaScript errors
- `Issue 1: Syntax error`
- `Issue 2: calling a non-existent function`
- `Issue 3: using document.getElementById before the element is part of the DOM`
- `Issue 4: assignment instead of equality`
- `Issue 5: missing parameters in function calls`

* Using Firebug
- `DOM`
- `Script`
- ```go
breakpoint
```
- `Console`

### 7) Building Smarter Forms
```go
properties
events
onchage
onsubmit
```
### 8) UI Enhancement
* CSS and JavaScript
```go
properties in CSS become camelCase in JavaScript
```
```html
#example{
width:340px;
color: #fff;
font-weight:bold;
background-color: #4343;
}
```
```javascript
myElement.style.width="340px";
myElement.style.color="#fff";
myElement.style.fontWeight="bold";
myElement.style.backgroundColor="#4343"
```
* applying and removing CSS classes

### 9) JavaScript Best Practice
* Understanding JavaScript style
```go
1. naming conventions: meaningful, camelCase, Object: uppercase first letter
```
* Minifying JavaScript codes
```go
reduce file size
use minification tools: JSMin, YUI Compressors, Google Closure Compiler
```
* Using JavaScript code checkers
```go
Tool: JSLint
```
### 10) JavaScript Libraries
* a bunch of codes people wrote before
* jQuery/Lightbox2/...
* it is important to explore JavaScript libraries
* jQuery
```javascript
//regular JavaScript
document.getElementById("myDiv").className = "highlight";
```
```javascript
//jQuery
jQuery("#myDiv").addClass("highlight");//addClass() method is defined in the jQuery library
```
* jQuery Alias
```go
replace jQuery with $
```
```javascript
// $("what to find").someAction(any params);
$("#myDiv").addClass("highlight");
// using this in jQuery
$("h2").click(function(){
  $(this).text("Your clicked me!");
}); //this points to element h2
```

# Mind Mapping


## 2. MDN - [JavaScript Guide](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide)



