# Javascript
- JavaScript is the preferred language for client-side scripting of web pages.
- JavaScript can programmatically access and alter HTML elements and change a web site dynamically.
- JavaScript can animate, move, transition, hide, and show parts of a page instead of refresh the entire page.
- JavaScript is object-oriented, dynamically/weakly typed(variables easily converted from one to another), lightweight, scripting language.
- JavaScript is very different from Java.
- JavaScript  uses objects that have constructors, properties, and methods.
- JavaScript is dynamically instead of statically typed, meaning type checking is done at run-time instead of compile-time.


## client sides script pros and cons
### pros
- Reduces the load from the server computers.
- Browser can respond to user events faster.
- JavaScript can interact with HTML in ways that servers can’t.

### cons
- No guarantee that client computer has JavaScript enabled.
- Client computers may be unpredictable depending on the operating systems, programs, configs, and browsers used.
- Web development can be difficult because of the added interactions of different languages that have to interact properly to display a web page.

## LOCATIONS
- Similar to CSS, Javascript can be inline, embedded, or external.
- It is preferred not to use inline JavaScript because of maintainability and performance reasons.

### INLINE
```html
<a href = "JavaScript:OpenWindow();">more info<a/>
<input type="button" onclick="alert('Are you sure');" />
```

### EMBEDDED
- Embedded injection is by adding Javascript inside a \<script> tag inside the .html file.
- The location of this tag is very important, because if some scripts rely on previously declared variables, the page will not run if this tag is placed before those variables are declared.
- This \<script> tag can be placed inside the <head> or <body> tags.
```html
<script type="text/javascript">
/* a js comment*/
alert ("Hello World");
</script>
```

### external script
- External injection is by importing JavaScript through a separate file.
- enternal custom Javascript files can be imported as well as libraries hosted on the internet such as JQuery.js, Moment.js, and Toastr.js.
```html
<head>
    <script type="text/JavaScript" src="greeting.js">
    </script>
</head>
```

### comments
- in-line comments are applied with //
- mult-line comments are applied with /**/


## variable
- in js, variable are dynamically typed, meaning they are called out with a wild card reserved term like 'var','let' or 'const', but their type can change from objects, arrays, ...etc
- no variable should be re-declared after it's delcared
```
var x;
var y =0;
y = 4
```

## scope
the scope of let is block-wide
```js
{
    let x =2
}
x =3; //this is illegal, due it is out of scope of the decoratio;
```

the scope of var however, is global.

```js
{
    var x =2;
}
x =3; //this is legal;
```

```js
{
    const x =2;
}
x =2; //this is illegal; due to scope reason
```

## variable declaration
since 2015, use of ```var``` is replaced with ```let```, due to scope reason;   
declare with "const" is also available, but the value of a const cannot be changed after it's declaration;  

## variable group
- in js, we can declare variable in group
```js
let a,b,c;
const d=2,e=3;
```

## VARIABLE SYNTAX
- Numbers can be written with or without decimals.
- Strings can be written with **double dashes or single dashes**.
- The = sign is used to assign values to variables.
- Arithmetic operators like +  - * / can used to do math on values.

## VARIABLE NOMENCLATURE LIMITATIONS
- the first character must a letter or an underline. you cannot use number as the first letter of a variable name 
- The rest of the variable name can include any letter, any number, or the underscore. You can't use any other characters, including spaces, symbols, and punctuation marks.
- case sensitive
- no limit on the length of the variable name
- no reserve words

##  HOISTING
- Hoisting is the process of allowing a programmer to declare variables anywhere in the code and will still work even if they are used before they are called.
- The ‘var’ callout can be declared anywhere because of hoisting but the ‘let’ and ‘const’ callout must be declared before used.

## NULL + UNDEFINED + NAN
- Null: a variable is declared and assigned a value of null but means nothing.  Null is also an object but as opposed to standard objects, null objects return falsy.
- Undefined: a var that is declared but not defined
- NaN: a var is not a number

## utility method
### TYPEOF
- The ‘typeof’ operator can be used to find the type of a variable.
- typeof doesnt work on array, use Array.isArray instead.

### ISNAN
- check if a value is "not a number"
```
isNaN("hello")=true;
isNaN(1)=false;

```

