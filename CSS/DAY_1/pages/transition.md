# Transition
CSS __transitions__ provide a way to control an animation’s speed and timing of the property changes. Instead of having property changes take effect immediately, changes in a property can take place over a period of time.

For example, if the mouse cursor hovers over a link, the link may change color or appearance, and usually the change is instantaneous. With CSS transitions enabled, changes can occur at time intervals that follow an acceleration curve, all of which can be customized.

We can control the following four aspects of an element’s transition:

* How much time there is before a transition begins
* How long a transition lasts
* Which property the transition is for
* How a transition accelerates

## transition
Shorthand property that sets different properties to translate an element in a single declaration.
### Syntax
```
transition: <values>;
```
The `transition` property can have the following properties as values:
* `transition-property`
* `transition-duration`
* `transition-timing-function`
* `transition-delay`
__Note__: The order in which the values are declared does not matter unless a delay is specified. The browser will always recognize the first time value as duration, so to declare a delay value we must first declare a duration value then a delay value.

### Example
Transitioning a `div` elements width from `100px` to `300px` in a linear motion, with a duration of 2 seconds after hovering over the element for 1 second.

```
div {
  height: 100px;
  width: 100px;
  transition: width 2s 1s linear;
}

div:hover {
  width: 300px;
}
```

## transition-delay
The `transition-delay` property specifies how long an element should wait before beginning a transition.
### Syntax
```
transition-delay: <value>;
```
The `transition-delay` value can be specified by one of the following:
* Seconds: 2s
* Milliseconds: 125ms

__Note__: A comma-separated list of values can be used to set different delays for properties of the same element. The delay of all properties will be the same if a single value is provided.

### Example
Specifying a `div` elements left margin transition to wait 200 milliseconds and width transition to wait 1 second before transitioning.
```
div {
  transition-delay: 200ms, 1s;
  transition-property: margin-left, width;
}
```

## transition-duration
The `transition-duration` specifies how long an elements transition should take to complete.

### Syntax
```
transition-duration: <value>;
```
The `transition-duration` value can be specified by one of the following:
* Seconds: 2s
* Milliseconds: 125ms

__Note__: We can give a comma-separated list of values to set different durations for properties of the same element. The duration of all properties will be the same if a single value is provided.

### Example
Setting a `div` element’s height transition to last `4` seconds and color transition to last `200 milliseconds`.
```
div {
  transition-duration: 4s, 200ms;
  transition-property: height, color;
}
```
## transition-property
Specifies the property or properties of an element that a transition effect should apply to.
### Syntax
```
transition-property: <values>;
```
The `transition-property` can have one of the following values:
* `all`: Default value, applies transition effect to all properties.
* `none`: No property will have transitioning effect.
* A single property name (e.g. `height`).
* A comma-separated lost of property names (e.g.`margin-right`, `margin-left`, `width`).

__Note__: Make sure to declare a `transition-duration` property, otherwise the duration will be `0` and have no transitioning effect.

### Example
Setting a `div` element to have a transition effect on its height, width, and top margin properties.
```
div {
  height: 100px;
  width: 100px;
  margin-top: 20px;
  margin-right: 50px;
  background-color: green;
  transition-duration: 2s;
  transition-property: height, width, margin-top;
}

div:hover {
  height: 50px;
  width: 50px;
  margin-top: 40px;
}
```

## transition-timing-function
Specifies the speed of an elements transition effect over the course of its duration.

### Syntax
```
transition-timing-function: <value>;
```
The transition-timing-function can have one of the following values:
* `ease`: Default value, speeds up until the middle of the transition then slows back down at the end.
* `linear`: Same speed from start to end.
* `ease-in`: Starts off slowly then increasing speed until the transition is complete.
* `ease-out`: Starts off quickly then decreasing speed until the transition is complete.
* `ease-in-out`: Starts slowly, then speeds up, then ends slowly.
* `steps(int, start|end)`: A stepping function that takes in two parameters. The first (required) parameter being the number of intervals or steps the transition effect takes to finish. The second parameter, which is optional, takes in either start or end. start will make value changes occur at the beginning of each interval while end will make the changes occur at the end of each interval. If no second parameter is specified, the default value will be end.
* `step-start`: Equal to steps(1, start).
* `step-end`: Equal to steps(1, end);
* `cubic-bezier(p1, p2, p3, p4)`: An author defined curve/speed, where p1 through p3 must be between 0 to 1.

__Note__: The integer value for `steps(int, start|end)` must be greater then `0`.

Make sure to declare a `transition-duration` property, otherwise the duration will be `0` and have no transitioning effect.

### Example
Defining a custom speed for a `p` elements transition effect.
```
p {
  transition-timing-function: ease-in-out;
}
```