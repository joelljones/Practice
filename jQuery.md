# jQuery

jQuery, a popular framework for using JavaScript and selectors to make interactive websites. It is a JavaScript library that makes it easy to add dynamic behavior to HTML elements.

## Table of Contents

- [Introduction to jQuery](#introduction-to-jquery)

### Resources

- [jQuery](https://jquery.com)
- [jQuery api](https://api.jquery.com)
- [jQuery alternative](http://jqapi.com)
- [W3Schools](https://w3schools.com/jquery)
- [GitHub](https://github.com/jquery/jquery)

---

# Introduction to jQuery

- You can include jQuery in a project by using a local copy of the source code or an external link to the source code.

  ```JavaScript
  <script
    src="https://code.jquery.com/jquery-3.2.1.min.js" integrity="sha256-hwg4gsxgFZhOsEEamdOYGBf13FyQuiTwlAQgxVSNgt4=" crossorigin="anonymous"></script>
  ```

- jQuery is JavaScript code, so it is written inside of a __.js__ file.

- The `$(document).ready()` call is necessary to begin writing jQuery.

  ```JavaScript
  $(document).ready(function() {

  });
  ```

- jQuery can target any DOM element with the CSS selector for that DOM element.

- jQuery provides built-in methods that add animation to elements or modify existing properties of elements.

- jQuery methods can accept zero, one, or multiple arguments, depending on functionality. You can find this information in their documentation.

- Event handlers allow a web page to modify its behavior based on user interactions, like clicking, mousing over, and more.

- The `this` keyword targets only the DOM element that is being interacted with, whereas selectors will target all elements of that type.

- DOM elements can be navigated, or traversed, using jQuery DOM traversal methods. This is one way of updating many elements simultaneously.

- Methods can be chained together to link behaviors and interactivity.

- The `$.ajax()` method can make requests for information from URLs and APIs.

- Plugins are libraries that allow you to write less jQuery while increasing the functionality on a web page. They can target many web page aspects, like scrolling, displaying information, and more.

- The [jQuery Plugin Registry](https://plugins.jquery.com) has a list of all available plugins.
