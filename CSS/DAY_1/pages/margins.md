# Margins
Margin refers to the space directly outside of the box. The margin property is used to specify the size of this space.

```
p {
  border: 1px solid aquamarine;
  margin: 20px;
}
```

Here, the code will place 20 pixels of space on the outside of the paragraph’s box on all four sides. This means that other HTML elements on the page cannot come within 20 pixels of the paragraph’s border.

If you want to be even more specific about the amount of margin on each side of a box, you can use the following properties:

### margin
Shorthand property for `margin-top`, `margin-bottom`, `margin-left` and `margin-right` to create space around an element or for each side individually.

```
margin: <value>;
```
where `<value>` can be one of the following:
* Keyword: `auto`
* Length: `20px`
* Percentage: `5%`

Note: Providing one value will effect the margin of all sides. Providing two values will result in the first value setting the margin of top and bottom and the second value setting the margin of left and right sides. Three values will result in the first value applied to the top, the second value to the left and right, and the third value applied to the bottom side. Four values will apply to top, right, bottom and left.

Set the margin on all sides to `20px` by providing just one value:
```
h1 {
  background-color: green;
  color: #fff;
  margin: 20px;
}
```

Set the top and bottom margins to `10px` and left and right to `20px` by providing two values:
```
h1 {
  background-color: green;
  color: #fff;
  margin: 10px 20px;
}
```

Set the top margin to `10px`, right and left to `20px` and bottom to `5px` by providing three values:
```
h1 {
  background-color: green;
  color: #fff;
  margin: 10px 20px 5px;
}
```

Set the top margin to `10px`, right to `15px`, left to `20px` and bottom to `5px`:
```
h1 {
  background-color: green;
  color: #fff;
  margin: 10px 15px 20px 5px;
}
```

Center `h1` horizontally:
```
h1 {
  background-color: green;
  color: #fff;
  width: 80%;
  margin: 0 auto;
}
```

### `margin-top`
Defines the top margin area for an element.
```
margin-top: <value>;
```
where `<value>` can be one of the following:
* Length: `20px`
* Percentage: `5%`

Note: values provided may be negative, placing the neighboring element closer.

Set the top margin of the `h1` element to be `20px`:
```
h1 {
  margin-top: 20px;
}
```


### `margin-left`
Defines the left margin area for an element.
```
margin-left: <value>;
```
where `<value>` can be one of the following:
* Length: `20px`
* Percentage: `5%`

Note: values provided may be negative, placing the neighboring element closer.

Set the top margin of the `h1` element to be `20px`:
```
h1 {
  margin-left: 20px;
}
```

### `margin-right`
Defines the right margin area for an element.
```
margin-right: <value>;
```
where `<value>` can be one of the following:
* Length: `20px`
* Percentage: `5%`

Note: values provided may be negative, placing the neighboring element closer.

Set the top margin of the `h1` element to be `20px`:
```
h1 {
  margin-right: 20px;
}
```

### `margin-bottom`
Defines the bottom margin area for an element.
```
margin-bottom: <value>;
```
where `<value>` can be one of the following:
* Length: `20px`
* Percentage: `5%`

Note: values provided may be negative, placing the neighboring element closer.

Set the top margin of the `h1` element to be `20px`:
```
h1 {
  margin-bottom: 20px;
}
```



