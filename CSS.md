# CSS

summary...

## Table of Contents

- [CSS Setup](#css-setup)
- [CSS Selectors](#css-selectors)
- [CSS Visual Rules](#css-visual-rules)
- [Display and Positioning](#display-and-positioning)
  - [The Box Model](#the-box-model)
  - [CSS Display](#css-display)
  - [Flexbox](#flexbox)
- [Design and UI Feedback](#design-and-ui-feedback)
  - [CSS - Color](#css-color)
  - [Design - Color](#design-color)
  - [CSS - Typography](#css-typography)
  - [Design - Typography](#design-typography)
  - [Pseudo-classes](#pseudo-classes)
  - [Animations - Transitions](#animations-transitions)
- [Responsive Design and Browser Compatibility](#responsive-design-and-browser-compatibility)
  - [Sizing Elements](#sizing-elements)
  - [Media Queries](#media-queries)
  - [Browser Compatibility](#browser-compatibility)
- [Icons, Assets and Accessibility](#icons-assets-and-accessibility)
  - [Font Awesome](#font-awesome)
  - [Managing Assets and Icons](#managing-assets-and-icons)
  - [Accessibility and ARIA](#accessibility-and-aria)

### Resources

- [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS)
- [Reference of web safe fonts](https://cssfontstack.com)
- [Chrome DevTools](https://developer.chrome.com/devtools)
- [Border styles](https://developer.mozilla.org/en-US/docs/Web/CSS/border-style#Values)
- [Colors](https://developer.mozilla.org/en-US/docs/Web/CSS/color_value)
- [Inline elements](https://developer.mozilla.org/en-US/docs/Web/HTML/Inline_elements)
- [Block level elements](https://developer.mozilla.org/en-US/docs/Web/HTML/Block-level_elements)
- [CSS Reset](http://meyerweb.com/eric/tools/css/reset)
- [Can I use](http://caniuse.com)
- [Vendor prefixes](https://developer.mozilla.org/en-US/docs/Glossary/Vendor_Prefix)
- [Generate necessary vendor prefixes](http://pleeease.io/play)
- [Modernizr](https://modernizr.com)
- [Paletton](http://paletton.com)
- [Adobe Color CC](http://color.adobe.com)
- [Color blindness](http://www.colourblindawareness.org/colour-blindness)
- [Color Laboratory](http://colorlab.wickline.org/colorblind/colorlab)
- [Google Fonts](https://fonts.google.com)
- [Font Squirrel](https://www.fontsquirrel.com)
- [Adobe Typekit](https://typekit.com)
- [dafont](http://www.dafont.com)
- [Typewolf](https://www.typewolf.com/google-fonts)
- [Google Font Combinations](https://www.behance.net/gallery/35768979/Typography-Google-Fonts-Combinations)
- [Hand-picked Tales from Æsop's Fables with Hand-picked Type from Google Fonts](https://femmebot.github.io/google-type)
- [Animated properties](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_animated_properties)
- [Transition timing function](https://developer.mozilla.org/en-US/docs/Web/CSS/transition-timing-function)
- [Transitions](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Transitions/Using_CSS_transitions)
- [Font Awesome](http://fontawesome.io)
- [Font Awesome cheat sheet](http://fontawesome.io/cheatsheet)
- [Favicon-Generator](http://www.favicon-generator.org)
- [Pixlr](https://pixlr.com/editor)
- [Online-convert](http://image.online-convert.com/convert-to-svg)
- [Web Accessibility Initiative](https://en.wikipedia.org/wiki/Web_Accessibility_Initiative)
- [ARIA](https://en.wikipedia.org/wiki/WAI-ARIA)
- [Semantic HTML elements](https://developer.mozilla.org/en-US/docs/Web/HTML/Element)
- [acceptable ARIA roles](https://www.w3.org/TR/html-aria/#allowed-aria-roles-states-and-properties)
- [ARIA presentation role](https://w3c.github.io/using-aria/#presentation)
- [ARIA properties](https://www.w3.org/TR/wai-aria/states_and_properties)

---

# CSS Setup

0. _CSS_, or Cascading Style Sheets, is a language that web developers use to _style_ the HTML content on a web page.

0. HTML and CSS are kept in separate files to keep code maintainable and readable, as well as keep structure separate from styling.

0. The `<style>` element allows you to write CSS code within the `<head>` element of an HTML file.

0. To style an HTML element, you can add the style attribute directly to the opening tag using _inline styles_:  

  `<p style="color: red;">This is an inline style</p>`

0. A CSS stylesheet can be linked to an HTML file using the `<link>` element, which requires three attributes:

  - `href` - set equal to the path of the CSS file
  - `type` - set equal to `text/css`
  - `rel` - set equal to `stylesheet`

  ```html
  <link href="style.css" type="text/css" rel="stylesheet">
  ```

0. Comments are written in CSS using the following syntax: `/* comment */`.


# CSS Selectors

- CSS can change the look of HTML elements. In order to do this, CSS must select HTML elements, then apply styles to them.

- CSS can select HTML elements by tag, `.class`, or `#id`.

- Multiple CSS classes can be applied to one HTML element:

  ```html
  <h1 class="green bold"> ... </h1>
  ```

- Classes can be reusable, while IDs can only be used once.

- IDs are more specific than classes, and classes are more specific than tags. That means IDs will override any styles from a class, and classes will override any styles from a tag selector.

- Multiple selectors can be chained together to select an element. This raises the specificity, but can be necessary.

  ```css
  h1.special {
  ```

- Nested elements can be selected by separating selectors with a space:

  ```css
  .main p {
  ```

- The `!important` flag will override any style, however it should almost never be used, as it is extremely difficult to override.

  ```css
  color: blue !important;
  ```

- Multiple unrelated selectors can receive the same styles by separating the selector names with commas:

  ```css
  h1, .menu {
  ```


# CSS Visual Rules

- CSS declarations are structured into _property_ and _value_ pairs:

  ```css
  color: blue;
  ```

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


# Display and Positioning

## The Box Model

0. The box model comprises a set of properties used to create space around and between HTML elements.

0. The `height` and `width` of a content area can be set in pixels or percentage.

0. `border` surrounds the content area and padding of an element. The color, style, and thickness of a border can be set with CSS properties.

0. `padding` is the space between the content area and the border. It can be set in pixels or percent.

0. `margin` is the amount of spacing outside of an element's border.

0. Horizontal margins add, so the total space between the borders of adjacent elements is equal to the sum of the right margin of one element and the left margin of the adjacent element.

0. Vertical margins collapse, so the space between vertically adjacent elements is equal to the larger margin.

0. `margin: 0 auto` horizontally centers an element inside of its parent content area, if it has a width.

0. The `overflow` property can be set to `visible`, `hidden`, or `scroll`, and dictates how HTML will render content that overflows its parent's content area.


## CSS Display

0. The default positioning of elements is based on the _flow_ of the HTML file.

0. `display: inline` elements appear next to each other on the same line.

  - The default display for some tags, such as `<em>`, `<strong>`, and `<a>`.

0. You can position elements to be displayed on their own line using `display: block`.

  - Elements that are block-level by default include all levels of heading elements (`<h1>` through `<h6>`), `<p>`, `<div>` and `<footer>`.

0. `display: inline-block` elements are on the same line as each other and their size can be set.

0. The default positioning for any element is `position: static` which means it will appear exactly as it does in the flow of the HTML document.

0. Elements with `position: absolute` positioning are removed from the flow of the document and positioned in relation to the parent element. This positioning will override display properties. An element with absolute positioning will scroll.

0. Elements with `position: fixed` positioning will not scroll as the page scrolls. This removes the element from the flow of the document.

0. Elements with `position: relative` positioning specify the element's distance from where it would have been positioned in the flow of the HTML document.

0. Non-static elements can be displayed in front or behind another element using the `z-index` property.


## Flexbox

A _flex container_ is an element on a page that contains flex items.  
All direct child elements of a flex container are _flex items_.

0. `display: flex` changes an element to a block-level container with flex items inside of it.

0. `display: inline-flex` allows multiple flex containers to appear inline with each other.

0. `justify-content` is used to space items along the major axis (horizontally).

  - `flex-start` — all items will be positioned in order starting, from the left of the parent container, with no extra space between or before them.

  - `flex-end` — all items will be positioned in order, with the last item starting on the right side of the parent container, with no extra space between or after them.

  - `center` — all items will be positioned in order, in the center of the parent container with no extra space before, between, or after them.

  - `space-around` — items will be positioned with equal space before and after each item, resulting in double the space between elements.

  - `space-between` — items will be positioned with equal space between them, but no extra space before the first or after the last elements.

0. `align-items` is used to space items along the cross axis (vertically).

  - `flex-start` — all elements will be positioned at the top of the parent container.

  - `flex-end` — all elements will be positioned at the bottom of the parent container.

  - `center` — the center of all elements will be positioned halfway between the top and bottom of the parent container.

  - `baseline` — the bottom of the content of all items will be aligned with each other.

  - `stretch` — if possible, the items will stretch from top to bottom of the container (this is the default value; elements with a specified height will not stretch; elements with a minimum height or no height specified will stretch).

0. `flex-grow` is declared on flex items and is used to specify how much space (and in what proportions) flex items absorb along the major axis.

0. `flex-shrink` is declared on flex items and is used to specify how much flex items shrink and in what proportions along the major axis.

0. `flex-basis` is used to specify the initial size of an element styled with `flex-grow` and/or `flex-shrink`.

0. `flex` is used to specify `flex-grow`, `flex-shrink`, and `flex-basis` in one declaration: `flex: 2 1 150px;`.

0. `flex-wrap` is declared on flex _containers_ and specifies that elements should shift along the cross axis if the flex container is not large enough.

  - `wrap` — child elements of a flex container will move down to the next line starting from the final item and working towards the first.

  - `nowrap` — prevents items from wrapping; this is the default value and is only necessary to override a wrap value set by a different CSS rule.

  - `wrap-reverse` — the wrapped element is displayed on top of the other elements in the flex container starting from the last and working toward the first (a mirror image of the wrap value).

0. `align-content` is declared on flex containers and is used to space rows along the cross axis (from the top to the bottom).

  - `flex-start` — all rows of elements will be positioned at the top of the parent container with no extra space between.

  - `flex-end` — all rows of elements will be positioned at the bottom of the parent container with no extra space between.

  - `center` — all rows of elements will be positioned at the center of the parent element with no extra space between.

  - `space-between` — all rows of elements will be spaced evenly from the top to the bottom of the container with no space above the first or below the last.

  - `space-around` — all rows of elements will be spaced evenly from the top to the bottom of the container with the same amount of space at the top and bottom and between each element.

  - `stretch` — if a minimum height or no height is specified, the rows of elements will stretch to fill the parent container from top to bottom (default value).

0. `flex-direction` is declared on flex containers and is used to specify the major and cross axes.

  - `row` — elements will be positioned from left to right across the parent element starting from the top left corner (default).

  - `row-reverse` — elements will be positioned from right to left across the parent element starting from the top right corner.

  - `column` — elements will be positioned from top to bottom of the parent element starting from the top left corner.

  - `column-reverse` — elements will be positioned from the bottom to the top of the parent element starting from the bottom left corner.

0. `flex-flow` is declared on flex containers and is used to specify `flex-wrap` and `flex-direction` in one declaration: `flex-flow: column wrap;`.

0. Flex containers can be nested inside of each other by declaring `display: flex` or `display: inline-flex` for children of flex containers.


# Design and UI Feedback

## CSS - Color

There are four ways to represent color in CSS:

- Named colors — there are 147 named colors, which you can review [here](https://msdn.microsoft.com/en-us/library/aa358802(v=vs.85).

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


## Design - Color

### DECIDING ON COLORS

Color palettes often follow a set of rules to make them more cohesive:

- Monochromatic — Variations on a single hue

- Analogous — Hues equidistant from each other (usually adjacent) on the color wheel and variations on these

- Complementary — Hues opposite each other on the color wheel and variations on these

### ACCESSIBLE COLORS

You can learn more about color blindness [here](http://www.colourblindawareness.org/colour-blindness).

You can use tools such as [Color Laboratory](http://colorlab.wickline.org/colorblind/colorlab) to emulate color-blindness as you're making decisions about your color palette.

### COLOR ON WEB PAGES

To choose text colors from your palette, find two contrasting colors within your palette, one dark and one light. Use one for the text and the other for the background.

Organize each element by importance. Then, apply the most striking colors to the most important elements.


## CSS - Typography

- _Typography_ is the art of arranging text on a page.

- Text can appear in any number of weights, with the `font-weight` property.

  1. `400` is the default `font-weight` of most text.
  2. `700` signifies a bold `font-weight`.
  3. `300` signifies a light `font-weight`.

- Text can appear in italics with the `font-style` property.

- The vertical spacing between lines of text can be modified with the `line-height` property:

  0. A unitless number, such as `1.2`. This number is an absolute value that will compute the line height as a ratio of the font size.
  0. A number specified by unit, such as `12px`. This number can be any valid CSS unit, such as pixels, percents, ems, or rems.

- _Serif_ fonts have extra details on the ends of each letter. _Sans-Serif_ fonts do not.

- _Fallback fonts_ are used when a certain font is not installed on a user's computer.

- [Google Fonts](https://fonts.google.com) provides free fonts that can be used in an HTML file with the `<link>` tag or the `@font-face` property.

- Local fonts can be added to a document with the `@font-face` property and the path to the font's source.


## Design - Typography

#### BACKGROUND

- font - refers to a typeface at a specific size

- typeface - describes a grouping of all sizes and styles of a specific typeface

#### SELECTING TYPEFACES FOR SITE DESIGN

###### SERIF VERSUS SANS-SERIF TYPEFACES

- serifs are very often employed by reading-focussed sites, such as news sites and blogs

- sans-serif fonts have become the most prevalent for display of text on computer screens

###### PAIRING TYPEFACES

- if you select a typeface on Google Fonts, at the bottom of the page you will be given suggested typeface pairings

The following resources provide in-depth advice on pairing fonts:

0. [Typewolf](https://www.typewolf.com/google-fonts)
0. [Google Font Combinations](https://www.behance.net/gallery/35768979/Typography-Google-Fonts-Combinations)
0. [Hand-picked Tales from Æsop's Fables with Hand-picked Type from Google Fonts](https://femmebot.github.io/google-type)

#### UTILIZING FONTS TO CONVEY CONTENT AND TONE

###### ESTABLISHING A VISUAL HIERARCHY

Typography should support at least three levels of hierarchy.

0. The primary level is for the most important content/information
0. The secondary level is to help organize your design into sections
0. The tertiary level is the meat of the design

###### SCALING

It is preferable to use ems and rems whenever possible.

###### LEADING AND TRACKING

Leading and tracking are tools to help make sure your text is readable.

Leading is the spacing between lines of text.

  - Using the CSS property `line-height`, you can make sure your lines are not crammed together or too far apart.

Tracking is the space between letters throughout a word.

  - `letter-spacing`

#### GETTING FEEDBACK


## Pseudo-classes

- _Pseudo-classes_ style elements based on user interactions and context within a web document.

- _Dynamic selectors_ style elements based on user interaction, and include `:link`, `:visited`, `:hover`, and `:active`.

- _Structural selectors_ style elements based on the location of their tags within an HTML document. These include `:first-child`, `:last-child`, and `:nth-child`.

  - `:nth-child(2n + 3)` selects every second, starting with the third.
  - `:nth-child(3n + 4)` selects every third, starting with the fourth.


## Animations - Transitions

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

```css
transition: all 1.5s linear 0.5s;
```

The shorthand property `transition` can be used to describe all four components of a transition at once. By using the comma (`,`) operator, many transitions can be described in one CSS rule.

```css
transition: width 750ms ease-in 200ms,
            left 500ms ease-out 450ms;
```


# Responsive Design and Browser Compatibility

## Sizing Elements

- Content on a website can be sized relative to other elements on the page using _relative measurements_.

- The unit of `em` sizes font relative to the font size of a parent element.

- The unit of `rem` sizes font relative to the font size of a root element. That root element is the `<html>` element.

- Percentages are commonly used to size box-model features, like the width, height, borders, padding, or margin of an element.

- When percentages are used to size width and height, child elements will be sized relative to the dimensions of their parent (remember that parent dimensions must first be set).

- Percentages can be used to set padding and margin. Horizontal and vertical padding and margin are set relative to the width of a parent element.

- The minimum and maximum width of elements can be set using `min-width` and `max-width`.

- The minimum and maximum height of elements can be set using `min-height` and `max-height`.

- When the height of an image or video is set, then its width can be set to `auto` so that the media scales proportionally. Reversing these two properties and values will also achieve the same result.

  ```css
  .container {
    width: 50%;
    height: 200px;
    overflow: hidden;
  }

  .container img {
    max-width: 100%;
    height: auto;
    display: block;
  }
  ```

- A background image of an HTML element will scale proportionally when its `background-size` property is set to `cover`.


## Media Queries

- When a website responds to the size of the screen it's viewed on, it’s called a _responsive_ website.

- You can write _media queries_ to help with different screen sizes.

- Media queries require _media features_. Media features are the conditions that must be met to render the CSS within a media query.

- Media features can detect many aspects of a user's browser, including the screen's width, height, resolution, orientation, and more.

`@media only screen and (max-width: 480px) {}`

  0. `@media` — This keyword begins a media query rule and instructs the CSS compiler on how to parse the rest of the rule.

  0. `only screen` — Indicates what types of devices should use this rule. `screen` is the media type always used for displaying content, no matter the type of device. The `only` keyword is added to indicate that this rule only applies to one media type (`screen`).

  0. `and (max-width : 480px)` — This part of the rule is called a _media feature_, and instructs the CSS compiler to apply the CSS styles to devices with a width of 480 pixels or smaller. Media features are the conditions that must be met in order to render the CSS within a media query.

- The `and` operator requires multiple media features to be true at once.

- A comma separated list of media features only requires one media feature to be true for the code within to be applied.

- The best practice for identifying where media queries should be set is by resizing the browser to determine where the content naturally breaks. Natural breakpoints are found by resizing the browser.


## Browser Compatibility

0. A website may not look the same in all browsers (or versions of browsers) due to differing user agent stylesheets across browsers.

0. User agent stylesheets can be reset with a CSS reset stylesheet.

  - Create a reset.css file.

  - Copy and paste CSS reset rules into the reset.css file.

  - A popular CSS reset can be found [here](http://meyerweb.com/eric/tools/css/reset/).

    ```css
    /* http://meyerweb.com/eric/tools/css/reset/
       v2.0 | 20110126
       License: none (public domain)
    */

    html, body, div, span, applet, object, iframe,
    h1, h2, h3, h4, h5, h6, p, blockquote, pre,
    a, abbr, acronym, address, big, cite, code,
    del, dfn, em, img, ins, kbd, q, s, samp,
    small, strike, strong, sub, sup, tt, var,
    b, u, i, center,
    dl, dt, dd, ol, ul, li,
    fieldset, form, label, legend,
    table, caption, tbody, tfoot, thead, tr, th, td,
    article, aside, canvas, details, embed,
    figure, figcaption, footer, header, hgroup,
    menu, nav, output, ruby, section, summary,
    time, mark, audio, video {
    	margin: 0;
    	padding: 0;
    	border: 0;
    	font-size: 100%;
    	font: inherit;
    	vertical-align: baseline;
    }
    /* HTML5 display-role reset for older browsers */
    article, aside, details, figcaption, figure,
    footer, header, hgroup, menu, nav, section {
    	display: block;
    }
    body {
    	line-height: 1;
    }
    ol, ul {
    	list-style: none;
    }
    blockquote, q {
    	quotes: none;
    }
    blockquote:before, blockquote:after,
    q:before, q:after {
    	content: '';
    	content: none;
    }
    table {
    	border-collapse: collapse;
    	border-spacing: 0;
    }
    ```

0. A CSS reset stylesheet can be linked in an HTML file.

  - Link to reset.css in the HTML file (make sure reset.css is loaded first before other CSS files, otherwise reset.css may reset your custom rules by accident).
  - `<link href="reset.css" type="text/css" rel="stylesheet">`

0. Resources like "[Can I use](http://caniuse.com/)" allow you to check if a CSS feature is supported across multiple browsers.

0. [Vendor prefixes](https://developer.mozilla.org/en-US/docs/Glossary/Vendor_Prefix) increase the browser compatibility of CSS features. This is because they indicate to browsers how the rule should be specifically implemented.

0. Polyfills are libraries that increase the browser compatibility of a website. They allow developers to write alternative CSS rules based on whether or not a browser supports a certain feature.


# Icons, Assets and Accessibility

## Font Awesome

0. The Font Awesome library can be linked to an HTML document from a remote CDN or a local CSS file.

0. Font Awesome icons are added to a website by setting an `<i>` tag's classes to `fa` and `fa-icon-name`, where `fa-icon-name` refers to the icon-specific class name.

0. Font Awesome icons can be resized using `fa-lg`, `fa-2x`, `fa-3x`, `fa-4x`, or `fa-5x`.

Here are a few best practices to help you anticipate and plan for user misunderstanding:

  0. Research the icon in question. When in doubt, check to see if the icon shows up on other popular sites.
  0. Use a word or two next to the icon for additional context.


## Managing Assets and Icons

_favicon_ - a small image displayed in the tab or browser bar containing the name of the page being viewed

Three types of image files:

0. JPEG - a highly compressible file type that is preferred for images with significant detail

0. PNG - a file type that is lossless (meaning that full quality is maintained) - generally preferred for images with less detail such as logos

0. SVG - useful for high resolution screens, scalable vector graphics (SVG) will change size (scale) for various screen sizes; SVGs also contain roughly 50% less data than their JPEG or PNG equivalents allowing web pages to load more quickly; they are becoming widely used for simple images such as icons and logos

### Making favicons

To convert an existing image to a favicon, you can use an online conversion tool such as [Favicon-Generator](http://www.favicon-generator.org).

### Editing Images

A best practice is to ensure that images are sized properly before adding them to an HTML file.

Adobe Photoshop is a commonly used and useful tool for all sorts of photo editing tasks, but requires a monthly subscription fee. A free and industry-accepted alternative is, [Pixlr](https://pixlr.com/editor).

The web standard for JPEG files is 85%.

### Converting to Scalable Vector Format

To convert an image to SVG, you can use an online conversion tool such as [online-convert](http://image.online-convert.com/convert-to-svg).


## Accessibility and ARIA

Using ARIA roles and properties, `alt` attributes, and semantic elements in your HTML is a simple way to make your website accessible to visually-impaired Internet users.

0. Using semantic HTML elements whenever possible (such as `<header>` instead of `<div id="header">`) will allow screen reader users to navigate your website more efficiently.

0. The `role` attribute is used to communicate information about the role of specific elements.

  - [list of acceptable ARIA roles](https://www.w3.org/TR/html-aria/#allowed-aria-roles-states-and-properties)

0. `role="presentation"` allows a screen reader to skip markup elements that don't directly contain useful information.

0. `aria-label` and other ARIA properties can be used to help users perceive information that is communicated visually but not through text.

0. The `alt` attribute should be added to every image element (and all other elements that support it) instead of `aria-label`. When used, its value should be a useful description of the image.