### TRUTHY / FALSY
- Truthy/Falsy logic is very helpful when doing logic in JavaScript.
- instead of writing if(a != null && a!= undefined) you can just write if(!a) and does the same logic thanks to truthy/falsy logic.
![](../IMG/2022-10-09-22-18-28.png)
- to evaluate truthy and falsy, we can use
```js
let a=0;
Boolean(a);
!!a;
```

## STRINGS
- The string class is used to defined arrays of chars.
```js
let a=new String("good");
let a="good";

```

### concatenated
- Using the `` tick notation came out in 2015 per the ES6 notation and is often used in development because it eases the process of concatenating strings with variables.

```js
var str = a.concat("Morning");
var str = a +"Morning";
var str = `${str}+Morning`;


let space=' ';
let a = "a"+space+"b";
let b =`a+${space}+b`;
```

### other string methods
#### slice()
- slice() extracts a part of a string and returns the extracted part in a new string.

- The method takes 2 parameters: the start position, and the end position (end not included).
```js
let str = "Apple, Banana, Kiwi";
let part = str.slice(7, 13);

//if the index is a negative number, the slice will be backwards.
```

#### substring()
- substring() is similar to slice().

- The difference is that start and end values less than 0 are treated as 0 in substring().

- If you omit the second parameter, substring() will slice out the rest of the string.

#### substr()
- substr() is similar to slice().

- The difference is that the second parameter specifies the length of the extracted part.

#### replace()
- replace the first matched pattern with the second parameter.
- f you want to replace all matches, use a regular expression with the /g flag set.
- The replace() method returns a new string. instead of change the given one.
```js
let text = "Please visit Microsoft and Microsoft!";
let newText = text.replace("Microsoft", "W3Schools");
```

#### toUpperCase()&&toLowerCase()
```js
let text1 = "Hello World!";
let text2 = text1.toUpperCase();
let text3 = text1.toLowerCase(); 
```

#### concat()
- concat() joins two or more strings:
```js
let text1 = "Hello";
let text2 = "World";
let text3 = text1.concat(" ", text2);
```

#### trim()
- The trim() method removes whitespace from both sides of a string:
```js
let text1 = "      Hello World!      ";
let text2 = text1.trim();
```

####  padStart()&&padEnd()
- The padStart() method pads a string with another string:
```js
let text = "5";
let padded = text.padStart(4,"x");
> xxx5
let padded = text.padEnd(3,"c");
> 5cc
```

#### charAt()&charCodeAt()
- The charAt() method returns the character at a specified index (position) in a string
- The charCodeAt() method returns the unicode of the character at a specified index in a string:

#### split()
- A string can be converted to an array with the split() method:
```js
let text = "a,b,c,d,e,f";
const myArray = text.split(",");
> myArray = {a b c d e f}
```

## NUMBERS
![](../IMG/2022-10-10-00-39-35.png)
![](../IMG/2022-10-10-00-41-14.png)

### arithmetic
![](../IMG/2022-10-10-00-43-35.png)
```
^ is xor
| is or 
```

## OBJECTS
### OBJECT ORIENTED PROGRAMMING
- Javascript is not a fully OOP program because it doesn’t use inheritance and polymorphism to the extent of other OOP programs like Java and C++
- However, it does use the object structure extensively, using constructors, properties, and methods.

### JSON
- JavaScript Object Notation(JSON) is the most common way to define JavaScript structures.
- Object keys are not limited to variable notation, they are similar to strings, they can include spaces, start with numbers,…etc.

### INITS
- Every data structure in JavaScript(whether array, boolean, date, math, string, object,…etc.) requires a constructor to initialize them.
- These initializations can be defined in different ways.

```js
var someObject= new ObjectName(para1, para2, para3);
```

### PROPERTIES
- Properties are defined with dot notation that separates the instance with the property.

### METHODS
- Objects can also have methods assigned to them.
- These functions will run whenever they are called using the same dot notation used to call properties.
![](../IMG/2022-10-10-01-09-45.png)

### DOCUMENT OBJECT MODEL(DOM)
- According to the W3C, the DOM is a platform and language neutral interface that allows programs and scripts to dynamically access and update the content, structure, and style of documents.
- the root of a DOM is document tag

### DOCUMENT OBJECT
- The document object is the root JavaScript object representing the entire HTML document.
- It includes some information about the page including docType and inputEncoding.
![](../IMG/2022-10-10-01-21-08.png)

### BROWSER OBJECT MODEL(BOM)
- The BOM is similar to the DOM, but includes a bunch of objects that are accessible within a browser.
- This includes history, screen, navigator, and location objects.

