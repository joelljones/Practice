# HTML

__Hypertext Markup Language (HTML)__ is the standard markup language for creating web pages and web applications. Web browsers receive HTML documents from a web server or from local storage and render them into multimedia web pages. HTML describes the structure of a web page semantically.

## Table of Contents

- [Introduction to HTML](#introduction-to-html)
- [HTML Tags](#html-tags)

### Resources

- [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML)
- [W3Schools](https://w3schools.com/html)
- [World Wide Web Consortium or W3C](https://w3.org/Consortium)
- [HTML tag/element reference](https://developer.mozilla.org/en-US/docs/Web/HTML/Element)

---

# Introduction to HTML

1. __HTML__ stands for __H__ yper __T__ ext __M__ arkup __L__ anguage and is used to create the structure and content of a webpage.

1. Most HTML elements contain opening and closing tags with raw text or other HTML tags between them.

1. Single-closing tags cannot enclose raw text or other elements: `<br />`.

1. Comments are written in HTML using the following syntax: `<!-- comment -->`.

1. HTML elements can be nested inside other elements. The enclosed element is the child of the enclosing parent element.

1. Whitespace between HTML elements helps make code easier to read while not changing how elements appear in the browser.

1. Indentation also helps make code easier to read. It makes parent-child relationships visible.

1. The `<!DOCTYPE html>` declaration should always be the first line of code in your HTML files.

1. The `<html>` element will contain all of your HTML code.

1. Information about the web page, like the title, belongs within the `<head>` of the page.

1. You can add a title to your web page by using the `<title>` element, inside of the head.

1. A webpage's title appears in a browser's tab.

1. Code for visible HTML content is placed inside of the `<body>` element.


# HTML Tags

1. Headings and sub-headings, `<h1>` to `<h6>` tags, are used to enlarge text.

1. `<p>`_(paragraphs)_, `<span>`_(same line)_ and `<div>`_(divide)_ tags specify text or blocks.

1. The `<em>`(_italic_) and `<strong>`(__bold__) tags are used to emphasize text.

1. Line breaks are created with the `<br />` or `<br>` tags.

1. Ordered lists (`<ol>`) are numbered and unordered lists (`<ul>`) are bulleted.

  - Individual list items must be added to the unordered list using the list item `<li>` tag, to describe an item in a list.

1. Images (`<img>`) and videos (`<video>`) can be added by linking to an existing source:

  ```html
  <img src="image-location.com" />

  <video src="myVideo.mp4" width="320" height="240" controls> Video not supported </video>
  ```

1. Anchor tags (`<a>`) are used to link to internal pages, external pages or content on the same page (see next):

  - internal/relative: `<a href="./contact.html">Contact</a>`  
  - external: `<a href="https://wikipedia.org">This Is A Link To Wikipedia</a>`  
  - new page: `<a href="https://wikipedia.org" target="_blank">This Is A Link To Wikipedia</a>`

1. You can create sections on a webpage and jump to them using `<a>` tags and adding ids to the elements you wish to jump to:

  - same page: `<a href="#top">Top</a>`

1. The `nav` element contains links to internal pages or content.

1. _Non-semantic_ tags means that they do not describe the content that is inside of them: `<div>`  
_Semantic_ tags are used to describe the content that they surround, which helps us modify and style our content later: `<nav>`
