# Sizing
The CSS `height` and `width` properties are used to set the height and width of an element. They do not include padding, borders, or margins of the element, but instead, the height/width of the area inside the padding, border, and margin.

The `height` and `width` properties may have the following values:
* `auto` (default): The browser calculates the height and width.
* `length`: Defines the height/width in px, cm, etc.
* `%`: Defines the height/width in percent of the containing block.
* `initial`: Sets the height/width to its default value.
* `inherit`: The height/width will be inherited from its parent value.

### `height`
Defines the height of an element’s content area. The content area is the space inside the padding, border, and margin of the element.
```
height: <value>;
```

where `<value>` can be one of the following:
* Length values: `100px`
* Percentage values: `20%`
* Keyword values: `auto`, `max-content`, `min-content`, `fit-content`

Note: In the case that `box-sizing` is set to `border-box`, the `height` of the element includes the content, padding and border. The `height` property will be overwritten by the `min-height`, and `max-height` properties.

Set the height of the `.box` element to be `100px`:
```
.box {
  height: 100px;
}
```
Set the height of the `.box` element to be `100px` including the padding and the border:
```
.box {
  box-sizing: border-box;
  padding: 20px;
  border: 2px solid black;
  height: 100px;
}
```

### `width`
Defines the width of an element’s content area. The content area is the space inside the padding, border, and margin of the element.

```
width: <value>;
```

where `<value>` can be one of the following:
* Length values: `330px`
* Percentage values: `50%`
* Keyword values: `auto`, `max-content`, `min-content`, `fit-content`


Note: In the case that `box-sizing` is set to `border-box`, the width of the element includes the content, padding and border. The `width` property will be overridden by the `min-width`, and `max-width` properties.

Set the `width` of the `.box` element to be `40em`:
```
.box {
  background-color: blue;
  width: 40em;
}
```
Set the width of the `.box` element to be `100px` including the padding and the border:

```
.box {
  box-sizing: border-box;
  padding: 20px;
  border: 2px solid black;
  width: 100px;
}
```

### `max-height`
Defines the maximum height of an element.

```
max-height: <value>;
```
where `<value>` can be one of the following:
* Length values: `200px`
* Percentage values: `15%`
* Keyword values: `none`, `max-content`, `min-content`, `fit-content`

Note: In the case that `box-sizing` is set to `border-box`, the `max-height` of the element includes the content, padding and border. `max-height` overrides the `height` property. `min-height` overrides `max-height`.

Set the `max-height` of the `.box` element to be `250px`:
```
.box {
  border: 2px solid black;
  max-height: 250px;
}
```

### `max-width`
Defines the maximum width of an element.

```
max-width: <value>;
```
Set the `max-width `of the `.box` element to be `50%`:


```
.box {
  border: 2px solid black;
  height: 100px;
  max-width: 50%;
}
```


#### `min-height`
Defines the minimum height of an element.
```
min-height: <value>;
```

Set the min-height of the `.box` element to be `100px`:

```
.box {
  border: 2px solid black;
  min-height: 100px;
}
```

### `min-width`
Defines the minimum width of an element.
```
min-width: <value>;
```

Set the `min-width` of the `.box` element to be `100px`:
```
.box {
  border: 2px solid black;
  width: 15%;
  min-width: 100px;
}
```