![](../IMG/2022-10-10-01-32-04.png)

## ARRAYS
- It’s important to stay consistent with notations throughout an app. \
![](../IMG/2022-10-10-10-10-55.png)
![](../IMG/2022-10-10-10-11-13.png)
### add or remove elements from an array
- Adding an item to an array can be done using the .push() notation.
- To remove the last item, the .pop() notation can be used.
- Additional array methods include concat(), slice(), join(), reverse(), shift(), and sort().

### loop through an array
```js
for (var i=1,i<10,i++){
    //op code
}

const a = ["a","b"];
a.forEach(elementInA => {
    // ...use `elementInA`...
});

for (const element of theArray) {
    // ...use `element`...
}
```
### COPYING ARRAYS
- Arrays in JavaScript are not deep copied by default, they are shallow copied.
- Shallow copies mean that only pointer references are copied, not the structure themselves.
- For instance, if array A is assigned array B, and A[0] = 5 is assigned after the copy, then B[0] will automatically be set to 5 also.
- To prevent this, a deep copy is required, and one of the common ways of achieving this is by using JSON.parse and JSON.stringify functions.  This method works for most structures, but it does glitch out on unique fields and data types.
```js
let toCopy = [1,2,3];
let clone = Json.parse(JSON.stringify(toCopy));
```
## MATH
- The math class is used to access common mathematic functions and values quickly.
- JavaScript math functions include max(), min(), pow(), sqrt(), exp(), sin(), cos(), and arctan().
- It also includes PI, E, and SQRT2.

### Random
![](../IMG/2022-10-10-17-12-45.png)

## date
- The JavaScript date class is also very helpful for declaring dates and times.
The date functions of JavaScript can sometimes have limitations.  For this reason, the **moment.js** library is often imported to address this issue.
```js
var d = new Date();
alert(`Today is ${d}`);
```
![](../IMG/2022-10-10-11-23-07.png)

## CONDITIONALS
- If an && symbol is used, it means that if the operand on the left is thruthy, the operand on the right will display.
- If an || symbol is used, it means that if the operand on the left is falsy, the operand on the right will display.

### OPTIONAL CHAINING
Conditional assignments are used in the form of optional chaining to avoid throwing an error if a nested field doesn’t exist.
Traditionally, optional chaining was achieved with this syntax:
```js
let x = a&&a.b&&a.b.c
```
But as of 2020, optional chaining was introduced with this syntax:
```js
let x = a?.b?.c;
```

### TOGGLE SYNTAX
- Toggling variables is often done with the ! operator.
- Toggling can be used for checkbox bindings, collapsing elements, or hiding elements.
```js
var x = true;
function toggle(){
    x = !x;
}
```

### == vs. ===
- == check the value of the expression
- === check both the value and the type of the expression

## loop
### FOR LOOPS
- A ‘for’ loop combines the common components of a loop, with initialization, condition, and post-loop operation into one statement.
- If break is used inside the ‘for’ loop, it will exit out of the loop.
- If continue is used inside a ‘for’ loop, it will skip the iteration.
- If return is used inside a ‘forEach’ loop, it will skip the iteration
- **there is no way to break out a forEach loop**

### WHILE LOOPS
- A while loop ends when a condition is met, otherwise it continues to loop.
- most browsers nowadays have a kill operation when it realizes that it is stuck in an infinite loop.

### functions
- Functions are the building blocks for modularity in JavaScript.
- They are defined by using the reserved word ‘function’ before the function name and optional parameters.
- Since JavaScript is dynamically typed, functions do not always need to return a type.

### CALLBACK FUNCTIONS
- in JS, a function can be passed as an parameter in another function.
- They are often used on asynchronous communications, where one function has to wait for another function.

### ARROW NOTATION
- Arrow notation is often used with array methods because it is more succinct.
- The values inside the () are the params and the values inside the {} is the logic.  A return line is required if {} is used.  If {} is not used, a return line is not required but the logic is usually only written within one line. 
![](../IMG/2022-10-10-12-40-49.png)

### GENERATORS
- Generators are functions that can return multiple values in a sequence.
- It does this using function* syntax, the .next() method, and will return a value, done object.
```js
function* generator(){
    yield 1;
    yield 2;
    return 3;
}

let a = generator();
let b=a.next();
```

