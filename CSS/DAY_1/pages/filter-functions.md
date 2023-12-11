# Filter Functions
The CSS `filter` property applies graphical effects like blur to an element. It is commonly used to adjust the rendering of images, backgrounds, and sometimes even borders.

## blur()
Defines the blur radius of an element.
### Syntax
```
filter: blur(radius);
```
where a required radius is a length value: `0`, `20px`, `2.4em`


### Example
Give the image a blur radius of `4px`:
```
.banner-image {
  filter: blur(4px);
}
```


## brightness()
Defines the brightness or darkness of an element.

### Syntax
```
filter: brightness(<value>);
```
where a required `<value>` can be one of the following:
* Number value: `0`, `1.4`
* Percentage value: `100%`, `50%`
### Example
```
.banner-image {
  filter: brightness(150%);
}
```

## contrast()
Defines the contrast on an element.

### Syntax
```
filter: contrast(<value>);
```
where a required `<value>` can be one of the following:

* Number value: `0`, `1.4`
* Percentage value: `100%`, `50%`
__Note__: Values of `1` and `100%` will have no effect. Values greater than `1` and `100%` will increase the contrast. Values less than `1` and `100%` will decrease the contrast. A value of `0` and `0%` will be completely gray.


### Example
Give the image a contrast of 200%:
```
.banner-image {
  filter: contrast(200%);
}
```


## drop-shadow()
Creates a drop shadow effect on an element.
### Syntax
```
filter: drop-shadow(<offset-h> <offset-v> <blur> <color>);
```
* `<offset-h>` (required): The horizontal offset of the shadow. Negative values will move the shadow to the left.
* `<offset-v>` (required): The vertical offset of the shadow. Negative values will move the shadow up.
* `<blur>` (optional): The blur of the shadow. A default value of 0 will create a hard shadow.
* `<color>` (optional): The color of the shadow. If unset, the value will be the color property value.
### Example
Give the image a drop shadow offset horizontally `-12px`, vertically `-12px` with a `blur` of `2em` and a `color` of `purple`.
```
.banner-image {
  filter: drop-shadow(-12px -12px 2em purple);
}
```

## grayscale()
Converts an element to grayscale.

### Syntax
```
filter: grayscale(<value>);
```
where a required `<value>` can be one of the following:

* Number value: `0`, `.4`
* Percentage value: `100%`, `50%`
__Note__: Values of `0` and `0% `will leave the image unchanged. Values of `1` and `100%` will convert the image to complete grayscale. If a value is omitted, the default value is `1`.


### Example
Give the image a grayscale of 20%:
```
.banner-image {
  filter: grayscale(20%);
}
```


## hue-rotate()
Accepts an angle value and rotates the hue of an element.

### Syntax
```
filter: hue-rotate(<angle>);
```
where a required `<angle>` can be one of the following: `.25turn`, `-45deg`, `1.57rad`, `31.3grad`

__Note__: Positive values increase the hue, negative values decrease the hue. A default value of 0 results in no change.
### Example
Rotate the hue of the image by 45 degrees:
```
.banner-image {
  filter: hue-rotate(45deg);
}
```

## invert()
Inverts the colors of an element.
### Syntax
```
filter: invert(<value>);
```
where a required `<value>` can be one of the following:
* Number value: `0`, `.4`
* Percentage value: `100%`, `50%`
__Note__: A value of `0` and `0%` will leave image unchanged. Values of `1` and `100%` will result in picture completely inverted. Value defaults to `1` and negatives values are not allowed.
### Example
Invert an image `75%`:
```
.banner-image {
  filter: invert(75%);
}
```

## opacity()
Controls how much of the background is visible through the element it is applied to.
### Syntax
```
filter: opacity(<value>);
```
Here the required `<value>` can be one of the following:
* Number value: `0`, `1`
* Percentage value: `25%`, `50%`
__Note__: Value defaults to `1` or `100%`, leaving the element unchanged. A value of 0 and 0% will be completely transparent. Negative values and values greater than `1` or `100%` are not allowed.


### Example
Set the opacity of `banner-image` element to 50%:
```
.banner-image {
  filter: opacity(50%);
}
```



## saturate()
Increase or decrease the intensity of the color of the element it is applied to.

### Syntax
```
filter: saturate(<value>);
```
where a required `<value>` can be one of the following:
* Number value: `0`, `1.5`
* Percentage value: `100%`, `50%`
Note: Value defaults to `1` or `100%` leaving element unchanged. Higher values will increase saturation. A value of `0` and `0%` will remove all color leaving the element completely unsaturated. Negative values are not allowed.

### Example
Set the saturation of a color to `25%`:
```
.banner-image {
  filter: saturate(25%);
}
```


## sepia()
Changes the color of an element to sepia.

### Syntax
```
filter: sepia(<value>);
```
where a required `<value>` can be one of the following:

* Number value: 0, 1
* Percentage value: 10%, 50%
__Note__: Value defaults to `1` or `100%` turning the element to sepia. A value of `0` and `0%` will leave element unchanged. Negative values as well as values greater than `1` or `100%` are not allowed.

### Example
Set sepia to `100%`:
```
.banner-image {
  filter: sepia(100%);
}
```
