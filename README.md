# Front-End Developer Job Interview QnA
To be successful in every interview!<br>
List of things to check before the interview as long as you work as a web developer

---
## General Question
**Responsive web design**
- approach to web page creation that makes use of flexible layouts, flexible images and cascading style sheet media queries.  The goal of responsive design is to build web pages that detect the visitor’s screen size and orientation and change the layout accordingly.

**Optimize a websites assets/resources**
- compress image files
- Concatenate and minify JavaScript and CSS Files
- Use sprite sheets and icon fonts
- Use a cdn for jquery and hosting video

 
 **3 ways to decrease page load.**
- The best way is usually to reduce your image sizes. Minify and concatenate JS/CSS. Have JS at the bottom of the page. Use a CDN.

**Overriding vs Overloading**


## HTML
**The importance of Doctype in HTML**
* Doctype tells the browser which version of HTML/XHTML standard is used and how to render the page.


**Metadata**
- Information data which is not be displayed on the page. But it's parsable. Typically used to specify page description, keywords, author




**The new features of HTML5 standard**

- Semantic elements: nav, article, section, header, footer and aside 
- Form controls: calender, data, time, email, url, and search
- Better support for embedded media using audio, video and canvas

**Semantic HTML**
- It means the opposite of using divs for everything. Taking advantage of new HTML5 elements like nav, article, header, footer, etc.

**cookies vs sessionStorage vs localStorage**
- Cookies are for storing small amounts of website data, such as a user name.  HTML5 Web Storage is a faster, improved means of storing website data.
- sessionStorage is available only when a browser’s tab is opened. (temporary data)
- localStorage survives on closing (persistant data)


**Data – attributes**
- Data attributes are used to store custom data directly inside HTML tags. They are easily-accessible from CSS and JavaScript






## CSS
Selectors - ID, Class, First-child etc..


**3 ways to apply css styles**
- Inline - inline style attribute on element
- Internal - using &#60;style&#62; block in the &#60;head&#62; section
- External - loading external css file using the &#60;link&#62; tag



