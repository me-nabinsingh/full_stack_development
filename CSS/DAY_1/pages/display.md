# display
The CSS `display` property is a fundamental attribute that controls how an HTML element is rendered on a webpage. It determines the type of box used for an element and influences its layout and positioning within the document.

Understanding the different values of the display property is crucial for building well-structured and responsive web layouts. By choosing the appropriate value, you can control the flow of elements, create grids, and adjust the visibility of specific elements.

```
display: <value>;
```

The following values can be appplied to the display property:
* inline
* block
* contents
* flex
* grid
* inline-block
* inline-flex
* inline-grid
* list-item
* run-in
* table
* table-caption
* table-column-group
* table-header-group
* table-footer-group
* table-row-group
* table-cell
* table-column
* table-row
* none
* initial
* inherit


## Differences Between Display Values
The display property in CSS allows you to control how elements are rendered on a webpage. Here are the commonly used display values and their descriptions:

### `1. display: block`
Elements with `display: block;` are rendered as block-level elements. They create a line break after the element and occupy the full width of their parent container.
```
.block-element {
  display: block;
}
```

### `2. display: inline`
Elements with `display: inline;` are rendered as inline elements. They don’t create line breaks and occupy only the necessary width and height based on their content.
```
.inline-element {
  display: inline;
}
```

### `3.display: inline-block`
Elements with `display: inline-block;` are rendered as inline-level block elements. They behave like inline elements but allow you to set width, height, padding, and margins.
```
.inline-block-element {
  display: inline-block;
}
```

### `4. display: none`
Elements with `display: none;` are not rendered and are completely hidden from the page. They don’t take up any space in the document flow.
```
.hidden-element {
  display: none;
}
```

### `5. display: flex`
Elements with display: flex; create a flex container, allowing you to build flexible and responsive layouts. Flex items inside the container can be positioned and resized using flexbox properties.

```
.flex-container {
  display: flex;
}
```

### `6. display: grid`
Elements with display: grid; create a grid container that enables you to define rows and columns, creating a two-dimensional grid system. Child elements inside the container can be placed in specific cells and adjusted for size and alignment.

```
.grid-container {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  grid-gap: 10px;
}
```

### Overriding Display Values
CSS specificity allows you to override default display values of elements. Here’s an example of overriding display:

```
/* Original CSS */
.element {
  display: inline;
}

/* Overriding with higher specificity */
.container .element {
  display: block;
}
```

### Responsive Design Considerations
The display property can be combined with media queries to create responsive designs. Here’s an example:

```
@media (max-width: 768px) {
  .element {
    display: none; /* Hide element on smaller screens */
  }
}

@media (min-width: 768px) {
  .element {
    display: block; /* Display element on larger screens */
  }
}
```

### display: grid and display: flex Comparison
CSS Grid and Flexbox are powerful layout tools. The choice between display: flex and display: grid depends on the layout requirements and the desired design approach. Flexbox is particularly useful for creating responsive and flexible layouts, especially when dealing with content in a linear fashion, such as navigation menus, image galleries, or vertically aligned elements.

```
.flex-container {
  display: flex;
  justify-content: space-around;
}
.flex-item {
  background-color: cyan;
  padding: 20px;
  margin: 2px;
}
.grid-container {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  grid-template-rows: auto;
  grid-gap: 10px;
}
.grid-item {
  background-color: orange;
  padding: 20px;
}
.item-1 {
  grid-column: 1 / span 2;
  grid-row: 1;
}
.item-2 {
  grid-column: 3;
  grid-row: 1 / span 2;
}
.item-3 {
  grid-column: 1;
  grid-row: 2 / span 2;
}
.item-4 {
  grid-column: 2 / span 2;
  grid-row: 3;
}
.item-6 {
  grid-column: 1 / span 3;
}
```
![](../images/css-display-flex-versus-grid.png)



### `clear`
Species whether an element coming after a floated element should be moved down or not.
```
clear: <value>;
```
The following values can be be appplied:
* `none`: The element is not moved down to clear past floating elements (the default).
* `left`: The element is moved down to clear past left floated elements.
* `right`: The element is moved down to clear past right floated elements.
* `both`: The element is moved down to clear past both left and right floated elements.

Making an img element move down a left floated h1 element.
```
.div1 h1 {
  float: left;
}

.div1 img {
  clear: left;
}
```


