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

- inline block: sometimes we need something which can stay inline but which we can set margins and paddings on

- about styling buttons: put class directly on your link. always use padding to create "size" of the button, and not width and height. the padding left and right needs to be bigger number than the padding on the top and bottom. in general, use 1:2.5 patio for the top and sides. But it really depends on the button. if it's a small button, you can use 1:1.5. if it's a big button, you can use 1:3.5. if it's a really big button, you can use 1:4.5. it's all about the look and feel of the button. you can also use a border-radius to round the corners of the button. you can also use a box-shadow to give it a little bit of depth. you can also use a text-shadow to give it a little bit of depth. you can also use a transition to make it look like it's moving when you hover over it. you can also use a transform to make it look like it's moving when you hover over it.

- specificity in CSS is all about how specific our selectors are. the more specific they are, the higher priority they have. from lowest to highest. element, class, id, inline styles. eg. p, .class, #id, style="color: red;"

  - this is one of the reasons many class naming conventions only use classes, and not ids. because ids are too specific, and can use issues.
  - generals rules get put on element selectors (e.g. body, headings, paragraphs, etc.), and specific rules get put on class selectors. ids are rarely used in CSS, and are mostly used for JavaScript.
  - if you have two selectors that are the same specificity, the one that comes last in the CSS file will win.

## Compound selectors and specificity

- for section tag, it's better to have h tag as first tag inside
- id 100, class 10, element 1
- give everything a class, and don't use ids in CSS. ids are for JavaScript.

## a better way to name our css classes

- use generic button class like 'btn', then use modifier classes like 'btn-primary', 'btn-secondary', 'btn-danger', 'btn-success', etc. `class="btn btn-primary"`
