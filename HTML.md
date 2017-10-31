# HTML

summary...

## Table of Contents

- [Introduction to HTML](#introduction-to-html)
- [HTML Tags](#html-tags)

### Resources

- []()

---

# Introduction to HTML

0. __HTML__ stands for __H__ yper __T__ ext __M__ arkup __L__ anguage and is used to create the structure and content of a webpage.

0. Most HTML elements contain opening and closing tags with raw text or other HTML tags between them.

0. Single-closing tags cannot enclose raw text or other elements: `<br />`.

0. Comments are written in HTML using the following syntax: `<!-- comment -->`.

0. HTML elements can be nested inside other elements. The enclosed element is the child of the enclosing parent element.

0. Whitespace between HTML elements helps make code easier to read while not changing how elements appear in the browser.

0. Indentation also helps make code easier to read. It makes parent-child relationships visible.

0. The `<!DOCTYPE html>` declaration should always be the first line of code in your HTML files.

0. The `<html>` element will contain all of your HTML code.

0. Information about the web page, like the title, belongs within the `<head>` of the page.

0. You can add a title to your web page by using the `<title>` element, inside of the head.

0. A webpage's title appears in a browser's tab.

0. Code for visible HTML content is placed inside of the `<body>` element.


# HTML Tags

0. Headings and sub-headings, `<h1>` to `<h6>` tags, are used to enlarge text.

0. `<p>`_(paragraphs)_, `<span>`_(same line)_ and `<div>`_(divide)_ tags specify text or blocks.

0. The `<em>`(_italic_) and `<strong>`(__bold__) tags are used to emphasize text.

0. Line breaks are created with the `<br />` or `<br>` tags.

0. Ordered lists (`<ol>`) are numbered and unordered lists (`<ul>`) are bulleted.

  - Individual list items must be added to the unordered list using the list item `<li>` tag, to describe an item in a list.

0. Images (`<img>`) and videos (`<video>`) can be added by linking to an existing source:

  `<img src="image-location.com" />`  

  `<video src="myVideo.mp4" width="320" height="240" controls> Video not supported </video>`

0. Anchor tags (`<a>`) are used to link to internal pages, external pages or content on the same page (see next):

  - internal/relative: `<a href="./contact.html">Contact</a>`  
  - external: `<a href="https://www.wikipedia.org">This Is A Link To Wikipedia</a>`  
  - new page: `<a href="https://www.wikipedia.org" target="_blank">This Is A Link To Wikipedia</a>`

0. You can create sections on a webpage and jump to them using `<a>` tags and adding ids to the elements you wish to jump to:

  - same page: `<a href="#top">Top</a>`

0. The `nav` element contains links to internal pages or content.

0. _Non-semantic_ tags means that they do not describe the content that is inside of them: `<div>`  
_Semantic_ tags are used to describe the content that they surround, which helps us modify and style our content later: `<nav>`
