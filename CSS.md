# CSS

summary...

## Table of Contents

- [CSS Setup](#css-setup)
- [CSS Selectors](#css-selectors)
- [CSS Visual Rules](#css-visual-rules)

### Resources

- []()

---

# CSS Setup

1. _CSS_, or Cascading Style Sheets, is a language that web developers use to _style_ the HTML content on a web page.

2. HTML and CSS are kept in separate files to keep code maintainable and readable, as well as keep structure separate from styling.

3. The `<style>` element allows you to write CSS code within the `<head>` element of an HTML file.

4. To style an HTML element, you can add the style attribute directly to the opening tag using _inline styles_:  

  `<p style="color: red;">This is an inline style</p>`

5. A CSS stylesheet can be linked to an HTML file using the `<link>` element, which requires three attributes:

  - `href` - set equal to the path of the CSS file
  - `type` - set equal to `text/css`
  - `rel` - set equal to `stylesheet`

  `<link href="style.css" type="text/css" rel="stylesheet">`

6. Comments are written in CSS using the following syntax: `/* comment */`.


# CSS Selectors

- CSS can change the look of HTML elements. In order to do this, CSS must select HTML elements, then apply styles to them.

- CSS can select HTML elements by tag, `.class`, or `#id`.

- Multiple CSS classes can be applied to one HTML element:

  `<h1 class="green bold"> ... </h1>`

- Classes can be reusable, while IDs can only be used once.

- IDs are more specific than classes, and classes are more specific than tags. That means IDs will override any styles from a class, and classes will override any styles from a tag selector.

- Multiple selectors can be chained together to select an element. This raises the specificity, but can be necessary.

  `h1.special {`

- Nested elements can be selected by separating selectors with a space:

  `.main p {`

- The `!important` flag will override any style, however it should almost never be used, as it is extremely difficult to override.

  `color: blue !important;`

- Multiple unrelated selectors can receive the same styles by separating the selector names with commas:

  `h1, .menu {`


# CSS Visual Rules

- CSS declarations are structured into _property_ and _value_ pairs:

  `color: blue;`

- The `font-family` property defines the typeface of an element.

  - `Times New Roman` is the default.
  - When the name of a typeface consists of more than one word, enclose the typeface's name in quotes: `"Courier New"`

- `font-size` controls the size of text displayed.

- `font-weight` defines how thin or thick text is displayed: `normal` or `bold`.

- The `align-text` property places text in the left, right, or center of its parent container.

- Text can have two different color attributes: `color` and `background-color`.

  - `color` defines the color of the text, while `background-color` defines the color behind the text.

- CSS can make an element transparent with the `opacity` (decimals) property.

- CSS can also set the background of an element to an image with the `background-image` property.
