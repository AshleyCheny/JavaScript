# JavaScript
* Browser: Chrome/Firefox
* Text Editor: Sublime Text2

## 1. Lynda.com - [JavaScript Essential Training](https://www.lynda.com/MyPlaylist/Watch/6752886/87513?autoplay=true)

* 1. How does JavaScript work with HTML and CSS?
* ---1) Client-Side programming Language
* ---2) Only works in a Web Browser
* ---3) Can not access to database
* 2. JavaScript is CASE SENSITIVE
* 3. JavaScript comment: two formard slashes// multi lines/*   */
* 4. When the JavaScript run?
* ---1) in the head/body-inline JavaScript
* 5. Variables are containers(e.g.,var year;) no need to specify the variable types
* 6. `Array` in JavaScript is dynamic.
* 7. An object has properties and methods. Check the properties and methods for objects througth Reference.
* 8. JavaScript `numbers` are 64-bit floating point numbers.
* 9. Not a Number(NaN), isNaN()
* 10. `String` methods: split(),indexOf(), slice(), substring(), substr().../string comparison(case sensitive)
* 11. `date` object month/week/hour is zero-based, date comparison
* 12. create a method for an object
```go
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
*  

# Mind Mapping


## 2. MDN - [JavaScript Guide](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide)



