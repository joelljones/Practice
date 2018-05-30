# Make a Website

## Table of Contents

- [Site Structure](#site-structure)
- [A Closer Look at CSS](#a-closer-look-at-css)
- [Boundaries and Space](#boundaries-and-space)
- [Building with bootstrap](#building-with-bootstrap)

---

# Site Structure

__LANGUAGES__

- __html__: stands for _hypertext markup language_, and is used to give a webpage structure.

- __css__: stands for _cascading style sheets_, and is used to style HTML elements.

__HTML ELEMENTS__

- _h1 - h6_: indicate text headings on a webpage. h1 is the largest heading; h6 is the smallest.

  `<h1>Heading</h1>`

- _p_: used for non-heading text, such as the bodies of articles or company descriptions.

    `<p>Description of company here.</p>`

- _a_: short for anchor and used to add links to other webpages. Anchor elements typically have an href attribute:

    `<a href="http://codecademy.com">Click here</a> to learn how to make a website!`

- _img_: used to add an image to a webpage. Image elements are _self-closing_ and do not require a closing tag:

    `<img src="https://images.com/favorite.png">`

- _video_: used to add videos to a webpage, and uses multiple attributes and a nested source element:

  ```html
  <video width="320" height="240" controls>
      <source src="https://movies.io/great-clip.mp4" type="video/mp4">
  </video>
  ```

- _unordered list_: used to create lists on a webpage and requires li elements inside a ul:

  ```html
  <ul>
      <li>list item</li>
      <li>another item</li>
      <li>yet another</li>
  </ul>
  ```

- _div_: used to organize HTML elements into different groups, which can be given a class attribute:

  ```html
  <div class="main">
      <h2>Subheading!</h2>
  </div>
  ```

- _metadata tags_: provide metadata about a webpage.

__WEB CONCEPTS__

- __parent/child elements__: used to describe HTML elements that enclose or are enclosed by other elements. For example, below the ul is the parent and the li items are children:

  ```html
  <ul>
      <li>...</li>
      <li>...</li>
      <li>...</li>
  </ul>
  ```

# A Closer Look at CSS

__WEB CONCEPTS__

- _CSS_: Language used to style websites. Colors, fonts, and page layouts for a site are managed using CSS.

- _CSS Selectors_: specifies exactly which HTML elements to style

  - _class selectors_: used to target classes of HTML elements

  - _id selectors_: used to style an HTML element which has an id attribute.

- _External Stylesheet_: CSS file that styles an HTML file externally via the HTML `link` element.

__CSS PROPERTIES__

- _font-family_: sets font for a CSS selector.

- _color_: sets font color for the CSS selector.

- _font-size_: sets font size for text.

- _background-image_: sets a background image of your choosing for a given selector.

# Boundaries and Space

__WEB CONCEPTS__

- _CSS Box Model_: illustrates the space and boundary properties of an HTML element that can be controlled using CSS.

__CSS SKILLS__

- _border_: sets the outline of an HTML page element, like a picture frame that contains the element.

- _padding_: sets the amount of space between an element's content and its border.

- _margin_: sets the amount of space between an HTML element and the next nearest element(s).

- _display_: property that determines how the selected element will be arranged in relation to other HTML elements on the page.

- _inline_: display value used to arrange HTML elements on the same line as neighboring elements.

- _flex_: display value that allows us to easily align multiple page elements vertically or horizontally.

- _float_: property used to float HTML elements left or right of neighboring elements.

- _position_: property used to position HTML elements in exact locations on a webpage.

# Building with Bootstrap

__WEB CONCEPTS__

- _CSS Framework_: Set of prewritten CSS rules designed to help you build webpages faster.

- _Bootstrap Grid_: 12 equal-sized columns which can be utilized via Bootstrap classes to build responsive page layouts quickly and reliably.

__BOOTSTRAP CLASSES__

- _row_: Arranges HTML elements in rows, and can be useful when building headers/navigation menus, main feature sections, supporting content sections and footers.

- _jumbotron_: Used to create large showcase sections featuring important content.

- _col-sm-*_: Used to span a specified number of columns on the Bootstrap grid. The "sm" is short for "small", and maintains desired CSS layouts on small screens (tablet-sized).

- _text-right_: Bootstrap class used to orient text to the right side of the webpage.

- _btn btn-primary_: Bootstrap class used to style page elements as buttons.
