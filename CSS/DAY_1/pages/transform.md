# Transform Functions
We can transform any HTML element using the `transform` property combined with CSS functions that scale, rotate, and even distort.

These functions apply both 2D and 3D transformations to element.

### Example
```
.shifted {
  transform: translate(0px, 100px);
}
```

## rotate()
The `rotate()` function rotates an element around a fixed point in a two-dimensional space.

### Syntax
```
transform: rotate(<angle>);
```

where a required <angle> can be one of the following:
* Degree value: `90deg`
* Radian value: `0.78rad`
* Gradian value: `200grad`
* Turn value: `.25turn`

### Example
Rotate image 45 degrees clockwise:
```
.hero-image {
  transform: rotate(45deg);
}
```

## scale()
Changes the size of an element to make it larger or smaller.
### Syntax
```
transform: scale(<value>);
```
where a required `<value>` can be one of the following:
* Number value: `.25`, `1.5`
* Percentage value: `25%`, `150%`

__Note__: A single value will be applied to the horizontal and vertical scale of an element. If a second value is provided, the first value will apply to the horizontal scale and the second value will apply to the vertical scale.

### Example
Shrink the .avatar element by `50%`:
```
.avatar {
  transform: scale(50%);
}
```


## skew()
The `skew()` function tilts an element on the x-axis or both the x and y axes on a two-dimensional plane.

### Syntax
```
transform: skew(<angle>);
```
where a required `<angle> `can be one of the following:
* Degree value: `90deg`
* Radian value: `0.78rad`
* Gradian value: `200grad`
* Turn value: `.25turn`

__Note__: If one value is provided, it corresponds to the x-axis. If two values are provided, the first value corresponds to the x-axis and the second value corresponds to the y-axis. Negative values are not allowed.

### Example
Skew our `.rectangle` element along the x-axis by 30deg:
```
.rectangle {
  height: 100px;
  width: 200px;
  background: blue;
  transform: skew(30deg);
}
```

## translate()
The `translate` function moves an element along the X- and/or Y-axis.

### Syntax
```
/* Single value */
transform: translate(<X-value>);

/* Double values */
transform: translate(<X-value>, <Y-value>);
```
The required `<X-value>` or `<Y-value>` can be one of the following:

* Length value: `100px`, `1.5em`
* Percentage value: `25%`, `50%`

A single value will represent only the horizontal axis. Providing a second comma-separated value will represent the vertical axis, as well. As far as the direction goes:

* A positive value moves the element towards the right along the horizontal X-axis or down the vertical Y-axis.
* A negative value moves the element left along the horizontal X-axis or up the vertical Y-axis.

### Example
In the example below, an element with a `.box` class is moved `100px` to the right, along the X-axis:

```
.box {
  transform: translate(100px);
}
```

In this example, the `.box` class element is moved `200px` to the right, along the X-axis, and `100px` up the vertical Y-axis.
```
.box {
  transform: translate(200px, -100px);
}
```

