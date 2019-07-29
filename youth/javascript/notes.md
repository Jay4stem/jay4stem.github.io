### JavaScript - Web application development

## History

JavaScript was introduced by Brendan Eich in 1995 for Netscape Communications. It was submitted few months later to Ecma International for consideration as an industry standard. The result standard version is ECMAScript.

Even if the name comes from a partnership between Netscape and Sun Microsystems (distributor of Java) JavaScript is not a "light" version of Java.

    A Brief History of JavaScript by Brendan Eich (video)

## Definition & properties

JavaScript is a scripting language that supports multiple programming styles. It differs from other languages such as C++, Java or PHP with its dynamic behaviour, its first-class functions and its prototype-based inheritance.

JavaScript lovers consider these features as the force of the language. It's very common for people who try to write JavaScript like they write code in other languages to hate it. Don't make this mistake!

    - Dynamic
    - Weakly typed
    - Multi-paradigm
    - Imperative
    - Functional
    - Object-oriented
    - First-class functions
    - Prototype-based

Usages

Even if it was originally designed to work in a browser environment, JavaScript is now used on several different platforms. Here are a few examples :

    - Web server
    - Browser addons/extensions
    - Mobile applications
    - Databases consoles
    - OpenOffice scripts/macros
    - Java applications

    - node.js
    - Building and extension for Firefox
    - Get started with Chrome extension development
    - PhoneGap
    - MongoDB
    - Mozilla Rhino

## Basic syntax

  1. JavaScript is case-sensitive.
  2. Lines end by semicolon ;.
  3. Block are delimited curly brackets by { }.
  4. Comments are between /* */ for multiple lines or after // for one line.
  
## Variables & Types

In JavaScript, Typing is dynamic. Therefore, there is NO type declaration before variable names. Instead we use a unique keyword : var. Note that a variable can be declared several times. If it's non-declared, the variable is automatically allocated at the first use.

### Number

Numbers like in any other languages are really important. Don't forget that a computer is primarly a super calculator. Integers and floats have the same type : Number. Of course, a variable can only be identified as type Number at execution time..

If you want to manipulate numbers, the objects Number and Math has lots of useful properties and methods. The other useful way to manipulate them is operators of course. See reference for more details.
```js
// Integer
var i;            // first declaration of i (type is undefined)
i = 2;            // i is now a integer (type is number)

In this example we see that floats can have strange behaviour, don't forget the internals of the float storage. It's stored as IEEE 754.

// Float
var i = -5.01;    // second declaration of i as a float (type is number)
j = 2;            // j was not declared, automatic assignement to 2
j = i + 1.12;     // j is now a float equal to 3.12 (still number)
// Be careful
var k = 0.1 + 0.2 // k => 0.30000000000000004

var l = new Number(7);    // DO NOT USE : type is object and not number

// Specials
var a = 10 / 0;           // => Infinity
var b = -10 / 0;          // => -Infinity
var c = Math.sqrt(-1);    // => NaN : Not a Number

    Number reference (MDN)
    Math reference (MDN)
    Why should you not use Number as a constructor? (stack overflow)
    The_Complete_JavaScript_Number_Reference, usage of new Number(2) (hunlock)
```

### String

Strings are really simple. Quotes or double quotes, no differences, some text in it and you're done. The most important property of a String when it comes to manipulation is length. It's not the only one, the String object contains a lot of useful properties and methods, see reference for more details.

The other way a good programer should manipulate string is regular expressions and as expected, JavaScript provides a regex engine and a RegExp object. Regex can be complicated to master, but the game is worth it since it's a multi language concept. See reference for more details.

var a = ""; // The empty string: it has zero characters
var b = 'There is no spoon.';
var c = "Only human.";
var d = 'pill="red"';
var e = "Free your mind.";
var f = "You're empty.\nSo are you."; // Type of all variables is string

var g = new String("Welcome to the real world.");
// DO NOT USE : type is object and not string

    String reference (MDN)
    Regex reference (MDN)
    regular-expressions.info
    Online testing tool (gskinner.com)

