# Flexbox

### Resources

- [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS)
- [W3Schools](https://w3schools.com/css)
- [W3C](https://www.w3.org/Style/CSS)

---

# Flexbox

A _flex container_ is an element on a page that contains flex items.  
All direct child elements of a flex container are _flex items_.

1. `display: flex` changes an element to a block-level container with flex items inside of it.

2. `display: inline-flex` allows multiple flex containers to appear inline with each other.

3. `justify-content` is used to space items along the major axis (horizontally).

  - `flex-start` — all items will be positioned in order starting, from the left of the parent container, with no extra space between or before them.

  - `flex-end` — all items will be positioned in order, with the last item starting on the right side of the parent container, with no extra space between or after them.

  - `center` — all items will be positioned in order, in the center of the parent container with no extra space before, between, or after them.

  - `space-around` — items will be positioned with equal space before and after each item, resulting in double the space between elements.

  - `space-between` — items will be positioned with equal space between them, but no extra space before the first or after the last elements.

4. `align-items` is used to space items along the cross axis (vertically).

  - `flex-start` — all elements will be positioned at the top of the parent container.

  - `flex-end` — all elements will be positioned at the bottom of the parent container.

  - `center` — the center of all elements will be positioned halfway between the top and bottom of the parent container.

  - `baseline` — the bottom of the content of all items will be aligned with each other.

  - `stretch` — if possible, the items will stretch from top to bottom of the container (this is the default value; elements with a specified height will not stretch; elements with a minimum height or no height specified will stretch).

5. `flex-grow` is declared on flex items and is used to specify how much space (and in what proportions) flex items absorb along the major axis.

6. `flex-shrink` is declared on flex items and is used to specify how much flex items shrink and in what proportions along the major axis.

7. `flex-basis` is used to specify the initial size of an element styled with `flex-grow` and/or `flex-shrink`.

8. `flex` is used to specify `flex-grow`, `flex-shrink`, and `flex-basis` in one declaration: `flex: 2 1 150px;`.

9. `flex-wrap` is declared on flex _containers_ and specifies that elements should shift along the cross axis if the flex container is not large enough.

  - `wrap` — child elements of a flex container will move down to the next line starting from the final item and working towards the first.

  - `nowrap` — prevents items from wrapping; this is the default value and is only necessary to override a wrap value set by a different CSS rule.

  - `wrap-reverse` — the wrapped element is displayed on top of the other elements in the flex container starting from the last and working toward the first (a mirror image of the wrap value).

10. `align-content` is declared on flex containers and is used to space rows along the cross axis (from the top to the bottom).

  - `flex-start` — all rows of elements will be positioned at the top of the parent container with no extra space between.

  - `flex-end` — all rows of elements will be positioned at the bottom of the parent container with no extra space between.

  - `center` — all rows of elements will be positioned at the center of the parent element with no extra space between.

  - `space-between` — all rows of elements will be spaced evenly from the top to the bottom of the container with no space above the first or below the last.

  - `space-around` — all rows of elements will be spaced evenly from the top to the bottom of the container with the same amount of space at the top and bottom and between each element.

  - `stretch` — if a minimum height or no height is specified, the rows of elements will stretch to fill the parent container from top to bottom (default value).

11. `flex-direction` is declared on flex containers and is used to specify the major and cross axes.

  - `row` — elements will be positioned from left to right across the parent element starting from the top left corner (default).

  - `row-reverse` — elements will be positioned from right to left across the parent element starting from the top right corner.

  - `column` — elements will be positioned from top to bottom of the parent element starting from the top left corner.

  - `column-reverse` — elements will be positioned from the bottom to the top of the parent element starting from the bottom left corner.

12. `flex-flow` is declared on flex containers and is used to specify `flex-wrap` and `flex-direction` in one declaration: `flex-flow: column wrap;`.

13. Flex containers can be nested inside of each other by declaring `display: flex` or `display: inline-flex` for children of flex containers.
