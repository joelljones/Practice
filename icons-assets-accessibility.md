# Icons, Assets and Accessibility

## Table of Contents

- [Font Awesome](#font-awesome)
- [Managing Assets and Icons](#managing-assets-and-icons)
- [Accessibility and ARIA](#accessibility-and-aria)

### Resources

- [Font Awesome](http://fontawesome.io)
- [Font Awesome cheat sheet](http://fontawesome.io/cheatsheet)
- [Favicon-Generator](http://favicon-generator.org)
- [Pixlr](https://pixlr.com/editor)
- [Online-convert](http://image.online-convert.com/convert-to-svg)
- [Web Accessibility Initiative](https://en.wikipedia.org/wiki/Web_Accessibility_Initiative)
- [ARIA](https://en.wikipedia.org/wiki/WAI-ARIA)
- [acceptable ARIA roles](https://w3.org/TR/html-aria/#allowed-aria-roles-states-and-properties)
- [ARIA presentation role](https://w3c.github.io/using-aria/#presentation)
- [ARIA properties](https://w3.org/TR/wai-aria/states_and_properties)

---

# Font Awesome

1. The Font Awesome library can be linked to an HTML document from a remote CDN or a local CSS file.

2. Font Awesome icons are added to a website by setting an `<i>` tag's classes to `fa` and `fa-icon-name`, where `fa-icon-name` refers to the icon-specific class name.

3. Font Awesome icons can be resized using `fa-lg`, `fa-2x`, `fa-3x`, `fa-4x`, or `fa-5x`.

Here are a few best practices to help you anticipate and plan for user misunderstanding:

  1. Research the icon in question. When in doubt, check to see if the icon shows up on other popular sites.
  2. Use a word or two next to the icon for additional context.

# Managing Assets and Icons

_favicon_ - a small image displayed in the tab or browser bar containing the name of the page being viewed

Three types of image files:

1. JPEG - a highly compressible file type that is preferred for images with significant detail

2. PNG - a file type that is lossless (meaning that full quality is maintained) - generally preferred for images with less detail such as logos

3. SVG - useful for high resolution screens, scalable vector graphics (SVG) will change size (scale) for various screen sizes; SVGs also contain roughly 50% less data than their JPEG or PNG equivalents allowing web pages to load more quickly; they are becoming widely used for simple images such as icons and logos

## Making favicons

To convert an existing image to a favicon, you can use an online conversion tool such as [Favicon-Generator](http://www.favicon-generator.org).

## Editing Images

A best practice is to ensure that images are sized properly before adding them to an HTML file.

Adobe Photoshop is a commonly used and useful tool for all sorts of photo editing tasks, but requires a monthly subscription fee. A free and industry-accepted alternative is, [Pixlr](https://pixlr.com/editor).

The web standard for JPEG files is 85%.

## Converting to Scalable Vector Format

To convert an image to SVG, you can use an online conversion tool such as [online-convert](http://image.online-convert.com/convert-to-svg).

# Accessibility and ARIA

Using ARIA roles and properties, `alt` attributes, and semantic elements in your HTML is a simple way to make your website accessible to visually-impaired Internet users.

1. Using semantic HTML elements whenever possible (such as `<header>` instead of `<div id="header">`) will allow screen reader users to navigate your website more efficiently.

2. The `role` attribute is used to communicate information about the role of specific elements.

    - [list of acceptable ARIA roles](https://www.w3.org/TR/html-aria/#allowed-aria-roles-states-and-properties)

3. `role="presentation"` allows a screen reader to skip markup elements that don't directly contain useful information.

4. `aria-label` and other ARIA properties can be used to help users perceive information that is communicated visually but not through text.

5. The `alt` attribute should be added to every image element (and all other elements that support it) instead of `aria-label`. When used, its value should be a useful description of the image.
