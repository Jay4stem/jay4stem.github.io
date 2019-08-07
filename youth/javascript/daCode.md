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

## Task
### Show the sign

Using if..else, write the code which gets a number via prompt and then shows in alert:

    1, if the value is greater than zero,
    -1, if less than zero,
    0, if equals zero.

In this task we assume that the input is always a number.

### Solution:
      let value = prompt('Type a number', 0);

      if (value > 0) {
        alert( 1 );
      } else if (value < 0) {
        alert( -1 );
      } else {
        alert( 0 );
      }
      
### || (OR)

The “OR” operator is represented with two vertical line symbols:
```js
result = a || b;
```
In classical programming, the logical OR is meant to manipulate boolean values only. If any of its arguments are true, it returns true, otherwise it returns false.

In JavaScript, the operator is a little bit trickier and more powerful. But first, let’s see what happens with boolean values.

There are four possible logical combinations:
```js
alert( true || true );   // true
alert( false || true );  // true
alert( true || false );  // true
alert( false || false ); // false
```
As we can see, the result is always true except for the case when both operands are false.

If an operand is not a boolean, it’s converted to a boolean for the evaluation.

For instance, the number 1 is treated as true, the number 0 as false:
```js
if (1 || 0) { // works just like if( true || false )
  alert( 'truthy!' );
}
```
Most of the time, OR || is used in an if statement to test if any of the given conditions is true.

For example:
```js
let hour = 9;

if (hour < 10 || hour > 18) {
  alert( 'The office is closed.' );
}
```
We can pass more conditions:
```js
let hour = 12;
let isWeekend = true;

if (hour < 10 || hour > 18 || isWeekend) {
  alert( 'The office is closed.' ); // it is the weekend
}
```

### && (AND)

The ```AND``` operator is represented with two ampersands``` &&```:
```js
result = a && b;
```
In classical programming, AND returns true if both operands are truthy and false otherwise:
```js
alert( true && true );   // true
alert( false && true );  // false
alert( true && false );  // false
alert( false && false ); // false
```
An example with if:
```js
let hour = 12;
let minute = 30;

if (hour == 12 && minute == 30) {
  alert( 'The time is 12:30' );
}
```
Just as with OR, any value is allowed as an operand of AND:
```js
if (1 && 0) { // evaluated as true && false
  alert( "won't work, because the result is falsy" );
}
```

### ! (NOT)

The boolean NOT operator is represented with an exclamation sign !.

The syntax is pretty simple:
```js
result = !value;
```
The operator accepts a single argument and does the following:

    Converts the operand to boolean type: true/false.
    Returns the inverse value.

For instance:
```js
alert( !true ); // false
alert( !0 ); // true
```
A double NOT !! is sometimes used for converting a value to boolean type:
```js
alert( !!"non-empty string" ); // true
alert( !!null ); // false
```
That is, the first NOT converts the value to boolean and returns the inverse, and the second NOT inverses it again. In the end, we have a plain value-to-boolean conversion.

There’s a little more verbose way to do the same thing – a built-in Boolean function:
```js
alert( Boolean("non-empty string") ); // true
alert( Boolean(null) ); // false
```
The precedence of ```NOT ! ```is the highest of all logical operators, so it always executes first, before``` && or ||```.

## Tasks
### Check the range between

Write an “if” condition to check that age is between 14 and 90 inclusively.

“Inclusively” means that age can reach the edges 14 or 90.

### Check the range outside

Write an if condition to check that age is <b>NOT</b> between 14 and 90 inclusively.

     Create two variants: the first one using NOT !, the second one – without it.
     
## Loops: while and for

We often need to repeat actions.

For example, outputting goods from a list one after another or just running the same code for each number from 1 to 10.

Loops are a way to repeat the same code multiple times.
### The “while” loop

The while loop has the following syntax:
```js
while (condition) {
  // code
  // so-called "loop body"
}
```
While the condition is truthy, the code from the loop body is executed.

For instance, the loop below outputs i while i < 3:
```js
let i = 0;
while (i < 3) { // shows 0, then 1, then 2
  alert( i );
  i++;
}
```
A single execution of the loop body is called an iteration. The loop in the example above makes three iterations.
```js
let i = 3;
while (i) { // when i becomes 0, the condition becomes falsy, and the loop stops
  alert( i );
  i--;
}
```
Curly braces are not required for a single-line body

If the loop body has a single statement, we can omit the curly braces {…}:
```js
let i = 3;
while (i) alert(i--);
```
### The “do…while” loop

The condition check can be moved below the loop body using the do..while syntax:
```js
do {
  // loop body
} while (condition);
```
The loop will first execute the body, then check the condition, and, while it’s truthy, execute it again and again.

For example:
```js
let i = 0;
do {
  alert( i );
  i++;
} while (i < 3);
```
This form of syntax should only be used when you want the body of the loop to execute at least once regardless of the condition being truthy. Usually, the other form is preferred: while(…) {…}.
### The “for” loop

The for loop is more complex, but it’s also the most commonly used loop.

It looks like this:
```js
for (begin; condition; step) {
  // ... loop body ...
}
```
Let’s learn the meaning of these parts by example. The loop below runs alert(i) for i from 0 up to (but not including) 3:
```js
for (let i = 0; i < 3; i++) { // shows 0, then 1, then 2
  alert(i);
}
```

## Loops: while and for

We often need to repeat actions.

For example, outputting goods from a list one after another or just running the same code for each number from 1 to 10.

Loops are a way to repeat the same code multiple times.
### The “while” loop

The while loop has the following syntax:
```js
while (condition) {
  // code
  // so-called "loop body"
}
```
While the condition is truthy, the code from the loop body is executed.

For instance, the loop below outputs i while i < 3:
```js
let i = 0;
while (i < 3) { // shows 0, then 1, then 2
  alert( i );
  i++;
}
```
A single execution of the loop body is called an iteration. The loop in the example above makes three iterations.
```js
let i = 3;
while (i) { // when i becomes 0, the condition becomes falsy, and the loop stops
  alert( i );
  i--;
}
```
Curly braces are not required for a single-line body

If the loop body has a single statement, we can omit the curly braces {…}:
```js
let i = 3;
while (i) alert(i--);
```
### The “do…while” loop

The condition check can be moved below the loop body using the do..while syntax:
```js
do {
  // loop body
} while (condition);
```
The loop will first execute the body, then check the condition, and, while it’s truthy, execute it again and again.

For example:
```js
let i = 0;
do {
  alert( i );
  i++;
} while (i < 3);
```
This form of syntax should only be used when you want the body of the loop to execute at least once regardless of the condition being truthy. Usually, the other form is preferred: while(…) {…}.
### The “for” loop

The for loop is more complex, but it’s also the most commonly used loop.

It looks like this:
```js
for (begin; condition; step) {
  // ... loop body ...
}
```
Let’s learn the meaning of these parts by example. The loop below runs alert(i) for i from 0 up to (but not including) 3:
```js
for (let i = 0; i < 3; i++) { // shows 0, then 1, then 2
  alert(i);
}
```

### Class Example:
Which values get shown by the "for" loop?
importance: 4

For each loop write down which values it is going to show. Then compare with the answer.

Both loops alert same values or not?

    The postfix form:
```js
    for (let i = 0; i < 5; i++) alert( i );
```
The prefix form:
```js
for (let i = 0; i < 5; ++i) alert( i );
```
## Task
### Sum numbers from the visitor:
    Create a script that prompts the visitor to enter two numbers and then shows their sum.
