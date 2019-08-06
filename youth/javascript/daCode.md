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







                              



                      
let name = "John";

// embed a variable
alert( `Hello, ${name}!` ); // Hello, John!

// embed an expression
alert( `the result is ${1 + 2}` ); // the result is 3

The expression inside ${…} is evaluated and the result becomes a part of the string. We can put anything in there: a variable like name or an arithmetical expression like 1 + 2 or something more complex.

Please note that this can only be done in backticks. Other quotes don’t have this embedding functionality!

alert( "the result is ${1 + 2}" ); // the result is ${1 + 2} (double quotes do nothing)

We’ll cover strings more thoroughly in the chapter Strings.
There is no character type.

In some languages, there is a special “character” type for a single character. For example, in the C language and in Java it is char.

In JavaScript, there is no such type. There’s only one type: string. A string may consist of only one character or many of them.
A boolean (logical type)

The boolean type has only two values: true and false.

This type is commonly used to store yes/no values: true means “yes, correct”, and false means “no, incorrect”.

For instance:

let nameFieldChecked = true; // yes, name field is checked
let ageFieldChecked = false; // no, age field is not checked

Boolean values also come as a result of comparisons:

let isGreater = 4 > 1;

alert( isGreater ); // true (the comparison result is "yes")

We’ll cover booleans more deeply in the chapter Logical operators.
The “null” value

The special null value does not belong to any of the types described above.

It forms a separate type of its own which contains only the null value:

let age = null;

In JavaScript, null is not a “reference to a non-existing object” or a “null pointer” like in some other languages.

It’s just a special value which represents “nothing”, “empty” or “value unknown”.

The code above states that age is unknown or empty for some reason.
The “undefined” value

The special value undefined also stands apart. It makes a type of its own, just like null.

The meaning of undefined is “value is not assigned”.

If a variable is declared, but not assigned, then its value is undefined:

let x;

alert(x); // shows "undefined"

Technically, it is possible to assign undefined to any variable:

let x = 123;

x = undefined;

alert(x); // "undefined"

…But we don’t recommend doing that. Normally, we use null to assign an “empty” or “unknown” value to a variable, and we use undefined for checks like seeing if a variable has been assigned.
