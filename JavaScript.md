# JavaScript

JavaScript, a popular programming language used to make websites interactive, is one of the most popular languages in the world and is used on many websites. It is used on the web to create dynamic behavior, manage data, and automate repetitive tasks.


## Table of Contents

- [Introduction to JavaScript](#introduction-to-javascript)


### Resources

- [MDN JavaScript](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
- [W3Schools](https://w3schools.com/js)
- [Eloquent JavaScript](http://eloquentjavascript.net)
- [You Don't Know JS](https://github.com/getify/You-Dont-Know-JS)

---

# Introduction to JavaScript

- `//` single-line comment

- `console.log();` command is used to print, or log, text to the console

- A semicolon is used to mark the end of a statement.

- Variables can store any data type, including strings, numbers, and booleans.

  - `var` indicates the creation of a variable

- Mathematical expressions include the following operators: `+`, `-`, `*`, and `/`.

- A function is a block of code that performs a task.

  ```JavaScript
  function functionName() {
    // a set of instructions that will only execute when the function is called
  }

  functionName(); // To call a function, you need the function's name, a pair of parentheses, and a semicolon.
  ```

- Methods are functions that perform a task on an object.

- Comparison operators compare values and return a boolean value (`true` or `false`). The operators include: `>`, `<`, `>=`, `<=`, `===`, and `!==`.

- Logical operators combine multiple boolean expressions or values to provide a single boolean output. The operators include `&&` and `||`.

- Conditional statements (`if`, `else if`, and `else`) execute code if a set of conditions are met.

- Arrays are lists of JavaScript values.

- Arrays are zero-indexed. Each item can be accessed using bracket (`[]`) notation and its numeric position.

- `for` loops execute for a set number of iterations.

  ```JavaScript
  for (var i = 0; i < 3; i++) {
    console.log('log/print something');
  }
  ```

  1. Within the `for` loop's parentheses, the _start condition_ is `var i = 0`, which means the loop starts counting at `0`.
  1. The _stop condition_ is `i < 3`, which means the loop runs as long as `i` is less than `3`. When `i` is equal to `3`, the loop will stop.
  1. The _iterator_ is `i++`. This means that `i` increases by one after each loop — `i++` is equivalent to writing `i = i + 1;`.
  1. Finally, the code block inside the curly braces executes until the loop stops.

- `while` loops execute as long as a certain condition is met.

  ```JavaScript
  var count = 5;
  while (count < 10){
    console.log('log/print something');
    count++;
  }
  ```

- Objects are like arrays, but use strings as keys to access their contents instead of position indices. Functions that are associated with an object are called methods.

  ```JavaScript
  var scoreboard = {
    teamA: 'Code',
    teamB: 'Cademy',
    scoreA: 0,
    scoreB: 0,
    incrementScoreA: function () {
      scoreboard.scoreA++;
    },
    incrementScoreB: function(){
      scoreboard.scoreB++;
    }
  };
  ```
