# CSS

__Cascading Style Sheets (CSS)__ is a style sheet language used for describing the presentation of a document written in a markup language. Although most often used to set the visual style of web pages and user interfaces written in HTML and XHTML, the language can be applied to any XML document.

CSS is designed primarily to enable the separation of presentation and content, including aspects such as the layout, colors, and fonts. This separation can improve content accessibility, provide more flexibility and control in the specification of presentation characteristics, enable multiple HTML pages to share formatting by specifying the relevant CSS in a separate .css file, and reduce complexity and repetition in the structural content.

Separation of formatting and content makes it possible to present the same markup page in different styles for different rendering methods, such as on-screen, in print, by voice (via speech-based browser or screen reader), and on Braille-based tactile devices. It can also display the web page differently depending on the screen size or viewing device. Readers can also specify a different style sheet, such as a CSS file stored on their own computer, to override the one the author specified.

Changes to the graphic design of a document (or hundreds of documents) can be applied quickly and easily, by editing a few lines in the CSS file they use, rather than by changing markup in the documents.

The CSS specification describes a priority scheme to determine which style rules apply if more than one rule matches against a particular element. In this so-called cascade, priorities (or weights) are calculated and assigned to rules, so that the results are predictable.

The CSS specifications are maintained by the World Wide Web Consortium (W3C).

## Table of Contents