### Boolean

Nothing fancy here, true of false. You'll see later that other types of variables (Number, String...) can by evaluated as booleans according to some rules.

var realWorld = false;
var matrix = true;         // Type of all variables is boolean

var a = new Boolean(true); // DO NOT USE : type is object and not boolean

    Boolean reference (MDN)

### null and undefined

Both null and undefined are used for absence of a value. One is used when the variable has been initialiazed : null. The other one is used when the variable has not been initialized : undefined. It can be returned by function that have no return statement.
```js
var neo;      // Type is undefined
neo = null;   // Type is object
```
    Typeof null is object (MDN)
    undefined reference (MDN)

### Arrays

An array is an ordered colleciton of values. Values can be of different types. Each value is called an element and is positioned in the array with a numeric index starting at zero.

The Array object has several properties and methods. The most important property is length, it contains the size of the array. See reference for more details.

    Array reference (MDN)

### Creating

The easiest way to create an array is with square brackets and comma separated values in it. Note that you can create an array with 4 undefined elements, length will be 4.
```js
var a = [];                         // no elements
var b = new Array();                // equivalent to a
var c = [,,,,];                     // 4 elements, all undefined.
var d = new Array(4);               // equivalent to c
var e = ["the", 1, true];           // 3 elements of different types
var f = new Array("the", 1, true);  // equivalent to e
```
## Reading and writing

Reading and writing in arrays is done with brackets and equal assignment operator. Note that reading from and index that haven't been initialized doesn't generate any errors, it returns undefined.

You can insert values in non consecutive indexes, it create a what's called a "sparse array". The length is updated to maximum index + 1.
```js
var a = ["white"];    // Start with a one-element array

var b = a[0];         // b => "white"
var c = a[100];       // c => undefined (no error)

a[1] = 3.14;          // a => ["white", 3.14]
var i = 2;
a[i] = 3;             // a => ["white", 3.14, 3]
a[i + 1] = "rabbit";  // a => ["white", 3.14, 3, "rabbit"]
a[a[i]] = a[0];       // a => ["white", 3.14, 3, "white"]

var d = a.length;     // d => 4
```
## Adding and deleting

To add and delete elements from an array, you can use the methods from the Array object. There's a lot of useful ones, from simple pop and push to more complex ones like splice. See reference for more details.
```js
var a = ["follow", "the", "white", "rabbit"];

var b = a.pop();             // a => ["follow", "the", "white"]
                             // b => "rabbit"
var c = a.push("RABBIT");    // a => ["follow", "the", "white", "RABBIT"]
                             // c => 4 (new length)

var d = a.shift();           // a => ["the", "white", "RABBIT"]
                             // d => "follow"
var e = a.unshift("FOLLOW"); // a => ["FOLLOW", "the", "white", "RABBIT"]
                             // e => 4 (new length)

var f = a.splice(2, 1);       // a => ["FOLLOW", "the", "RABBIT"]
                              // f => "white"
var g = a.splice(1, 2, "ME"); // a => ["FOLLOW", "ME"]
                              // g => ["the", "RABBIT"]
```
## Operators

Operators are really powerful in JavaScript. Unlike in some other languages like C, operators are not only used to do maths, they are also very useful with strings.

    Operator Precedence reference (MDN)

## Arithmetic

Arithmetic operators work the same way as a lot of other programming languages. Note that + is used to concatenate strings.
```js
var a = 6 + 4;                    // a => 10
var b = -a;                       // b => -10
var c = 6 - 4;                    // c => 2

var d = 1, e = ++d;               // d and e are both 2
var f = 1, g = f++;               // f is 2, g is 1
var h = 7, i = --h;               // h and i are both 6
var j = 7, k = j--;               // j is 6, k is 7

var l = 3 * 3                     // l => 9
var m = 10 / 3                    // m => 3.3333333333333335
var n = 10 % 3                    // n => 1

var o = "Dodge" + " " + "this."   // o => "Dodge this.";
```
    Arithmetics operators reference (MDN)

## Equality

