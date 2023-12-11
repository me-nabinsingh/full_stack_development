# Padding
The space between the contents of a box and the borders of a box is known as padding. Padding is like the space between a picture and the frame surrounding it.

In CSS, you can modify this space with the padding property.
```
p.content-header {
  border: 3px solid coral;
  padding: 10px;
}
```

Here, the code added 10 pixels of space between the content of the paragraph (the text) and the borders, on all four sides.

The padding property is often used to expand the background color and make the content look less cramped.

### `padding`
Shorthand property for `padding-top`, `padding-bottom`, `padding-left` and `padding-right` that sets the space between the content and margin of an element or for each side individually.

```
padding: <value>;

```
where `<value>` can be one of the following:
* Length: `20px`
* Percentage: `5%`

Note: Providing one value will effect the padding of all four borders. Providing two values will result in the first value setting the padding of top and bottom and the second value setting the padding of left and right sides. Three values will result in the first value applied to the top, the second value to the left and right, and the third value applied to the bottom. Four values will apply to top, right, bottom and left.

Set the padding on all sides to `20px`:
```
h1 {
  border: 2px solid green;
  padding: 20px;
}
```
Set the top and bottom padding to be `4px` and left and right to `2px`:
```
h1 {
  border-color: green;
  border-style: dashed;
  padding: 4px 2px;
}
```
Set the top padding to `10px`, right and left to `20px` and bottom to `5px`:
```
h1 {
  border-color: green;
  border-style: dashed;
  padding: 10px 20px 5px;
}
```
Set the top padding to `10px`, right to `15px`, left to `20px` and bottom to `5px`:
```
h1 {
  border-color: green;
  border-style: dashed;
  padding: 10px 15px 20px 5px;
}
```


### `padding-top`
Defines the `width` of the top padding for an element.
```
padding-top: <value>;
```
where `<value>` can be one of the following:
* Length: `20px`
* Percentage: `5%`

Set the top padding of the h1 element to be 20px:
```
h1 {
  padding-top: 20px;
}
```

### `padding-right`

### `padding-bottom`

### `padding-left`







