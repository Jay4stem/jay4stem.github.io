## Hello World
```html
<!DOCTYPE HTML>
<html>

<body>

  <p>Before the script...</p>

  <script>
    alert( 'Hello, world!' );
  </script>

  <p>...After the script.</p>

</body>

</html>
```

## Variables

A variable is a “named storage” for data. We can use variables to store goodies, visitors, and other data.

To create a variable in JavaScript, use the let keyword.

The statement below creates (in other words: declares or defines) a variable with the name “message”:
```js
let message;
```
Now, we can put some data into it by using the assignment operator =:
```js
let message;

message = 'Hello'; // store the string
```
The string is now saved into the memory area associated with the variable. We can access it using the variable name:
```js
let message;
message = 'Hello!';

alert(message); // shows the variable content
```
To be concise, we can combine the variable declaration and assignment into a single line:
```js
let message = 'Hello!'; // define the variable and assign the value

alert(message); // Hello!
```
We can also declare multiple variables in one line:
```js
let user = 'John', age = 25, message = 'Hello';
```
That might seem shorter, but we don’t recommend it. For the sake of better readability, please use a single line per variable.

The multiline variant is a bit longer, but easier to read:
```js
let user = 'John';
let age = 25;
let message = 'Hello';
```
Some people also define multiple variables in this multiline style:
```js
let user = 'John',
  age = 25,
  message = 'Hello';
```
…Or even in the “comma-first” style:
```js
let user = 'John'
  , age = 25
  , message = 'Hello';
```
## Real World Example
We can easily grasp the concept of a “variable” if we imagine it as a “box” for data, with a uniquely-named sticker on it.

For instance, the variable message can be imagined as a box labeled "message" with the value "Hello!" in it:

