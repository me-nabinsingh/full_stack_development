# Math Functions
Performing dynamic mathematical calculations to set property values might sound difficult, but the `calc()` function makes handling mathematical expressions simple and if we want to create responsive elements, the `min()` and `max()` functions are great solutions for setting case-specific design constraints.

## calc()
Performs mathematical calculations to determine values for properties.

### Syntax
```
<property>: calc(<expression>);
```
where `<expression>` can be any simple expression combining the following operators, using standard operator precedence rules:
* `+`: addition.
* `-`: subtraction.
* `*`: multiplication.
* `/`: division.

__Note__: Spaces are required around the `-` and `+` operators. They are not required for `/` and `*` operators.

### Example
Calculate the total width of the div using absolute lengths.
```
div {
  width: calc(10px + 120px);
}
```
This will be `130px` wide.


Set the width property to `10px` less than the CSS variable `--custom-width`:
```
.card {
  --custom-width: 33%;
  width: calc(var(--custom-width) - 10px));
}
```

## clamp()
The `clamp()` function restricts a given value between an upper and lower bound. In this way, it acts like a combination of the `min()` and `max()` functions.

### Syntax
```
<property>: clamp(<lower bound>, <value>, <upper bound>)
```
The `<value>` is valid as long as it is between the `<lower bound>` and `<upper bound>`. This ensures that the `<property>` has a minimum and maximum `<value>`.

Each argument to `clamp()` can be a combination of CSS units, or evaluations of them, using the following:

* Absolute units: `10px`
* Relative units: `40vh`
* Math expressions: `40vw - 20px`
* Nested math function values: `min(20vw, 200px)`

### Example
```
.display-font {
  font-size: clamp(2rem, 3vw, 5rem);
}
```
In the example above, `.display-font` elements will have their font-size clamped down to span `3%` of the viewport’s width. However, it can be no more than `5rem` and no less than `2rem`.

## min()
Sets the smallest value from a list of one or more comma-separated expressions as the value for a CSS property.

### Syntax
```
<property>: max(<expression>, <expression>);
```
where `<expression>` can be one of the following:

* Length values: `10px`
* Relative length values: `40vh`
* Nested math function values: `min(20vw, 200px)`
* Math expressions using arithmetic operators: `40vw - 20px`

### Example
Set the width of the `.box-max` to whichever value is less, `50vw` or `700px`:
```
.box-min {
  background-color: blue;
  height: 100px;
  width: min(50vw, 700px);
}
```

## max()
Sets the largest value from a list of one or more comma-separated expressions as the value for a CSS property.

### Syntax
```
<property>: max(<expression>, <expression>);

```
where `<expression>` can be one of the following:

* Length values: `10px`
* Relative length values: `40vh`
* Nested math function values: `min(20vw, 200px)`
* Math expressions using arithmetic operators: `40vw - 20px`

### Example
Set the width of the `.box-max` to whichever value is greater, `50vw` or `700px`:
```
.box-max {
  background-color: blue;
  height: 100px;
  width: max(50vw, 700px);
}
```