**Specification - Priority (from low to high)**
 -  CSS specificity is a score or rank that decides which style declaration has to be used to an element.

  1. Type selectors (e.g. h1) and pseudo-elements (e.g. ::before)
  1. Class selectors, attributes selectors (e.g. [type="radio"]) and pseudo-classes (e.g. :hover)
  1. ID selectors (e.g. #example)
  1. !important - overrides every other selectors, including inline added into a tag.


**Flex**
- It allows you to design a flexible responsive layout structure without using any float or positioning property of CSS. To use CSS flexbox you need to define a flex container initially.

flex-direction
flex-wrap
flex-flow
justify-content
align-items
align-content


**Position static vs absolute vs fixed vs relative**
- *Static* - this is the default value, all elements are in order as they appear in the document.
- *Relative* - the element is positioned relative to its normal position.
- *Absolute* - the element is positioned absolutely to its first positioned parent.
- *Fixed* - the element is positioned related to the browser window.
- *Sticky* - the element is positioned based on the user's scroll position.


**display: none vs visibility: hidden**
- *display: none* - none removes the element from the flow, allowing other elements to fill in.
- *visibility: hidden* – only hides the element,  but space is allocated for it on the page


**Normalize CSS vs Reset CSS**
- Each browser has different default styles.
Normalizing will fix the browser style that has the difference
Resetting removes all the native styles provided by browsers.


**Sprites**
- CSS sprite is merging multiple images into a single image.
It reduces the amount of WEB-requests and increases page speed

**SVG**
- SVG stands for Scalable Vector Graphics, it is used to show vector graphics on the page. The biggest benefit is that SVG-images don’t lose quality when zoomed or resized (unlike JPG).
You can easily change the size, color and animate SVG images. SVG’s also can be bundled in a SVG – sprite.


**CSS preprocessor (Sass, Less or Stylus)**
- CSS preprocessor is a tool which allows you to create CSS code much faster, in a more structured manner. <br>
A program/tool that has its own syntax which gets compiled later in standard CSS code.
Preprocessors extend the CSS functional by adding variables, mixins, partials, also allow to use operators inside the code.


**Box-Model**
- Box model represents a structured way to space elements in relationship to each other. It is made of margins, borders, padding, and content. When the page is being rendered, the browser shows each of the elements as a rectangular which can be styled using CSS.

**box-sizing:border-box**
**Layout -float, box-grid etc..**


## Javascript
**“==” vs “===” operators**
- == : Check value only (javascript do type coercion)
- === : Check value as well as type. more strictly, the types must be the same to be considered equal.

**What's a hashtable?**
- A hashtable is an associative array of key/value pairs. JavaScript Objects are hashtables.

**Scoping: difference var / const / let**
 - *var* has global scope and functional scope depending on where it is. var is hoisted.

- *let & const* were introduced in ES6, They have block scoping inside of the curly brackets. They aren’t hoisted<br>
- *const* - many people think const is immutable, but it can be changed property with inside them, just you can’t reassign const.


**Closure**&#42;&#42;&#42;

- A closure is a function defined inside another function (called parent function) and has access to the variable which is declared and defined in parent function scope.

- The closure has access to variable in three scopes:
  - Variable declared in his own scope
  - Variable declared in parent function scope
  - Variable declared in global namespace

```javascript
function outerFunc() {
  var x = 10;
  var innerFunc = function () { console.log(x); };
  return innerFunc;
}

/*
 When outerFunc is called, it return innerFunc.
 then execution context of outerFunc is destroyed.
 */
var inner = outerFunc();
inner(); // 10


/* Even though outerFunc's life-cycle is finished, (execution context is destroyed)
innerFunc can access to local variable of outerFunc */
```

**How/why would you use Closure?&#42;&#42;**
 
**Keyword: This**
- The JavaScript this keyword refers to the object it belongs to.
It has different values depending on where it is used: <br>
  - In a method, this refers to the owner object.
Alone, this refers to the global object.
  - In a function, this refers to the global object.
  - In a function, in strict mode, this is undefined.
  - In an event, this refers to the element that received the event.
- Methods like call(), and apply() can refer 'this' to any object.


**What's a typical use case for anonymous functions?**
- For single use methods, like when you need to pass a one-liner of code to another function.
- Or when you want to scope vars via a closure.

**Call, Apply, and Bind methods (why would you use?)**
- .apply and .call do the same thing, 
- but .apply uses an array containing arguments for the target method as the second parameter.
- function.prototype.bind
  - Use this to create functions that when called have a particular value for this and therefore binding it to the original value of the target object

**Hoisting**
- Hoisting is JavaScript's default behaviour of moving declarations to the top.
Hoisting is the JavaScript interpreter's action of moving all variable and function declarations to the top of the current scope. There are two types of hoisting:
  - variable hoisting - rare
  - function hoisting - more common
- Wherever a var (or function declaration) appears inside a scope, that declaration is taken to belong to the entire scope and accessible everywhere throughout.


**Synchronous vs Asynchronous**
- Synchronous way:
  - It waits for each operation to complete, after that only it executes the next operation. For your query: The console.log() command will not be executed until & unless the query has finished executing to get all the result from Database.

- Asynchronous way:
   - It never waits for each operation to complete, rather it executes all operations in the first GO only. The result of each operation will be handled once the result is available. For your query: The console.log() command will be executed soon after the Database.Query() method. While the Database query runs in the background and loads the result once it is finished retrieving the data.

- Use cases:
If your operations are not doing very heavy lifting like querying huge data from DB then go ahead with Synchronous way otherwise Asynchronous way.

In Asynchronous way you can show some Progress indicator to the user while in background you can continue with your heavy weight works. This is an ideal scenario for GUI apps.


ES6 Class
Promises - 3states : fulfilled / rejected / pending
Async/Await
Observables


**Callback function**
- A callback function is a function that is passed to another function as an argument and is executed after some operation has been completed. Below is an example of a simple callback function that logs to the console after some operations have been completed.
```javascript
function modifyArray(arr, callback) {
  // do something to arr here
  arr.push(100);
  // then execute the callback function that was passed
  callback();
}

var arr = [1, 2, 3, 4, 5];

modifyArray(arr, function() {
  console.log("array has been modified", arr);
}); //[ 1, 2, 3, 4, 5, 100 ] 

```
**Null vs Undefined**
- JavaScript (and by extension TypeScript) has two bottom types: null and undefined. They are intended to mean different things:
  - Something hasn't been initialized : undefined.
  - Something is currently unavailable: null.

  
 

## White Board
String manipulation- reverse,
Palindromes
Fibonacci sequence
Fizzbuzz


**Q. How do you create a private variable in Javascript?**
```javascript
function secretVariable(){
	var private = "super secret code";
	return function () {
		return private;
	}
}

var getPrivateVariable = secretVariable(); 

console.log(secretVariable());  // f(){ return private;}
console.log(getPrivateVariable()); // "super secret code"

```



**Q. What is the output?**
```javascript
var hero = {
  _name: 'John Doe',
  getSecretIdentity: function (){
    return this._name;
  }
};

var storeSecretIdentity = hero.getSecretIdentity;
var storeSecretIdentity2 = hero.getSecretIdentity.bind(hero); 

console.log(storeSecretIdentity()); //undefined
console.log(hero.getSecretIdentity()); // John Doe
console.log(storeSecretIdentity2()); //John Doe


/*
have to rebind hero, stick the hero onto stolensecretIdentity.
(Haven’t extracted the hero from it)
*/
```


**Q. What is the output?**
```javascript
var num = 4;
function outer() {
	var num = 2;
	function inner(){
		num++;
		var num = 3;
		console.log(num);
	}
	inner();
}
outer(); //3
```





 
## Framework
**Understand Life cycle Hooks**


