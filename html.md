# HTML

__Hypertext Markup Language (HTML)__ is the standard markup language for creating web pages and web applications. Web browsers receive HTML documents from a web server or from local storage and render them into multimedia web pages. HTML describes the structure of a web page semantically.


## Table of Contents

- [Introduction to HTML](#introduction-to-html)
- [HTML Tags](#html-tags)
- [Tables](#tables)


### Resources

- [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML)
- [W3Schools](https://w3schools.com/html)
- [World Wide Web Consortium or W3C](https://w3.org/Consortium)
- [HTML tag/element reference](https://developer.mozilla.org/en-US/docs/Web/HTML/Element)

---

# Introduction to HTML

1. __HTML__ stands for __H__ yper __T__ ext __M__ arkup __L__ anguage and is used to create the structure and content of a webpage.

2. Most HTML elements contain opening and closing tags with raw text or other HTML tags between them.

3. Single-closing tags cannot enclose raw text or other elements.

4. Comments are written in HTML using the following syntax: `<!-- comment -->`.

5. HTML elements can be nested inside other elements. The enclosed element is the child of the enclosing parent element.

6. Whitespace between HTML elements helps make code easier to read while not changing how elements appear in the browser.

7. Indentation also helps make code easier to read. It makes parent-child relationships visible.

8. The `<!DOCTYPE html>` declaration should always be the first line of code in your HTML files.

9. The `<html>` element will contain all of your HTML code.

10. Information about the web page, like the title, belongs within the `<head>` of the page.

11. You can add a title to your web page by using the `<title>` element, inside of the head.

12. A webpage's title appears in a browser's tab.

13. Code for visible HTML content is placed inside of the `<body>` element.


# HTML Tags

1. Headings and sub-headings, `<h1>` to `<h6>` tags, are used to enlarge text.

2. `<p>`_(paragraphs)_, `<span>`_(same line)_ and `<div>`_(divide)_ tags specify text or blocks.

3. The `<em>`(_italic_) and `<strong>`(__bold__) tags are used to emphasize text.

4. Line breaks are created with the `<br />` or `<br>` tags.

5. Ordered lists (`<ol>`) are numbered and unordered lists (`<ul>`) are bulleted.

  - Individual list items must be added to the unordered list using the list item `<li>` tag, to describe an item in a list.

6. Images (`<img>`) and videos (`<video>`) can be added by linking to an existing source:

  `<img src="image-location.com" />`  

  `<video src="myVideo.mp4" width="320" height="240" controls> Video not supported </video>`

7. Anchor tags (`<a>`) are used to link to internal pages, external pages or content on the same page(see #8):

  - internal/relative: `<a href="./contact.html">Contact</a>`  
  - external: `<a href="https://www.wikipedia.org/">This Is A Link To Wikipedia</a>`  
  - new page: `<a href="https://www.wikipedia.org/" target="_blank">This Is A Link To Wikipedia</a>`

8. You can create sections on a webpage and jump to them using `<a>` tags and adding ids to the elements you wish to jump to:

  - same page: `<a href="#top">Top</a>`

9. The `nav` element contains links to internal pages or content.

10. _Non-semantic_ tags means that they do not describe the content that is inside of them: `<div>`  
_Semantic_ tags are used to describe the content that they surround, which helps us modify and style our content later: `<nav>`


# Tables

1. The `<table>` element creates a table.

2. The `<tr>` element adds rows to a table.

3. To add data to a row, you can use the `<td>` element.

4. Table headings clarify the meaning of data. Headings are added with the `<th>`` element.

5. Table data can span columns using the `colspan` attribute.

6. Table data can span rows using the `rowspan` attribute.

7. Tables can be split into three main sections: a head, a body, and a footer.

8. A table's head is created with the `<thead>` element.

9. A table's body is created with the `<tbody>` element.

10. A table's footer is created with the `<tfoot>` element.

11. All the CSS properties you learned about in this course can be applied to tables and their data.