![Variable Box](https://javascript.info/article/variables/variable.svg)

We can put any value in the box.

We can also change it as many times as we want:
```js
let message;

message = 'Hello!';

message = 'World!'; // value changed

alert(message);
```
When the value is changed, the old data is removed from the variable:

![Variable Box 2](https://javascript.info/article/variables/variable-change.svg)

We can also declare two variables and copy data from one into the other.
```js
let hello = 'Hello world!';

let message;

// copy 'Hello world' from hello into message
message = hello;

// now two variables hold the same data
alert(hello); // Hello world!
alert(message); // Hello world!
```

## Task
### Working with variables
    Declare two variables: admin and name.
    Assign the value "John" to name.
    Copy the value from name to admin.
    Show the value of admin using alert (must output “John”).

## Data types
A variable in JavaScript can contain any data. A variable can at one moment be a string and at another be a number:
```js
// no error
let message = "hello";
message = 123456;
```
Programming languages that allow such things are called<strong> “dynamically typed”</strong>, meaning that there are data types, but variables are not bound to any of them.

There are seven basic data types in JavaScript. Here, we’ll cover them in general and in the next chapters we’ll talk about each of them in detail.

### A number
```ja
let n = 123;
n = 12.345;
```
The number type represents both integer and floating point numbers.

There are many operations for numbers, e.g. multiplication *, division /, addition +, subtraction -, and so on.

### Mathematical operations are safe

Doing maths is “safe” in JavaScript. We can do anything: divide by zero, treat non-numeric strings as numbers, etc.

The script will never stop with a fatal error (“die”). At worst, we’ll get NaN as the result.

Special numeric values formally belong to the “number” type. Of course they are not numbers in the common sense of this word.

We’ll see more about working with numbers in the chapter Numbers.

### A string

A string in JavaScript must be surrounded by quotes.
```js
let str = "Hello";
let str2 = 'Single quotes are ok too';
let phrase = `can embed ${str}`;
```
In JavaScript, there are 3 types of quotes.
```js
    Double quotes: "Hello".
    Single quotes: 'Hello'.
    Backticks: `Hello`.
```
Double and single quotes are “simple” quotes. There’s no difference between them in JavaScript.
```js                
let name = "John";

// embed a variable
alert( `Hello, ${name}!` ); // Hello, John!

// embed an expression
alert( `the result is ${1 + 2}` ); // the result is 3
```
The expression inside ```${…}``` is evaluated and the result becomes a part of the string. We can put anything in there: a variable like name or an arithmetical expression like 1 + 2 or something more complex.

Please note that this can only be done in backticks. Other quotes don’t have this embedding functionality!
```js
alert( "the result is ${1 + 2}" ); // the result is ${1 + 2} (double quotes do nothing)
```
### A boolean (logical type)

The boolean type has only two values: ```true and false.```

This type is commonly used to store yes/no values: true means “yes, correct”, and false means “no, incorrect”.

For instance:
```js
let nameFieldChecked = true; // yes, name field is checked
let ageFieldChecked = false; // no, age field is not checked

Boolean values also come as a result of comparisons:

let isGreater = 4 > 1;

alert( isGreater ); // true (the comparison result is "yes")
```

### The “null” value

The special null value does not belong to any of the types described above.

It forms a separate type of its own which contains only the null value:
```js
let age = null;
```
It’s just a special value which represents “nothing”, “empty” or “value unknown”.

The code above states that age is unknown or empty for some reason.

### Backticks
Backticks embed the expression inside ```${...}``` into the string.
```js
let name = "Ilya";

// the expression is a number 1
alert( `hello ${1}` ); // hello 1

// the expression is a string "name"
alert( `hello ${"name"}` ); // hello name

// the expression is a variable, embed it
alert( `hello ${name}` ); // hello Ilya
```

## Type Conversions
There are also cases when we need to explicitly convert a value to the expected type.

### ToString

String conversion happens when we need the string form of a value.

For example, alert(value) does it to show the value.

We can also call the ```String(value)``` function to convert a value to a string:
```js
let value = true;
alert(typeof value); // boolean

value = String(value); // now value is a string "true"
alert(typeof value); // string
```
String conversion is mostly obvious. A false becomes "false", null becomes "null", etc.

### ToNumber

Numeric conversion happens in mathematical functions and expressions automatically.

For example, when division / is applied to non-numbers:
```js
alert( "6" / "2" ); // 3, strings are converted to numbers
```
We can use the Number(value) function to explicitly convert a value to a number:
```js
let str = "123";
alert(typeof str); // string

let num = Number(str); // becomes a number 123

alert(typeof num); // number
```

### ToBoolean

Boolean conversion is the simplest one.

It happens in logical operations (later we’ll meet condition tests and other similar things) but can also be performed explicitly with a call to Boolean(value).

The conversion rule:

    Values that are intuitively “empty”, like 0, an empty string, null, undefined, and NaN, become false.
    Other values become true.

For instance:
```js
alert( Boolean(1) ); // true
alert( Boolean(0) ); // false

alert( Boolean("hello") ); // true
alert( Boolean("") ); // false
```

There are 3 browser-specific functions to interact with visitors:
  - alert
        shows a message.
  - prompt
        shows a message asking the user to input text. It returns the text or, if Cancel button or Esc is clicked, null.
  - confirm
        shows a message and waits for the user to press “OK” or “Cancel”. It returns true for OK and false for Cancel/Esc.

All these methods are modal: they pause script execution and don’t allow the visitor to interact with the rest of the page until the window has been dismissed.

There are two limitations shared by all the methods above:

    The exact location of the modal window is determined by the browser. Usually, it’s in the center.
    The exact look of the window also depends on the browser. We can’t modify it.
 
### Task
### A simple page:
    Create a web-page that asks for a name and outputs it.
    
    Solution:
    let name = prompt("What is your name?", "");
    alert(name);

    The full page:

    <!DOCTYPE html>
    <html>
    <body>

      <script>
        'use strict';

        let name = prompt("What is your name?", "");
        alert(name);
      </script>

    </body>
    </html>
    
 ## Control Structures
 ### The “if” statement

The if(...) statement evaluates a condition in parentheses and, if the result is true, executes a block of code.

For example:
```js
let year = prompt('In which year was ECMAScript-2015 specification published?', '');

if (year == 2015)
alert( 'You are right!' );
```

In the example above, the condition is a simple equality check (year == 2015), but it can be much more complex.

If we want to <strong>execute more than one statement</strong>, we have to wrap our code block inside curly braces:
```js
if (year == 2015) {
  alert( "That's correct!" );
  alert( "You're so smart!" );
}
```
We recommend wrapping your code block with curly braces ```{}``` every time you use an if statement, even if there is only one statement to execute. Doing so improves readability.

### The “else” clause

The if statement may contain an optional “else” block. It executes when the condition is false.

For example:
```js
let year = prompt('In which year was the ECMAScript-2015 specification published?', '');

if (year == 2015) {
  alert( 'You guessed it right!' );
} else {
  alert( 'How can you be so wrong?' ); // any value except 2015
}
```
Several conditions: “else if”

Sometimes, we’d like to test several variants of a condition. The else if clause lets us do that.

For example:
```js
let year = prompt('In which year was the ECMAScript-2015 specification published?', '');

if (year < 2015) {
  alert( 'Too early...' );
} else if (year > 2015) {
  alert( 'Too late' );
} else {
  alert( 'Exactly!' );
}
```
In the code above, JavaScript first checks ```year < 2015```. If that is falsy, it goes to the next condition ```year > 2015```. If that is also falsy, it shows the last alert.

There can be more else if blocks. The final else is optional.
