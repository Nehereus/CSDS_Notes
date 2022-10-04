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
- This<script> tag can be placed inside the <head> or <body> tags.
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
- 