# Flexbox
The Flexible Box Layout, commonly known as Flexbox, is a layout model that allows for responsive elements within a container that can automatically adapt to differing screen sizes.

```
div {
  display: flex;
}
```

### Properties for the Parent (flex container)
![Properties for the Parent](../images/01-container.svg)

## display
This defines a flex container; inline or block depending on the given value. It enables a flex context for all its direct children.

```
.container {
  display: flex; /* or inline-flex */
}
```

## flex
The `flex` property is a shorthand that combines the `flex-grow`, `flex-shrink`, and `flex-basis` properties. This syntax allows for the concise delineation of flex item parameters with one line of code.

### Syntax
```
#item {
  flex: <flex-grow> <flex-shrink> <flex-basis>;
}
```
The values can be any of the following options:
* A keyword: `auto`
* A length: `200px`
* An integer or decimal: `1` , `.5`
* `flex-shrink` and `flex-basis` are optional.

Default values are `0` `1` `auto`.

### Example
An element that will occupy twice the space as other items in the same container:
```
#item-foo {
  flex: 2 0 auto;
}
```



## flex-direction
![flex-direction](../images/flex-direction.svg)
A property that specifies the direction in which elements are distributed within a container.

This establishes the main-axis, thus defining the direction flex items are placed in the flex container. Flexbox is (aside from optional wrapping) a single-direction layout concept. Think of flex items as primarily laying out either in horizontal rows or vertical columns.


### Syntax
```
#element-container {
  display: flex;
  flex-direction: <flex-value>;
}
```
The `<flex-value>` can be one of four options:
* Elements arranged left to right: `row`
* Elements arranged right to left: `row-reverse`
* Elements arranged top to bottom: `column`
* Elements arranged bottom to top: `column-reverse`

## Example
Content that is arranged horizontally within a container:
```
#spam-container {
  display: flex;
  flex-direction: row;
}
```

## flex-wrap
![flex-wrap](../images/flex-wrap.svg)
A property that specifies if elements will occupy multiple lines and the direction in which the items are distributed.

### Syntax
```
#element-container {
  display: flex;
  flex-wrap: <wrap-value>;
}
```
The `<wrap-value>` can be one of three options:
* `wrap`
* `nowrap`
* `wrap-reverse`

### Example
Content that does not utilize multiple lines:
```
#spam-container {
  display: flex;
  flex-direction: row;
  flex-wrap: nowrap;
}
```
## flex-flow
The `flex-flow` property is a shorthand for specifying the `flex-direction` and `flex-wrap` properties. Defining `flex-flow` provides the parameters for child elements to be organized across the horizontal and vertical axes.

### Syntax
```
#element-container {
  display: flex;
  flex-flow: <flow-value> <flow-value>;
}
```
A `<flow-value>` can be any of the values available for `flex-direction` and `flex-wrap`:
* `flex-direction`: `row`, `row-reverse`, `column`, `column-reverse`
* `flex-wrap`: `wrap`, `nowrap`, `wrap-reverse`

### Example
Content that is spaced horizontally and wrapping top to bottom:
```
#spam-container {
  display: flex;
  flex-flow: row wrap;
}
```

## justify-content
![justify-content](../images/justify-content.svg)
The `justify-content` defines the alignment along the main axis. It helps distribute extra free space leftover when either all the flex items on a line are inflexible, or are flexible but have reached their maximum size. It also exerts some control over the alignment of items when they overflow the line.

### Syntax
```
#element-container {
  display: flex;
  justify-content: <justify-content-value>;
}
```
The `<justify-content-value>` can be one of the following options:
* `flex-start` (default): items are packed toward the start of the flex-direction.
* `flex-end`: items are packed toward the end of the flex-direction.
* `start`: items are packed toward the start of the writing-mode direction.
* `end`: items are packed toward the end of the writing-mode direction.
* `left`: items are packed toward left edge of the container, unless that doesn’t make sense with the flex-direction, then it behaves like start.
* `right`: items are packed toward right edge of the container, unless that doesn’t make sense with the flex-direction, then it behaves like end.
* `center`: items are centered along the line
* `space-between`: items are evenly distributed in the line; first item is on the start line, last item on the end line
* `space-around`: items are evenly distributed in the line with equal space around them. Note that visually the spaces aren’t equal, since all the items have equal space on both sides. The first item will have one unit of space against the container edge, but two units of space between the next item because that next item has its own spacing that applies.
* `space-evenly`: items are distributed so that the spacing between any two items (and the space to the edges) is equal.

## align-items
![align-items](../images/align-items.svg)

