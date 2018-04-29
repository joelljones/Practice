# jQuery

jQuery, a popular framework for using JavaScript and selectors to make interactive websites. It is a JavaScript library that makes it easy to add dynamic behavior to HTML elements.


## Table of Contents

- [Introduction to jQuery](#introduction-to-jquery)
- [jQuery Setup](#jquery-setup)
- [jQuery Effects](#jquery-effects)
- [Mouse Events](#mouse-events)
- [Style Methods](#style-methods)
- [Traversing the DOM](#traversing-the-dom)


### Resources

- [jQuery](https://jquery.com)
- [GitHub](https://github.com/jquery/jquery)
- [jQuery api](https://api.jquery.com)
- [jQuery alternative](http://jqapi.com)
- [W3Schools](https://w3schools.com/jquery)

---

# Introduction to jQuery

https://api.jquery.com  
http://jqapi.com

jQuery, a popular framework for using JavaScript and selectors to make interactive websites. It is a JavaScript library that makes it easy to add dynamic behavior to HTML elements.

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


# jQuery Setup

```JavaScript
$(function() {

  $('.someClass').on('click', () => {
    $('.someOtherClass').hide();
  });

});
```

OR

```JavaScript
$(document).ready(() => {

  $('.someClass').on('click', () => {
    $('.someOtherClass').hide();
  });

});
```

OR

```JavaScript
$(document).ready(() => {

  const $jQueryObject = $('.someClass');

  $jQueryObject.on('click', () => {
    $('.someOtherClass').hide();
  });

});
```


# jQuery Effects

These methods instantly hide or show elements on a web page:

- `.hide()`
- `.show()`
- `.toggle()`

These methods make elements disappear or appear over a given period of time:

- `.fadeOut()`
- `.fadeIn()`
- `.fadeToggle()`

These methods make elements slide up or down into place over a given period of time:

- `.slideUp()`
- `.slideDown()`
- `.slideToggle()`


# Mouse Events

- Event handlers are comprised of an event listener and a callback function. An event listener specifies the type of event that will be detected. The callback function executes when the event happens. Everything together is the event handler.

- An event listener is set up using the `.on()` method.

- The events listened for included: `'click'`, `'mouseenter'`, and `'mouseleave'`.

- `event.currentTarget` refer to the individual element that an event occurred on.


# Style Methods

- The `.css()` method can change style properties of an element.

- The `.css()` method can accept multiple styles at once if you pass it a JavaScript object as its argument.

- The `.animate()` method can change specific style properties over a period of time.

- The `.addClass()` will add a CSS class to an element, and the `.removeClass()` method will remove a CSS class.

- The `.toggleClass()` method will toggle a class on or off an element.


# Traversing the DOM

- `.children()` to target an element's child elements.

- `.siblings()` to target elements adjacent to an element.

- `.parent()` to target an element's parent.

- `.closest()` travels up the DOM tree from the current element to target the closest element with a given selector.

- `.next()` to target the element immediately following the selected element.

- `.prev()` to target the element that is immediately preceding the selected element.

- `.find()` to target descendant elements by some selector, ie- class, id, tag etc.

- In addition to these methods, there are even more, including `.prevUntil()`, `.nextUntil()` and others.
