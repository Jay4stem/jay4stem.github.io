### Hello World
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

### Variables

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
