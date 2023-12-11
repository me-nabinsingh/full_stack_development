# Borders
A border is a line that surrounds an element, like a frame around a painting.

Borders can be set with a specific `width`, `style`, and `color`:
* `width`: The thickness of the border. A border’s thickness can be set in pixels or with one of the following keywords: thin, medium, or thick.
* `style`: The design of the border. Web browsers can render any of 10 different styles. Some of these styles include: none, dotted, and solid.
* `color`: The color of the border. Web browsers can render colors using a few different formats, including 140 built-in color keywords.

```
p {
  border: 3px solid coral;
}
```
In the example above, the border has a width of 3 pixels, a style of solid, and a color of coral. All three properties are set in one line of code.

The default border is `medium none color`, where `color` is the current color of the element. If `width`, `style`, or `color` are not set in the CSS file, the web browser assigns the default value for that property.

```
p.content-header {
  height: 80px;
  width: 240px;
  border: solid coral;
}
```
In this example, the border style is set to `solid` and the `color` is set to `coral`. The `width` is not set, so it defaults to `medium`.

### `border`
Shorthand property that sets different properties for an element’s border in a single declaration.

```
border: <values>;
```
The border property accepts one or more of the following properties as values:
* `border-style`(required)
* `border-color`
* `border-width`

Setting a div elements border style to dashed.
```
div {
  /* <border-style> */
  border: dashed;
}
```
Setting an `img` elements border to dotted, red and a width of `20px`.
```
div {
  /* <border-width> | <border-style> | <border-color> */
  border: 20px dotted red;
}
```

### `border-top`
Shorthand property that defines the width, color, and style of the top border of an element.

```
border-top: <value>;
```
where `<value>` can be one of the following:
* Border width: `thick`
* Border style: `dashed`
* Border color: `#f1f1f1`

Note: values can be provided in any order.

Set the top border of the `h1` element to be `green`, `3 pixels thick`, and `dotted`:

```
h1 {
  border-top: green 3px dotted;
}
```
### `border-right`

### `border-bottom`

### `border-left`

### `border-width`
Shorthand property that sets the width for the overall border of an element or for each side individually.

```
/* Keyword values */
border-width: thin;
border-width: medium;
border-width: thick;

/* <length> values */
border-width: 4px;
border-width: 1.2rem;

/* top and bottom | left and right */
border-width: 2px 1.5em;

/* top | left and right | bottom */
border-width: 1px 2em 1.5cm;

/* top | right | bottom | left */
border-width: 1px 2em 0 4rem;

/* Global values */
border-width: inherit;
border-width: initial;
border-width: revert;
border-width: revert-layer;
border-width: unset;
```

The `border-width` property may be specified using one, two, three, or four values.
* When one value is specified, it applies the same width to all four sides.
* When two values are specified, the first width applies to the top and bottom, the second to the left and right.
* When three values are specified, the first width applies to the top, the second to the left and right, the third to the bottom.
* When four values are specified, the widths apply to the top, right, bottom, and left in that order (clockwise).

Set all borders of the h1 element to medium width:
```
h1 {
  border-color: green;
  border-style: dashed;
  border-width: medium;
}
```

### `border-style`
Sets the style of the border. The default value is `none`.
```
where <line-style> can be the following values:

```
* `none`
* `hidden`
* `dotted`
* `dashed`
* `solid`
* `double`
* `groove`
* `ridge`
* `inset`
* `outset`

Set border of the `h1` element to be green, 3 pixels thick, and dotted:

```
h1 {
  border-color: green;
  border-width: 3px;
  border-style: dotted;
}
```

### `border-color`
Sets the color of the border. The default value is the current element color.
```
border-color: <color>;
```
where `<color>` can be one of the following:
* Color keyword: red, transparent, darkblue
* Hexadecimal value: #FF0000
* RGB value: rgb(255, 0, 0)
* RGBA value: rgba(255, 0, 255, 0.3)
* HSL value: hsl(0, 100%, 50%)
* HSLA Value: hsla(180, 80%, 100%, 0.8)

Set the border of the `h1` element to be green, 3 pixels thick, and dotted:

```
h1 {
  border-color: green;
  border-width: 3px;
  border-style: dotted;
}
```

### `border-radius`
The `border-radius` property defines rounded corners on an element. It measures the radii for each corner and can have one to four specified values.
```
/* Four values */
border-radius: <top-left> <top-right> <bottom-right> <bottom-left>;

/* Three values */
border-radius: <top-left> <top-right + bottom-left> <bottom-right>;

/* Two values */
border-radius: <top-left + bottom-right> <top-right + bottom-left>;

/* One value */
border-radius: <all corners>;
```
Both absolute and relative units can be used as values for this property.
```
p {
  border: 1px solid blue;
  border-radius: 10px;
}
```

```
p {
  border: 3px solid black;
  border-radius: 0px 25px;
}
```
Sets a 3-pixel solid black border around each paragraph with 25-pixel rounding only on the top right and bottom left.