A particularity of JavaScript is the two kinds of equality comparison : strict and type-converting. Just remember that strict equal === compares both types and values and type-converting equal == converts one type to the other and just compares values.

Best practice is to always use the strict equality. It prevents a lot of mistakes.
```js
// Equality
var a = "2" == 2;    // a => true
var b = "2" != 2;    // b => false

// Strict equality
var c = "2" === 2;   // c => false
var d = "2" !== 2;   // d => true
```
    Comparison operators reference (MDN)

## Comparison

Like arithmetics, comparison operators work the same way as a lot of other programming languages. Note that these operators can be used to compare string.
```js
var a = 2 > 2;          // a => false
var b = 2 <= 2;         // b => true
var c = "2" >= 2;       // c => true
var d = 2 < 2;          // d => false
var e = 2 <= 2;         // e => true

var f = 'abc' < 'def'   // f => true
```
    Comparison operators reference (MDN)

## Logical
```js
var a = true && false;  // a => false
var b = true || false;  // b => true
var c = !true;          // c => false
```
    Logical operators reference (MDN)

## Bitwise

Bitwise operators help programmers to use numbers like sequences of 32 bits (zeros and ones). It's not always easy to understand what's going on but it's very useful, for example if you're implementing bitmasks.
```js
var a = 42 & 2   // a =>          2  (AND)
var b =  7 | 2   // b =>          2  (OR)
var c =  7 ^ 2   // c =>          7  (XOR)
var d = ~8       // d =>         -7  (NOT)
var e =  1 << 3  // e =>          8  (Shift left)
var f =  8 >> 2  // f =>          2  (Shift right)
var g = -1 >>  2 // g =>         -1
var h = -1 >>> 2 // h => 1073741823  (Shift right with zero fill)
```
    Bitwise operators reference (MDN)

## Assignement

Assignement operators saves you some place and can improve code readability. Use them carefuly!
```js
var a = 1, b = 0;
a += b    // a = a + b
a -= b    // a = a - b
a *= b    // a = a * b
a /= b    // a = a / b
a %= b    // a = a % b
a <<= b   // a = a << b
a >>= b   // a = a >> b
a >>>= b  // a = a >>> b
a &= b    // a = a & b
a |= b    // a = a | b
a ^= b    // a = a ^ b
```
    Assignment operators reference (MDN)

## in

The in operator is used to verify if a property is specified on an object. Be careful when you use it.
```js
var a = [1,9,4];
var b = (2 in a);          // b => true
var c = (9 in a);          // c => false
var d = (length in a);     // d => true
```
    in operator reference (MDN)

## typeof

typeof is used at compilation time to verify the type of a variable.
```js
var a = 3;
var b = typeof a;   // b => "number"
var c = "";
var d = typeof c;   // d => "string"
var e = true;
var f = typeof e;   // f => "boolean"
```
    in operator reference (MDN)

## Type conversions

JavaScript is not statically typed but you can determine the type of a variable at execution time. Conversion from one type to another can be done explicitly or implicitly. It's really important to understand implicit ones, they can help you to avoid strange behaviours and bugs.
Explicit

Explicit conversions can for example help you to convert a string to a number. Note that even if integers and floats are both number, using parseInt on a float removes the decimals and makes it by definition an integer.
```js
// to Number
var a = Number("10");         // a => 10
var b = Number(false);        // b =>  0
var c = parseInt("10", 10);   // c => 10
var d = parseInt(10.2);       // d => 10
var e = parseFloat("10.2");   // e => 10.2

// to String
var a = String(false);        // a => "false"
var b = String(10);           // b => "10"
var c = String(10.2);         // c => "10.2"
var d = (10).toString();      // d => "10"

// to Boolean
var a = Boolean(10);          // a => true
var b = Boolean(0);           // b => false
var c = Boolean(0.3);         // c => true
var d = Boolean("true");      // d => true
```
## Implicit

There's a lot of ways to convert a string to a number. Performances can differ a lot depending on the technique used and the plateform. A shorter syntax is often prefered for bandwith uses.

