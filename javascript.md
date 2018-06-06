# JavaScript

JavaScript, a popular programming language used to make websites interactive, is one of the most popular languages in the world and is used on many websites. It is used on the web to create dynamic behavior, manage data, and automate repetitive tasks.

## Table of Contents

- [Introduction to JavaScript](#introduction-to-javascript)
- [Variables](#variables)
- [Control Flow](#control-flow)
- [Functions](#functions)
- [Scope](#scope)
- [Arrays](#arrays)
- [Loops](#loops)
- [Iterators](#iterators)
- [Objects](#objects)
- [Classes](#classes)
- [Browser Compatibility and Transpilation](#browser-compatibility-and-transpilation)
- [Modules](#modules)
- [Requests](#requests)

### Resources

- [MDN JavaScript](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
- [W3Schools](https://w3schools.com/js)
- [Eloquent JavaScript](http://eloquentjavascript.net)
- [You Don't Know JS](https://github.com/getify/You-Dont-Know-JS)

---

# Introduction to JavaScript

JavaScript, a popular programming language used to make websites interactive, is one of the most popular languages in the world and is used on many websites. It is used on the web to create dynamic behavior, manage data, and automate repetitive tasks.

- Four essential data types in JavaScript include strings, numbers, booleans, and null.

- Data is printed, or logged, to the console with `console.log()`.

- Four built-in mathematical operators include `+`, `-`, `*`, and `/`.

- JavaScript associates certain properties with different data types.

- JavaScript has built-in methods for different data types.

- Libraries are collections of methods that can be called without an instance.

- You can write single-line comments with `//` and multi-line comments between `/*` and `*/`.

- A semicolon is used to mark the end of a statement.

# Variables

- Variables hold reusable data in a program.

- Variables can store any data type, including strings, numbers, and booleans.

  - `let` or `var` indicates the creation of a variable

- JavaScript will throw an error if you try to reassign `const` variables.

- You can reassign variables that you create with the `let` keyword.

- Unset variables store the primitive data type `undefined`.

- Mathematical assignment operators make it easy to calculate a new value and assign it to the same variable.

- The `+` operator is used to interpolate (combine) multiple strings.

- In JavaScript ES6, backticks and `${}` are used to interpolate values into a string.

- Special characters:

  - `\\` : \ (backslash)
  - `\"` : '' (double quote)
  - `\'` : ' (single quote)
  - `\n` : newline
  - `\t` : tab

# Control Flow

- `if`/`else` statements make binary decisions and execute different code based on conditions.

  - "If something is true, let's do option 1, or else, if it is false, let's do option 2."

- All conditions are evaluated to be truthy or falsy.

  ```JavaScript
  let variableOne = 'I Exist!';
  if (variableOne) {
  // This code will run because variableOne contains a truthy value.
  } else {
  // This code will not run because the first block ran.
  }
  ```

  - All variables that have been created and set are truthy (and will evaluate to true if they are the condition of a control flow statement) unless they contain one of the seven values listed below:

    - `false`
    - `0` and `-0`
    - `""` and `''` (empty strings)
    - `null`
    - `undefined`
    - `NaN` (Not a Number)
    - `document.all`

- We can add more conditional statements to `if`/`else` statements with `else if`.

- `switch` statements make complicated `if`/`else` statements easier to read and achieve the same result.

  ```JavaScript
  let groceryItem = 'papaya';

  switch (groceryItem) {
    case 'tomato':
      console.log('Tomatoes are $0.49');
      break;
    case 'lime':
      console.log('Limes are $1.49');
      break;
    case 'papaya':
      console.log('Papayas are $1.29');
      break;
    default:
      console.log('Invalid item');
  }
  ```

  1. The `switch` keyword initiates the statement and is followed by `( ... )`, which contains the condition that each `case` will compare to.

  2. Inside the block, `{ ... }`, there are `cases`. `case` is like the `else if` part of an `if`/`else if`/`else` statement.

  3. The program stops with the `break` keyword. This keyword will prevent the `switch` statement from executing any more of its code. Without adding `break` at the end of each case, the program will execute the code for all matching cases and the default code as well. This behavior is different from `if`/`else` conditional statements which execute only one block of code.

  4. At the end of each `switch` statement, there is a `default` condition. If none of the `cases` are true, then this code will run.

- The ternary operator (`?`) and a colon (`:`) allow us to refactor simple `if`/`else` statements.

  ```JavaScript
  isNightTime ? console.log('Turn on the lights!') : console.log('Turn off the lights!');
  ```

  1. `isNightTime ?` — the conditional statement followed by a question mark. This checks if `isNightTime` is truthy.

  2. `console.log ('Turn on the lights!')` — this code will be executed if the condition is truthy.

  3. `:` — a colon separates the two different blocks of code that can be executed.

  4. `console.log('Turn off the lights!');` — this code will be executed if the condition is falsy

- Comparison operators, including `<`, `>`, `<=`, and `>=` can compare two variables or values.

- After two values are compared, the conditional statement evaluates to `true` or `false`.

- The logical operator `&&` checks if both sides of a condition are truthy.

- The logical operator `||` checks if either side is truthy.

- The logical operator `!==` checks if the two sides are not equal.

- An exclamation mark (`!`) switches the truthiness / falsiness of the value of a variable.

- One equals symbol (`=`) is used to assign a value to a variable.

- Three equals symbols (`===`) are used to check if two variables are equal to each other.

# Functions

- _Functions_ are blocks of code written to perform a task.

  ```js
  function functionName() {
    // a set of instructions that will only execute when the function is called
  }

  functionName(); // To call a function, you need the function's name, a pair of parentheses, and a semicolon.
  ```

- Functions take data, perform a set of tasks on the data, and then return the result.

- We can define parameters to be used when calling the function.

- When calling a function, we can pass in _arguments_, which will set the function's parameters.

- _Parameters_ are variables in a function definition that represent data we can input into the function.

- We can use `return` to return the result of a function which allows us to call functions anywhere, even inside other functions.

- A _function declaration_ is a function that is bound to an identifier or name.

  - require the keyword function, a name, and a function body.

  - You can identify this by the use of `function name()` and the `{}` below.

  - do not end in a semi-colon.

  ```js
  function name (parameter) {
    return parameter * parameter;
  }
  ```

- A _function expression_ is similar to function declaration, with the exception that the identifier can be omitted, creating an anonymous function.

  - often stored in a variable

  - can be identified by the absence of a function name immediately trailing the function keyword

  - end with a semi-colon since they are stored in a variable

  ```js
  const name = function (parameter) {
    return parameter * parameter;
  };
  ```

- _arrow function_ syntax - variable is set equal `=` to a set of parentheses followed by an arrow token `() =>`, indicating the variable stores a function

  ```js
  const name = (parameter) => {
    return parameter * parameter;
  };
  ```

- The most condensed form of the function is known as _concise body_.

  1. Functions that take a single parameter should not use parentheses.

  2. A function composed of a sole single-line block is automatically returned. The contents of the block should immediately follow the arrow `=>` and the `return` keyword can be removed. This is referred to as _implicit return_.

  3. A function composed of a sole single-line block does not need brackets.

  ```js
  const name = parameter => functionBlock;
  ```

# Scope

- _Scope_ is the idea in programming that some variables are accessible/inaccessible from other parts of the program.

- _Global Scope_ refers to variables that are accessible to every part of the program.

- _Block Scope_ refers to variables that are accessible only within the block they are defined.

  - A _block_ refers to the `{}` braces of a function, a loop, or an `if` statement, and serves as an important structural marker for our code.

# Arrays

- Arrays are lists and are a way to store data in JavaScript.

- Arrays are created with brackets `[]`.

- Each item inside of an array is at a numbered position, starting at `0`.

- We can access one item in an array using its numbered position, with syntax like: `myArray[0]`.

- We can also change an item in an array using its numbered position, with syntax like `myArray[0] = "new string";`

- Arrays have a `length` property, which allows you to see how many items are in an array.

- Arrays have their own methods, including `.push()` and `.pop()`, which add and remove items from an array, respectively.

- Arrays have many other methods that perform different functions, such as `.slice()` and `.shift()`. You can read the documentation for any array method on the [Mozilla Developer Network](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array) website.

- Variables that contain arrays can be declared with `let` or `const`. Even when declared with `const`, arrays are still mutable; they can be changed. However, a variable declared with `const` cannot be reassigned.

# Loops

- `for` loops allow us to repeat a block of code a known amount of times.

  ```js
  for (let i = 0; i < myArray.length; i++) {
    console.log(myArray[i]);
  }
  ```

  1. Within the `for` loop's parentheses, the _start condition_ is `var i = 0`, which means the loop starts counting at `0`.

  2. The _stop condition_ is `i < 3`, which means the loop runs as long as `i` is less than `3`. When `i` is equal to `3`, the loop will stop.

  3. The _iterator_ is `i++`. This means that `i` increases by one after each loop — `i++` is equivalent to writing `i = i + 1;`.

  4. Finally, the code block inside the curly braces executes until the loop stops.

- We can use a `for` loop inside another `for` loop to compare two lists.

  ```js
  for (let i = 0; i < myArray.length; i++) {
    for (let j = 0; j < yourArray.length; j++) {
      // code to run
     }
   }
  ```

- `while` loops are for looping over a code block an unknown amount of times.

  ```js
  while (condition) {
    // code block that loops until condition is false
  }
  ```

- Infinite loops occur when stop conditions are never met.

  ```js
  for (let i = 0; i < array.length; i--) {
     // some code
  }
  ```

# Iterators

https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array#Iteration_methods

- `.forEach()` is used to execute the same code on every element in an array but does not change the array and returns `undefined`.

- `.map()` executes the same code on every element in an array and returns a new array with the updated elements.

- `.filter()` checks every element in an array to see if it meets certain criteria and returns a new array with the elements that return truthy for the criteria.

- All iterator methods can be written using arrow function syntax. In fact, given the succinctness and the implicit return of arrow function syntax, this is quickly becoming the preferred way to write these types of method calls.

- Additional iterator methods such as `.some()`, `.every()`, `.reduce()` perform different functions.

# Objects

- Objects store key-value pairs and let us represent real-world things in JavaScript.

- Properties in objects are separated by commas. Key-value pairs are always separated by a colon.

  ```js
  let restaurant = {
    name: 'Italian Bistro',
    seatingCapacity: 120,
    hasDineInSpecial: true,
    entrees: ['Penne alla Bolognese', 'Chicken Cacciatore', 'Linguine Pesto'],
    incrementSeating: () => {
      restaurant.seatingCapacity++;
    },
    decrementSeating() {
      restaurant.seatingCapacity--;
    }
  };
  ```

- You can add or edit a property within an object with dot notation.

  ```js
  restaurant.desserts = ['Homemade Tiramisu', 'Canolli', 'Cheesecake'];
  ```

- A method is a function in an object.

  ```js
  openRestaurant: () => {
    return 'Unlock the door, flip the open sign. We are open for business!';
  },
  closeRestaurant() {
    return 'Lock the door, flip the open sign. We are closed.'
  };
  ```

- `this` helps us with scope inside of object methods. `this` is a dynamic variable that can change depending on the object that is calling the method.

- Getter and setter methods allow you to process data before accessing or setting property values.

  ```js
  set seatingCapacity(seatingCapacity) {
    if (typeOf newCapacity === 'number') {
      this._seatingCapacity = newCapacity;
    } else {
        console.log(`Change ${newCapacity} to a number.`)
    }
  },

  get seatingCapacity() {
    console.log(`There are ${this._seatingCapacity} seats at Italian Bistro.`);
    return this._seatingCapacity;
  };
  ```

# Classes

- _Classes_ are templates for objects.

- Javascript calls a _constructor_ method when we create a new instance of a class.

  ```js
  class Dog {
    constructor(name) {
      this.name = name;
      this.behavior = 0;
    }
  }
  ```

- _Inheritance_ is when we create a parent class with properties and methods that we can extend to child classes.

- We use the `extends` keyword to create a subclass.

- The `super` keyword calls the `constructor()` of a parent class.

  ```js
  class Cat extends Animal {
    constructor(name, usesLitter) {
      super(name);
      this._usesLitter = usesLitter;
    }
  }
  ```

- Static methods are called on the class, but not on instances of the class.

# Browser Compatibility and Transpilation

- ES5 — The old JavaScript version that is supported by all modern web browsers.

- ES6 — The new(er) JavaScript version that is not supported by all modern web browsers. The syntax is more readable, similar to other programming languages, and addresses the source of common bugs in ES5.

- [caniuse.com](caniuse.com) — a website you can use to look up HTML, CSS, and JavaScript browser compatibility information.

- Babel — A JavaScript package that transpiles JavaScript ES6+ code to ES5.

- `npm init` — A terminal command that creates a __package.json__ file.

- __package.json__ — A file that contains information about a JavaScript project.

- `npm install` — A command that installs Node packages.

- `babel-cli` — A Node package that contains command line tools for Babel.

- `babel-preset-env` — A Node package that contains ES6+ to ES5 syntax mapping information.

- __.babelrc__ — A file that specifies the version of the JavaScript source code.

- `"build"` script — A __package.json__ script that you use to tranpsile ES6+ code to ES5.

- `npm run build` — A command that runs the `build` script and transpiles ES6+ code to ES5.

---

$ npm init

$ npm install babel-cli -D

- The `-D` flag instructs npm to add each package to a property called `devDependencies` in __package.json.__

$ npm install babel-preset-env -D

- Once you `npm install` packages, you can find the Babel packages and all their dependencies in the __node_modules__ folder.

$ touch .babelrc

- Open __.babelrc__ and add:

  ```js
  {
    "presets": ["env"]
  }
  ```

Open __package.json__ and add below the "test" script: `"build": "babel src -d lib"`

- `babel` — The Babel command call responsible for transpiling code.
- `src` — Instructs Babel to transpile all JavaScript code inside the __src__ directory.
- `-d` — Instructs Babel to write the transpiled code to a directory.
- `lib` — Babel writes the transpiled code to a directory called `lib`.

$ npm run build

# Modules

_Modules_ in JavaScript are reusable pieces of code that can be exported from one program and imported for use in another program.

- `module.exports` exports the module for use in another program.
- `require()` imports the module for use in the current program.

ES6 introduced a more flexible, easier syntax to export modules:

- default exports use `export default` to export JavaScript objects, functions, and primitive data types.

- named exports use the `export` keyword to export data in variables.

- named exports can be aliased with the `as` keyword.

- `import` is a keyword that imports any object, function, or data type.

# Requests
