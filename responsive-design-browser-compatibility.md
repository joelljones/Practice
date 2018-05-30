# Responsive Design and Browser Compatibility

## Table of Contents

- [Sizing Elements](#sizing-elements)
- [Media Queries](#media-queries)
- [Browser Compatibility](#browser-compatibility)

### Resources

- [CSS Reset](http://meyerweb.com/eric/tools/css/reset)
- [Can I use](http://caniuse.com)
- [Modernizr](https://modernizr.com)
- [Vendor prefixes](https://developer.mozilla.org/en-US/docs/Glossary/Vendor_Prefix)
- [Generate necessary vendor prefixes](http://pleeease.io/play)

---

# Sizing Elements

- Content on a website can be sized relative to other elements on the page using _relative measurements_.

- The unit of `em` sizes font relative to the font size of a parent element.

- The unit of `rem` sizes font relative to the font size of a root element. That root element is the `<html>` element.

- Percentages are commonly used to size box-model features, like the width, height, borders, padding, or margin of an element.

- When percentages are used to size width and height, child elements will be sized relative to the dimensions of their parent (remember that parent dimensions must first be set).

- Percentages can be used to set padding and margin. Horizontal and vertical padding and margin are set relative to the width of a parent element.

- The minimum and maximum width of elements can be set using `min-width` and `max-width`.

- The minimum and maximum height of elements can be set using `min-height` and `max-height`.

- When the height of an image or video is set, then its width can be set to `auto` so that the media scales proportionally. Reversing these two properties and values will also achieve the same result.

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

- A background image of an HTML element will scale proportionally when its `background-size` property is set to `cover`.

# Media Queries

- When a website responds to the size of the screen it's viewed on, it’s called a _responsive_ website.

- You can write _media queries_ to help with different screen sizes.

- Media queries require _media features_. Media features are the conditions that must be met to render the CSS within a media query.

- Media features can detect many aspects of a user's browser, including the screen's width, height, resolution, orientation, and more.

`@media only screen and (max-width: 480px) {}`

1. `@media` — This keyword begins a media query rule and instructs the CSS compiler on how to parse the rest of the rule.

2. `only screen` — Indicates what types of devices should use this rule. `screen` is the media type always used for displaying content, no matter the type of device. The `only` keyword is added to indicate that this rule only applies to one media type (`screen`).

3. `and (max-width : 480px)` — This part of the rule is called a _media feature_, and instructs the CSS compiler to apply the CSS styles to devices with a width of 480 pixels or smaller. Media features are the conditions that must be met in order to render the CSS within a media query.

    - The `and` operator requires multiple media features to be true at once.

    - A comma separated list of media features only requires one media feature to be true for the code within to be applied.

    - The best practice for identifying where media queries should be set is by resizing the browser to determine where the content naturally breaks. Natural breakpoints are found by resizing the browser.

# Browser Compatibility

1. A website may not look the same in all browsers (or versions of browsers) due to differing user agent stylesheets across browsers.

2. User agent stylesheets can be reset with a CSS reset stylesheet.

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

3. A CSS reset stylesheet can be linked in an HTML file.

    - Link to reset.css in the HTML file (make sure reset.css is loaded first before other CSS files, otherwise reset.css may reset your custom rules by accident).
    - `<link href="reset.css" type="text/css" rel="stylesheet">`

4. Resources like "[Can I use](http://caniuse.com)" allow you to check if a CSS feature is supported across multiple browsers.

5. [Vendor prefixes](https://developer.mozilla.org/en-US/docs/Glossary/Vendor_Prefix) increase the browser compatibility of CSS features. This is because they indicate to browsers how the rule should be specifically implemented.

6. Polyfills are libraries that increase the browser compatibility of a website. They allow developers to write alternative CSS rules based on whether or not a browser supports a certain feature.