The `align-items` defines the default behavior for how flex items are laid out along the __cross axis__ on the current line. Think of it as the justify-content version for the cross-axis (perpendicular to the main-axis).
### Syntax
```
#element-container {
  display: flex;
  align-items: <align-items-value>;
}
```
The `<align-items-value>` can be one of the following options:
* `stretch` (default): stretch to fill the container (still respect min-width/max-width)
* `flex-start` / `start` / `self-start`: items are placed at the start of the cross axis. The difference between these is subtle, and is about respecting the flex-direction rules or the writing-mode rules.
* `flex-end` / `end` / `self-end`: items are placed at the end of the cross axis. The difference again is subtle and is about respecting flex-direction rules vs. writing-mode rules.
* `center`: items are centered in the cross-axis
* `baseline`: items are aligned such as their baselines align

## align-content
![align-content](../images/align-content.svg)

The `align-content` aligns a flex container’s lines within when there is extra space in the cross-axis, similar to how justify-content aligns individual items within the main-axis.
### Syntax
```
#element-container {
  display: flex;
  align-content: <align-content-value>;
}
```
The `<align-content-value>` can be one of the following options:
* `normal` (default): items are packed in their default position as if no value was set.
* `flex-start` / `start`: items packed to the start of the container. The (more supported) flex-start honors the flex-direction  while start honors the writing-mode direction.
* `flex-end` / end: items packed to the end of the container. The (more support) flex-end honors the flex-direction while end honors the writing-mode direction.
* `center`: items centered in the container
* `space-between`: items evenly distributed; the first line is at the start of the container while the last one is at the end
* `space-around`: items evenly distributed with equal space around each line
* `space-evenly`: items are evenly distributed with equal space around them
* `stretch`: lines stretch to take up the remaining space

### Example
```
#spam-container {
  display: flex;
  flex-direction: row;
  flex-wrap:wrap;
  align-content: space-between;
}
```
## gap, row-gap, column-gap
The `gap` property explicitly controls the space between flex items. It applies that spacing only between items not on the outer edges.

### Syntax
```
#element-container {
  display: flex;
  gap: <gap-value>;
}
```
It is not exclusively for flexbox, gap works in grid and multi-column layout as well.

### Example
```
.container {
  display: flex;
  ...
  gap: 10px;
  gap: 10px 20px; /* row-gap column gap */
  row-gap: 10px;
  column-gap: 20px;
}
```

### Properties for the Children (flex items)
![flex-items](../images/02-items.svg)

## order
![order](../images/order.svg)
By default, flex items are laid out in the source order. However, the order property controls the order in which they appear in the flex container.

### Syntax
#element-container {
  order: <order-value>
}
The `<order-value>` can be one of the following options:
* Number value: `5`

Items with the same order revert to source order.

## flex-grow
![flex-grow](../images/flex-grow.svg)
A property that specifies how much space an item may occupy relative to the other items in the container. An item assigned a flex-grow value of 3, will stretch to occupy 3 times more space than an item assigned a value of 1.

### Syntax
```
#element-container {
  display: flex;
  flex-grow: <flex-value>;
}
```
The `<flex-value>` should be an integer or decimal value. The default value is zero, which limits an item to the initial or default size regardless of the available space.

### Example
Item three will stretch to occupy twice as much space as the other items:

```
#main-container {
  margin: 2% 1% 0 1%;
  display: flex;
  flex-flow: row wrap;
  justify-content: space-around;
  align-items: stretch;
}

#item-1 {
  display: flex;
  flex-grow: 1;
}

#item-2 {
  display: flex;
  flex-grow: 1;
}

#item-3 {
  display: flex;
  flex-grow: 2;
}
```

## flex-shrink
The `flex-shrink` property specifies how much space an item may be scaled down relative to the other items in the container (when items in the flex container are larger than the space available). An item assigned a flex-shrink value of 2, will be scaled twice as much as an item assigned a value of 1.

### Syntax
```
#element-container {
  display: flex;
  flex-shrink: <flex-value>;
}
```
The `<flex-value>` should be an integer or decimal value. The default value is one; therefore, initially all elements in a container will be scaled by the same factor in order to meet the space available.

### Example
An image that will not scale down given flex-shrink conditions:
```
#img-one {
  display: flex;
  flex-shrink: 0;
}
```


## flex-basis
A property that defines the default size of a flex item.
### Syntax
```
#item-a {
  display: flex;
  flex-basis: <flex-value>;
}
```
The `<flex-value>` can be any of the following:
* Grid keyword ( some are not well supported ) : `auto`, `max-content`, `min-content`
* Pixel value: `300px`
* Percent value: `25%`

### Example
An image that has a starting width of 200 pixels:
```
#img-gallery {
  display: flex;
  flex-flow: row wrap;
}

#img-one {
  display: flex;
  flex-basis: 200px;
}
```

## align-self
![align-self](../images/align-self.svg)
The `align-self` allows the default alignment (or the one specified by align-items) to be overridden for individual flex items.

### Syntax
```
#item-a {
  display: flex;
  align-self: <align-self-value>;
}
```
<align-self-value> can have value of `auto`, `flex-start`, `flex-end`,  `center`,  `baseline`, `stretch`;

Note that `float`, `clear` and `vertical-align` have no effect on a flex item.

