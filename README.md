# JavaScript
* Browser: Chrome/Firefox
* Text Editor: Sublime Text2

## 1. Lynda.com - [JavaScript Essential Training](https://www.lynda.com/MyPlaylist/Watch/6752886/87513?autoplay=true)

* 1. How does JavaScript work with HTML and CSS?
```go
Client-Side programming Language
Only works in a Web Browser
Can not access to database
```
* 1. JavaScript is CASE SENSITIVE
* 3. JavaScript comment: two formard slashes// multi lines/*   */
* 4. When the JavaScript run? in the head/body-inline JavaScript
* 5. Variables are containers(e.g.,var year;) no need to specify the variable types
* 6. `Array` in JavaScript is dynamic.
* 7. An `object` has properties and methods. Check the properties and methods for objects througth Reference.
* 8. JavaScript `numbers` are 64-bit floating point numbers.
* 9. Not a Number(NaN), isNaN()
* 10. `string` methods: split(),indexOf(), slice(), substring(), substr().../string comparison(case sensitive)
* 11. `date` object month/week/hour is zero-based, date comparison
* 12. create a method for an object
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
*  13. `DOM`(Document Object Model)
```go
What is the document? --> web page
What are the objects? --> things, pieces
What is the model? --> tree structure, a standard we can use
so, DOM is not a language, it is an idea, an convention
it is an agreed-upon terminology that will let us describe and interact with any web page.

What we can do with DOM?
Get the title text
Get the second paragraph
Get the third link in the menu and set its CSS to display:none
Change the background color of all paragraphs with a class of "important"
Get all the <li> elements in the last unordered list
Find the image with an id of "logo" and move it 40 pixels to the right
Change a link so it performs a JavaScript function when clicked
Create a new unordered list and insert between first and second paragraphs

DOM is a way to reach into the page from the script and the way the page can reach into the script 
A TREE STRUCTURE OF A WEB PAGE
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

# Mind Mapping


## 2. MDN - [JavaScript Guide](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide)



