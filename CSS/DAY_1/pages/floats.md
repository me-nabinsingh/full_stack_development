# Floats
The float property moves an element to the left or right within its containing element, outside of the default positioning.
```
float: <value>;
```
The following values can be be appplied to the float property:
* `right`: The element floats on the right side of its container.
* `left`: The element floats on the left side of its container.
* `none`: The default value, ensures the element will not float left or right.

Making an `img` element `float` to the `left` of its container.
```
.container {
  height: 200px;
  width: 200px;
}

.container img {
  float: left;
}
```
