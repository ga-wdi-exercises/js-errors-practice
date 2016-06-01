# JS Errors Practice

In the spaces below, **write code that would produce the corresponding error message.**

> Each of these errors could be caused by any number of different code combinations; just write the first you find.

Then, on the line below, **write an explanation of why your code causes this error**.

The prompts get progressively more difficult.

You can edit the `<script>` element of the enclosed [index.html](./index.html) as your scratch pad.

**Hint:** In a few of the spaces below, rather than just putting stuff inside the `<script>` tags you may need to edit the tags themselves.

#### `Uncaught SyntaxError: Unexpected token {`
  ```html
  <script>
  function hello(){
  </script>
  ```
  > Missing a `}`

#### `Uncaught ReferenceError: greeting is not defined`
  ```html
  <script>
  alert(greeting);
  </script>
  ```
  > Need `var greeting` somewhere

#### `GET file:///scripts.js net::ERR_FILE_NOT_FOUND`
  ```html
  <script src="/scripts.js"></script>
  ```
  > The file doesn't exist

#### `GET http://maxcdn.com/bootstrap.css 400 (Not Found)`
  ```html
  <script src="http://maxcdn.com/bootstrap.css"></script>
  ```
  > The URL doesn't exist

#### `Uncaught TypeError: "hello".push is not a function`
  ```html
  <script>
  "hello".push("world");
  </script>
  ```
  > `.push` is an array method, not a string method

#### `Uncaught TypeError: this.greet is not a function`
  ```html
  <script>
  this.greet();
  </script>
  ```
  > Whatever `this` is, it doesn't have a `greet` method

#### `Uncaught TypeError: Cannot read property 'name' of undefined`
  ```html
  <script>
  var bob;
  console.log(bob.name);
  </script>
  ```
  > `bob` has no value; it's undefined

#### `Uncaught SyntaxError: Unexpected token ILLEGAL`
  ```html
  <script>
  console.log("hello
  </script>
  ```
  > Missing a closing `")`

#### `Uncaught SyntaxError: missing ) after argument list`
  ```html
  <script>
  console.log("hello"
  </script>
  ```
  > Missing a closing `)`

#### `Uncaught ReferenceError: Invalid left-hand side in assignment`
  ```html
  <script>
  42 = "the answer";
  </script>
  ```
  > `42` is always `42`. You can't change its value.

#### `Uncaught SyntaxError: Unexpected number`
  ```html
  <script>
  var 42 = "the answer";
  </script>
  ```
  > Variable names cannot begin with numbers.

#### `Uncaught SyntaxError: Unexpected string`
  ```html
  <script>
  var myArray = ["a" "b" "c"];
  </script>
  ```
  > Items in arrays must be separated by commas.

#### `Uncaught SyntaxError: Unexpected identifier`
  ```html
  <script>
  var me = {name: "Robin" age: 47}
  </script>
  ```
  > Key/value pairs in objects must be separated by commas.

#### `Uncaught SyntaxError: Unterminated template literal`
  ```html
  <script>
  var name = "Jimmy Bob";`
  </script>
  ```
  > There's a trailing `` ` ``. Note: **This happens all the time when copying stuff from Slack.**

#### `Uncaught RangeError: Maximum call stack size exceeded`
  ```html
  <script>
  function recursion(){
    recursion();
  }
  recursion();
  </script>
  ```
  > The function calls itself, which calls itself... until it has called itself an infinite number of times.
