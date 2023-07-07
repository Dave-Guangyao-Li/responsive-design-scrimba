- [Responsive Design Scrimba](https://scrimba.com/learn/responsive/margin-and-padding-collapsing-margins-c39EgLua)

# Notes

- margins will collapse any time they touch each other. So, if the first child in an element has a megin-top, that can merge with parent's margin-top.
- for consistency, often we "turn off" the margin-top pn typography related elements like h1, h2, p, etc. by setting them to 0. That way we can use padding on the parent, and know the exact spacing that we'll have, and can keep all sides consistent. Also, when we get into layouts with flexbox and grid, margins no longer collapse, so this helps us keep things consistent. we can include all elements in one selector

  ```css
  h1,
  h2,
  h3,
  p {
    margin-top: 0;
  }
  ```

- block level elements will create a new line of content, stacking on top of each other by default. eg. Paragraphs, Headings, lists and list items, div, header, footer, main, section, etc.
- inline elements stay within the flow of what's around them. eg. Links, span, strong, em, images(sort of) but img is not exactly inline, it's inline-block, which means it's inline, but it can have a width and height, and it can have padding and margin, but it will stay within the flow of what's around it.

  - inline elements will not respect width and height
  - padding and margin on the top or bottom may cause issues
  - you can only nest other inline elements in them (such as outting a link inside a strong element).
  - span elemtn is a generic inline element that can be used for styling purposes, or to wrap other inline elements. we put class on span to style it.

- about styling links
  - links have different "states" that we can style as well.
  - default "link" state; Visited; Focus; Hover; Active(actively clicking on it)
  - we can style these states by using pseudo classes. eg. a:link, a:visited, a:focus, a:hover, a:active