- [CSS Setup](#css-setup)
- [CSS Selectors](#css-selectors)
- [CSS Visual Rules](#css-visual-rules)
- [The Box Model](#the-box-model)
- [Changing the Box Model](#changing-the-box-model)
- [Display and Positioning](#display-and-positioning)
- [CSS - Color](#css-color)
- [CSS - Typography](#css-typography)
- [Pseudo-classes](#pseudo-classes)
- [Animations - Transitions](#animations-transitions)

### Resources

- [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS)
- [W3Schools](https://w3schools.com/css)
- [W3C](https://www.w3.org/Style/CSS)
- [Chrome DevTools](https://developer.chrome.com/devtools)
- [Reference of web safe fonts](https://cssfontstack.com)
- [Paletton](http://paletton.com)
- [Adobe Color CC](http://color.adobe.com)
- [Color blindness](http://colourblindawareness.org/colour-blindness)
- [Color Laboratory](http://colorlab.wickline.org/colorblind/colorlab)
- [Google Fonts](https://fonts.google.com)
- [Font Squirrel](https://fontsquirrel.com)
- [Adobe Typekit](https://typekit.com)
- [dafont](http://dafont.com)
- [Typewolf](https://typewolf.com/google-fonts)
- [Google Font Combinations](https://behance.net/gallery/35768979/Typography-Google-Fonts-Combinations)
- [Hand-picked Tales from Æsop's Fables with Hand-picked Type from Google Fonts](https://femmebot.github.io/google-type)

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

  `h1.special {}`

- Nested elements can be selected by separating selectors with a space:

  `.main p {}`

- The `!important` flag will override any style, however it should almost never be used, as it is extremely difficult to override.

  `color: blue !important;`

- Multiple unrelated selectors can receive the same styles by separating the selector names with commas:

  `h1, .menu {}`

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

# The Box Model

1. The box model comprises a set of properties used to create space around and between HTML elements.

2. The height and width of a content area can be set in pixels or percentage.

3. Borders surround the content area and padding of an element. The color, style, and thickness of a border can be set with CSS properties.

4. Padding is the space between the content area and the border. It can be set in pixels or percent.

5. Margin is the amount of spacing outside of an element's border.

6. Horizontal margins add, so the total space between the borders of adjacent elements is equal to the sum of the right margin of one element and the left margin of the adjacent element.

7. Vertical margins collapse, so the space between vertically adjacent elements is equal to the larger margin.

8. `margin: 0 auto` horizontally centers an element inside of its parent content area, if it has a width.

9. The `overflow` property can be set to `display`, `hide`, or `scroll`, and dictates how HTML will render content that overflows its parent's content area.

10. The `visibility` property can hide or show elements.

# Changing the Box Model

1. In the default box model, box dimensions are affected by border thickness and padding.

2. The `box-sizing` property controls the box model used by the browser.

3. The default value of the `box-sizing` property is `content-box`.

4. The value for the new box model is `border-box`.

5. The `border-box` model is not affected by border thickness or padding.

# CSS Display and Positioning

1. The default positioning of elements is based on the _flow_ of the HTML file.

2. The `display` property allows you control how an element flows vertically and horizontally a document.

3. `display: inline` elements appear next to each other on the same line.

    - The default display for some tags, such as `<em>`, `<strong>`, and `<a>`.
    - take up as little space as possible, and they cannot have manually-adjusted `width` or `height`.

4. You can position elements to be displayed on their own line using `display: block`.

    - Elements that are block-level by default include all levels of heading elements (`<h1>` through `<h6>`), `<p>`, `<div>` and `<footer>`.

    - take up the width of their container and can have manually-adjusted `height`s.

5. `display: inline-block` elements are on the same line as each other and their size can be set.

6. The `position` property allows you to specify the position of an element in three different ways.

7. The default positioning for any element is `position: static` which means it will appear exactly as it does in the flow of the HTML document.

8. When set to `relative`, an element's position is relative to its default position on the page.

9. When set to `absolute`, an element's position is relative to its closest positioned parent element. It can be pinned to any part of the web page, but the element will still move with the rest of the document when the page is scrolled.

10. When set to `fixed`, an element's position can be pinned to any part of the web page. The element will remain in view no matter what.

11. The `z-index` of an element specifies how far back or how far forward an element appears on the page when it overlaps other elements.

12. The `float` property can move elements as far left or as far right as possible on a web page.

13. You can clear an element's left or right side (or both) using the `clear` property.

# CSS Color

There are four ways to represent color in CSS:

- Named colors — there are 147 named colors.

- Hexadecimal or hex colors

  - Hexadecimal is a number system with has sixteen digits, 0 to 9 followed by "A" to "F".

  - Hex values always begin with `#` and specify values of red, blue and green using hexademical numbers such as `#23F41A`.

- RGB

  - RGB colors use the `rgb()` syntax with one value for red, one value for blue and one value for green.

  - RGB values range from 0 to 255 and look like this: `rgb(7, 210, 50)`.

- HSL

  - HSL stands for hue (the color itself), saturation (the intensity of the color), and lightness (how light or dark a color is).

  - Hue ranges from 0 to 360 and saturation and lightness are both represented as percentages like this: `hsl(200, 20%, 50%)`.

- You can add opacity to color in RGB and HSL by adding a fourth value, `a`, which is represented as a percentage.

# CSS - Typography

- _Typography_ is the art of arranging text on a page.

- Text can appear in any number of weights, with the `font-weight` property.

  1. `400` is the default `font-weight` of most text.
  2. `700` signifies a bold `font-weight`.
  3. `300` signifies a light `font-weight`.

- Text can appear in italics with the `font-style` property.

- The vertical spacing between lines of text can be modified with the `line-height` property:

  1. A unitless number, such as `1.2`. This number is an absolute value that will compute the line height as a ratio of the font size.
  2. A number specified by unit, such as `12px`. This number can be any valid CSS unit, such as pixels, percents, ems, or rems.

- _Serif_ fonts have extra details on the ends of each letter. _Sans-Serif_ fonts do not.

- _Fallback fonts_ are used when a certain font is not installed on a user's computer.

- [Google Fonts](https://fonts.google.com) provides free fonts that can be used in an HTML file with the `<link>` tag or the `@font-face` property.

- Local fonts can be added to a document with the `@font-face` property and the path to the font's source.

- The `word-spacing` property changes how far apart individual words are.

- The `letter-spacing` property changes how far apart individual letters are.

- The `text-align` property changes where text horizontally on a page.

# Pseudo-classes

- _Pseudo-classes_ style elements based on user interactions and context within a web document.

- _Dynamic selectors_ style elements based on user interaction, and include `:link`, `:visited`, `:hover`, and `:active`.

- _Structural selectors_ style elements based on the location of their tags within an HTML document. These include `:first-child`, `:last-child`, and `:nth-child`.

  - `:nth-child(2n + 3)` selects every second, starting with the third.
  - `:nth-child(3n + 4)` selects every third, starting with the fourth.

# Animations - Transitions

CSS Transitions have 4 components:

- A _property_ that will transition.

- The _duration_ which describes how long the transition takes.

- The _delay_ to pause before the transition will take place.

- The _timing function_ that describes the transition's acceleration.

  - `ease` - starts the transition slowly, speeds up in the middle, and slows down again at the end
  - `ease-in` — starts slow, accelerates quickly, stops abruptly
  - `ease-out` — begins abruptly, slows down, and ends slowly
  - `ease-in-out` — starts slow, gets fast in the middle, and ends slowly
  - `linear` — constant speed throughout

A simple transition can be described with a property and a duration, which can be written like this:

```css
transition-property: color;
transition-duration: 1s;
```

Many properties' _state changes_ can be transitioned, including color, background color, font size, width, and height. `all` is also a valid transition property that causes every changing property to transition.

- `transition: all 1.5s linear 0.5s;`

The shorthand property `transition` can be used to describe all four components of a transition at once. By using the comma (`,`) operator, many transitions can be described in one CSS rule.

```css
transition: width 750ms ease-in 200ms,
            left 500ms ease-out 450ms;
```