### EVALS
- convert a string to a math expression; 
```js
> var x =10;
undefined
> var z =20
undefined
> eval("x*z");
200
```
### REGEX MODIFIERS
- /i case sensitive matching.
- /g perform a global match;
- /m perform a multiple match;

### ALERTS AND CONFIRMS
- The alert() and confirm() functions are used to display pop-ups to the user.
- Alerts are usually never used on production code, most serious applications use custom professional modals, but alerts are good for debugging.

## DOM
### NODES
- In the DOM, each element within an HTML document is a node.
- The most common task in JavaScript is finding the right node, accessing it, and modifying it using properties and methods.

### DOM ACCESS
- One of the common ways to select elements in HTML is using the getElementById() method.
- This method selects a specific Id on the HTML, and binds JavaScript to it.  There is also a class version of this with getElementByClassName().
- also, to select a node by tag, we can use document.getElementsbyTagName();

### ELEMENT NODE OBJECT
- The object returned from .getElementById() is an element node object.
- The node object includes the content wrapped around the <> and </> tags.
- the selected element contains several properties

![](../IMG/2022-10-10-13-20-10.png)
![](../IMG/2022-10-10-13-25-33.png)

### DOM CONTENT MODS
- Using the element node object, changes can be made to content in the DOM.
![](../IMG/2022-10-10-13-29-33.png)

- Using the element node object, changes can also be made to the style of the DOM.
- It is encouraged to use a class selector when changing an HTML element style dynamically using JavaScript
![](../IMG/2022-10-10-13-32-30.png)


## EVENTS
- An event is an action that can be detected by JavaScript and serve as a trigger.
- Most of created by inputs from the user, but others can be triggered by the browser.
- An event is said to be triggered, and then caught by a JavaScript function, and the response is executed.
- Event handlers are used to respond to certain events.

### legacy HOOKS
- JavaScript can be inserted inline, embedded, or on an external file.
- In the 90s, events were historically inserted inline a tag using hooks, but later they were inserted using listeners.
![](../IMG/2022-10-10-17-14-54.png)

### LISTENERS
- The idea of listeners is that the HTML is left intact, but JavaScript selects certain elements and adds an event to it.
- This method is better than using old fashion event hooks because it uncouples the HTML from the JavaScript.
- The disadvantage is that only one handler can respond to any given element event.

#### syntax
![](![](../IMG/2022-10-10-17-20-31.png).png)

#### EVENT BUBBLING
- When an event happens on an element, it first runs the handlers on it, then on its parent, then all the way up on other ancestors.
For instance, in the blue boxes shown, if all 3 elements(form, div, p) have an event, and p is clicked, the p event will handle first, the - div event will handle second, and the form event will handle third.
- To prevent bubbling the **event.stopPropagation()** can be used to only run the event clicked on.
![](../IMG/2022-10-10-17-25-57.png)

####  EVENT OBJECT
- Event functions pass a parameter called the event object, that provides information about the DOM element.
- This object has a lot of useful properties and methods such as bubbles, cancelable, and prevent default.

#### Bubbles 
a bool is set to true, so it knows to first check for an event handler at the element, otherwise it will continue to bubble up to the parent searching for this handler, all the way up to the root.  If none is found, the event will remain unhandled.
#### Cancelable 
a bool that indicates whether the event can be cancelled.  
#### PreventDefault 
actually cancels a default event.  So if an event is cancellable, the preventDefault function will often follow.  An example is preventing a link from opening up and bypassed with other code.

### FRAME EVENTS
- Frame events usually run based on the life cycle of the page and run once.
- They can trigger if user loads page or exits page.
![](../IMG/2022-10-10-17-33-26.png)

## class
### CLASS PROTOTYPES
- Once a constructor is created, it can not be modified unless a prototype is used.
- A prototype can add or delete properties and methods from a constructor as shown below.
![](../IMG/2022-10-10-17-35-55.png)

## SEQUENCING
### PROMISES
- A promise represents an operation that hasn’t completed yet.
- It is an object that represents the eventual completion or failure of an asynchronous operation.
- Promises can be chained with .then()
- The returned states is either resolved, rejected, or pending.
![](../IMG/2022-10-10-17-36-55.png)
### async/await
- The Async/Await syntax is an alternative way to make promises easier to code so that they are sequential.
- The Async syntax is used before the function definition, and await is used before the function call. 
![](../IMG/2022-10-10-17-37-56.png)

### timeout
- Timeouts are used to run code after a set duration.
![](../IMG/2022-10-10-17-39-41.png)