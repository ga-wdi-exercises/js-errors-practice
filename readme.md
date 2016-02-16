# JS Errors Practice

In the spaces below, write code that would produce the corresponding error message. Each of these errors could be caused by any number of different code combinations; just write the first you find.

The prompts get progressively more difficult. 

You can edit the `<script>` element of the enclosed [index.html](./index.html) as your scratch pad.

**Hint:** In a few of the spaces below, rather than just putting stuff inside the `<script>` tags you may need to edit the tags themselves.

1. `Uncaught SyntaxError: Unexpected token {`
  ```html
  <script>
  function hello(){
  </script>
  ```
  > Missing a `}`

- `Uncaught ReferenceError: greeting is not defined`
  ```html
  <script>
  alert(greeting);
  </script>
  ```
  > Need `var greeting` somewhere

- `GET file:///scripts.js net::ERR_FILE_NOT_FOUND`
  ```html
  <script src="/scripts.js"></script>
  ```
  > The file doesn't exist

- `GET http://maxcdn.com/bootstrap.css 400 (Not Found)`
  ```html
  <script src="http://maxcdn.com/bootstrap.css"></script>
  ```
  > The URL doesn't exist

- `Uncaught TypeError: "hello".push is not a function`
  ```html
  <script>
  "hello".push("world");
  </script>
  ```
  > `.push` is an array method, not a string method

- `Uncaught TypeError: this.greet is not a function`
  ```html
  <script>
  this.greet();
  </script>
  ```
  > `this` is the `Window`, and the `Window` doesn't have a method called `greet`

- `Uncaught TypeError: Cannot read property 'name' of undefined`
  ```html
  <script>
  var bob;
  console.log(bob.name);
  </script>
  ```
  > `bob` doesn't have a value

- `Uncaught SyntaxError: Unexpected token ILLEGAL`
  ```html
  <script>
  console.log("hello
  </script>
  ```
  > Missing a closing `")`

- `Uncaught SyntaxError: missing ) after argument list`
  ```html
  <script>
  console.log("hello"
  </script>
  ```
  > Missing a closing `)`

- `Uncaught ReferenceError: Invalid left-hand side in assignment`
  ```html
  <script>
  42 = "the answer";
  </script>
  ```
  > You can't change the value of `42`

- `Uncaught SyntaxError: Unexpected number`
  ```html
  <script>
  var 42 = "the answer";
  </script>
  ```
  > You can't use numbers as variable names

- `Uncaught SyntaxError: Unexpected string`
  ```html
  <script>
  var myArray = ["a" "b" "c"];
  </script>
  ```
  > Items in arrays must be separated by commas

- `Uncaught SyntaxError: Unexpected identifier`
  ```html
  <script>
  var me = {name: "Robin" age: 47}
  </script>
  ```
  > Pairs in objects must be separated by commas

- `Uncaught SyntaxError: Unterminated template literal`
  ```html
  <script>
  var name = "Jimmy Bob";`
  </script>
  ```
  > There's a trailing `` ` ``. This happens all the time when copying stuff from Slack.

- `Uncaught RangeError: Maximum call stack size exceeded`
  ```html
  <script>
  function recursion(){
    recursion();
  }
  recursion();
  </script>
  ```
  > The function calls itself, which calls itself... until it has called itself an infinite number of times.