Look carefully how the + operator behaves with strings and numbers.
```js
// to Number
var a = +"10";            // a => 10
var b = "10" >> 0;        // b => 10
var c = "10" * 1;         // c => 10
var d = ~~"10";           // d => 10
var e = "2" * "5";        // e => 10 (both strings converts to number)

// to String
var a = 10 + "10";             // a => "1010"
var b = "10" + "10";           // b => "1010"
var c = 10 + " agents";        // c => "10 agents"
var d = 10 + 10 + " agents";   // d => "20 agents"

// to Boolean
var a = !!'morpheus';     // a => true
var b = !!'';             // b => false
var c = !!'0';            // c => true
var d = !!'1';            // d => true
```
    String to number comparison (jsperf.com)

## Statements

## Conditional

In JavaScript, conditionnal statements behaves pretty much like in other common languages.

Note that the conditional ternary operator should only be used in simple cases. It is often use for variable assignment and its usage is synonym of shorter syntax and readability. If you think it doesn't make your code better, use a classic if.
### if/else

In this case, normal equality is handy, used with null, it can test null || undefined.
```js
if (username == null) {  // if username is null or undefined,
  username = "Trinity";  // define it
}

if (bulletCount === 1) {
  bulletCount += ' bullet';
} else {
  bulletCount += ' bullets';
}

var user = (name == null) ? 'default user' : name;
```
    If...else reference (MDN)

### switch

Switch usage is often advised when you have too much if statements. Don't forget the break keyword. Note that you can use string unlike some other languages.
```js
var quote;
switch (characterName) {
  case 'Smith':
    quote = 'Goodbye, Mr. Anderson...';
    break;
  case 'Neo':
    quote = 'I know kung fu.';
    break;
  default:
    quote = 'What is the Matrix?';
    break;
}
```
    Switch reference (MDN)

### loops
```js
for (var i = 0; i < 10; i++) {
  doSomething();
}

var count = 0;
while (count < 10) {
  doSomething();
  count++;
}

var count = 100;
do {
  doSomething();
} while (--count > 0);
```
    Loops reference (MDN)

### for...in loops

for..in loops are used to iterate over properties of an object.

Array indexes are just enumerable properties with integer names. Therefore, for...in loops could be used to enumerate elements of an array.

Because of performance issues and in order to avoid bugs, use classic for loops instead of for..in with arrays.
```js
var a = [123, 456, 789];
for (var i in a) {      // DO NOT use with arrays
  doSomething(a[i]);
}
```
Because of performance issues and in order to avoid "bugs" and "strange behaviours", use classic for loops instead of for..in with arrays.

    for...in loops reference (MDN)
    for vs. for..in (JSperf.com)

Browser objects

Every JavaScript plateform/environment adds objects with global scope. They're meant to provide helpful features to developers. In web browsers the most important ones are : document and window.

Another object is present but only in modern browsers : console. Since it's not standard, implementations may differ, see references for more details. Remember that older browsers don't support it, so don't let console.log('foo') etc... in production code.

var title = document.title;
var href = window.location.href;
var userAgent = window.navigator.userAgent;

window.alert('Never send a human to do a machine\'s job.');
var bluePill = confirm('Take the blue pill?');
var name = prompt('What is your name?');

console.log('Perhaps we are asking the wrong questions.');
console.error('Nothing. Just had a little déjà vu.');
console.info('A déjà vu is usually a glitch in the Matrix.');
console.warn('The Matrix is a system, Neo. That system is our enemy.');

    document reference (MDN)
    window reference (MDN)
    Firefox web console (MDN)
    Chrome web console
    IE web console
    Opera web console
    Safari web console

## Tools

Your browser should have two very useful tools to work with JavaScript :

    JavaScript Debugger
    JavaScript Console

There's also great tools on the web :

    JSfiddle (online playground)
    JS Bin (online playground)
    Codepen (online playground)
    tinkerbin (online playground)
    JSperf (online benchmarking tool)


    JavaScript Reference (MDN)
    ECMAScript documentation
    JavaScript Garden (github)
    Eloquent JavaScript


