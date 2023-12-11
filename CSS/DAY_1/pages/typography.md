# Typography

Typography is the art of arranging text on a page. Some of the most important information a user will see on a web page will be textual.

Styling text to make page content accessible and engaging can significantly improve user experience.

Some of the things that typography can help with:
* How to style and transform fonts.
* How to lay text out on a page.
* How to add external fonts to your web pages.

### `@font-face`
Specifies a custom font to be used to display text.
The `@font-face` rule allows us to use custom fonts instead of just using “web-safe” fonts. We can give the font a name then point to the file in which the font is stored.


```
@font-face {
  font-family: /* Font name */ ;
  src: url(' ') /* Link to font */;
}
```

Creating a custom font called `superFont` then applying the font to a `div`.

```
@font-face {
  font-family: superFont;
  src: url('super_font.ttf');
}

div {
  font-family: superFont;
}
```

### `font`
The `font` property is a shorthand property that sets different properties for an elements `font` in a single declaration.

```
font: <values>;
```
The font property can have the following properties as `<values>`:

Required values:
* `font-family`
* `font-size`

Optional values:

* `line-height`
* `font-weight`
* `font-stretch`
* `font-style`
* `font-varient`

Note: Some edge cases to keep in mind:
* `font-style`, `font-variant`, and `font-weight` must come before `font-size`.
* `line-height` must be declared after `font-size` and only following a forward slash.


```
h1 {
  font: italic 10px/40px Georgia, sans-serif;
}
```
The above would be the same as:

```
h1 {
  font-style: italic;
  font-size: 10px;
  line-height: 40px;
  font-family: Georgia, sans-serif;
}
```

Setting an `h2` font with all seven properties in one declaration.

```
h2 {
  /* font-stretch | font-style | font-varient | font-weight | font-size | line-height | font-family */
  font: expanded italic small-caps bolder 20px/30px cursive;
}
```

### `font-family`
Specify the typeface in a rule set.
```
font-family: <font-family-name>;
```
Set the `h1` tag to `Roboto`:


```
h1 {
  font-family: Roboto;
}
```

### `font-size`
The `font-size` property sets text size. Font size values can be in many different units like absolute lengths and relative lengths.

```
font-size: <font-size-value>;
```

Absolute lengths can be the following:
* `px`
* `in`
* `mm`
* `cm`
* `pt`
* `pc`

Relative lengths can be the following:
* `%`
* `em`
* `rem`
* `ch`
* `ex`
* `vh`
* `vw`
* `vmax`
* `vmin`

Set the `p` tag to `16px`:
```
p {
  font-size: 16px;
}
```

### `font-style`
To set the font style in which text will appear.

```
font-style: <font-style-value>;
```

The `font-style-value` can be the following:
* `normal`
* `oblique`
* `italic`
* `inherit`
* `initial`

Set the `p` tag to `italic`:

```
p {
  font-style: italic;
}
```

### `font-weight`

To set the text to be thicker or thinner.

```
font-weight: <font-weight-value>;
```

The `font-style-value` can be the following:
* `normal`
* `bolder`
* `bold`
* `initial`
* `inherit`
* `lighter`

or can be in the form of numerical values from `100` to `900`. The default value is normal while the default numerical value is `400`.

Set the `p` tag to `bold`:
```
p {
  font-weight: bold;
}
```

### `letter-spacing`
Set the horizontal spacing between the individual characters in an element.

```
letter-spacing: <letter-spacing-value>;
```

The CSS units for `letter-spacing-value` can be:
* `px`
* `em`

Set the letter space between letters in `p` tag to `15px`:

```
p {
  letter-spacing: 15px;
}
```


### `line-height`
Set the vertical spacing between lines of text.
```
line-height: <line-height-value>;
```

The `line-height-value` do not accept negative value. The `line-height-value` can be in any CSS units such as:
* `px`
* `rem`
* `em`
* `%`

Set the line height on `p` tag to `10px`:
```
p {
  line-height: 10px;
}
```

### `text-align`
To set the text alignment of inline contents.
```
text-align: <text-align-value>;
```
The `text-align-value` can be the following:
* `left`
* `center`
* `right`

Set the `p` tag to `center`:
```
p {
  text-align: center;
}
```
### `text-decoration`
To add lines on the text.
```
text-decoration: <text-align-value>;
```
The `text-decoration-value` can be the following:
* `none`
* `underline`
* `overline`
* `line-through`

Set the `p` tag to `center`:
```
p {
  text-decoration: underline;
}
```
### `text-indent`
The `text-indent` leaves empty space on the first line in a text-block.
```
text-indent: <value>;
```
The amount of indentation can be specified by using percentages or length values (`px`, `em`, etc.).
```
p {
  text-indent: 20%;
}
```

### `text-justify`
Sets the justifcation method of text when `text-align: justify;` is applied to an element.
```
text-justify: <value>;
```
The following values can be be appplied to the `text-justify` property:
* `none`: Disables justification methods.
* `inter-word`: Adjusts the spacing between words.
* `inter-character`: Adjusts the spacing between characters.
* `auto`: Allows the browser to determine the justification method.

Setting a `p` element with a justifaction of `inter-word`:
```
p {
  text-align: justify;
  text-justify: inter-word;
}
```

### `text-overflow`
Specifies how hidden content is signaled to the user.

```
text-overflow: <value>;
```

The following values can be be appplied to the `text-overflow` property:
* `clip`: Default value. Cuts off/hides the overflowing content.
* `ellipsis`: Displays an ellipsis, `“…”`.
* `" "`: A custom string set by the author.

Note: The properties `white-space: nowrap;` and `overflow: hidden;` are required for `text-overflow` to work.

```
div {
  text-overflow: ellipsis;

  /* Additional properties required for text-overflow to function: */
  overflow: hidden;
  white-space: nowrap;
}
```

### `text-shadow`
Adds shadow to text.
```
text-shadow: 2px 4px 10px blue;
```
The shadow is created with a combination of `x` and `y` offsets from the element, blur radius, and color:
* value 1 (required): Offsets the x-axis.
* Value 2 (required): Offsets the y-axis.
* Value 3 (optional): Sets the blur radious.
* Value 4 (optional): Sets the color of the shadow.

Note: We can add multiple text shadows by comma separating.

Creating a basic text shadow.

```
h1 {
  /* x-offset | y-offset */
  text-shadow: 2px 4px;
}
```

Creating a text shadow with blur effect and blue color.
```
h1 {
  /* x-offset | y-offset | blur-radius | color */
  text-shadow: 2px 4px 10px blue;
}
```

Adding multiple text-shadows.
```
h1 {
  /* x-offset | y-offset | blur-radius | color */
  text-shadow: 2px 4px 10px #00e9ec, 3px 6px 5px green;
}
```


### `text-transform`
Specifies how to capitalize an element’s text.
```
text-transform: <value>;
```

The following values can be be appplied to the `text-transform` property:
* `none` (default): The text renders as is.
* `capitalize`: Transforms the first character of every word to uppercase.
* `uppercase`: Transforms all characters to uppercase.
* `lowercase`: Transforms all characters to lowercase.

Transforming every character of a text block to uppercase.

```
p {
  text-transform: uppercase;
}
```

### `word-spacing`
The word-spacing attribute is used to set the size of spaces between words.
```
word-spacing: <word-spacing-value>;
```

The CSS units for `word-spacing-value` can be:
* `px`
* `em`

Set the space between the words to `0.5em`:
```
p {
  word-spacing: 0.5em;
}
```
Note: For word spacing, using em values are recommended because the spacing can be set to match the size of the font.

