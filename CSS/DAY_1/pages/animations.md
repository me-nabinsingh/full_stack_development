# Animations
A CSS animation lets an HTML element gradually change from one style to another, without using JavaScript. Any number of CSS properties can be changed, for any amount of times.

To use CSS animation, some keyframes for the animation must be specified.

### @keyframes Rule
Keyframes hold what CSS styles the element will have at certain times. When specifying styles inside the `@keyframes` rule, the animation will gradually change from the current style(s) to the new style(s).

To get an animation to work, the animation must be bound to an element and the animation-duration should be defined. In this example code, the `<h1>` element will load as purple and gradually change to yellow over the course of 5 seconds.

```
/* The animation */
@keyframes color-change {
  from {
    color: purple;
  }
  25% {
    color: orange;
  }
  50% {
    color: red;
  }
  75% {
    color: blue;
  }
  to {
    color: yellow;
  }
}

/* The element */
h1 {
  color: purple;
  animation-name: color-change;
  animation-duration: 5s;
}

```

## @keyframes
Controls an animation with multiple intermediate steps, defining the values of the properties at each keyframe.

### Syntax
```
@keyframes animation-name {
  <keyframe-selector> {
    <keyframe-declaration>
  }
  <keyframe-selector> {
    <keyframe-declaration>
  }
}
```

* `<keyframe-selector>`: The selector for the element(s) to which the keyframe declaration should be applied.
* `<keyframe-declaration>`: The declaration block of the keyframe, made up of the property/value pairs.

__NOTE__: if you are only defining two keyframes, you can use the keywords from and to which are the same as `0%` and `100%` respectively for the `<keyframe-selector>`. Further customization on the animation property allows you to specify how many times an animation should play, duration of animation, change the direction of an animation, and much more.

### Example
Run the keyframes rule fade for a duration of two seconds:
```
div {
  height: 200px;
  width: 200px;
  background-color: black;
  animation-duration: 2s;
  animation-name: fade;
}

@keyframes fade {
  from {
    background-color: black;
  }
  to {
    background-color: white;
  }
}
```

Run the keyframes rule fadeoutfadein for a duration of two seconds:
```
div {
  height: 200px;
  width: 200px;
  background-color: black;
  animation-duration: 4s;
  animation-name: fadeoutfadein;
}

@keyframes fadeoutfadein {
  0% {
    background-color: black;
  }
  20% {
    background-color: white;
  }
  40% {
    background-color: black;
  }
  60% {
    background-color: black;
  }
  80% {
    background-color: white;
  }
  100% {
    background-color: black;
  }
}
```

## animation
Shorthand property that sets the animations for an element.
```
animation: <value>;
```
where `<value>` can be and of the following keywords:
* `animation-fill-mode`: `forwards`
* `animation-delay`: `2s`
* `animation-duration`: `4s`
* `animation-iteration-count`: `infinite`
* `animation-direction`: `alternate`
* `animation-timing-function`: `linear`
* `animation-name`: `keyframes rule`
* `animation-play-state`: `running`

__Note__ : If you do not specify animation-duration property, the default value is 0s, resulting in the animation not being played. The order of time values is important. The first will be applied to animation-duration and the second to animation-delay.

### Example
Set `fadetowhite` animation to run two seconds, loop infinitely, and alternate directions:
```
div {
  height: 100px;
  width: 100px;
  background-color: #000;
  animation: fadetowhite 2s infinite alternate;
}

@keyframes fadetowhite {
  from {
    background-color: #000;
  }
  to {
    background-color: #fff;
  }
}
```

## animation-delay
Defines when an animation starts.

### Syntax
```
animation-delay: <value>;
```

where `<value>` can be one of the following:
* Seconds: `2s`
* Milliseconds: `200ms`

__Note__: If not provided, an animation will occur immediately because the default value is `0s`.

### Example
Wait `2s` then run the animation:
```
div {
  height: 200px;
  width: 200px;
  background-color: blue;
  animation-name: disappear;
  animation-duration: 2s;
  animation-delay: 2s;
}

@keyframes disappear {
  from {
    background-color: blue;
  }
  to {
    background-color: white;
  }
}
```

## animation-direction
Determines whether an animation runs forward or in reverse on some or all of its cycles.
### Syntax
```
animation-direction: <value>;
```
where `<value>` can be one of the following:
* `normal`: Animation will play as specified.
* `reverse`: Animation will be played in the reverse direction as specified.
* `alternate`: causes the cycles to alternate between normal and reverse.
* `alternate-reverse`: causes the cycles to alternate between reverse and normal.

### Example
Reverse the direction of the animation:
```
div {
  height: 200px;
  width: 200px;
  background-color: blue;
  animation-name: slideleft;
  animation-duration: 4s;
  animation-direction: reverse;
}

@keyframes slideleft {
  from {
    margin-left: 100%;
  }
  to {
    margin-left: 0%;
  }
}
```

## animation-duration
Defines how long an animation should take to complete.

### Syntax
```
animation-duration: <value>;
```
where `<value>` can be one of the following:
* Seconds: `2s`
* Milliseconds: `200ms`

__Note__: If not provided, an animation will not occur because the default value is 0s.

### Example
Change color of box from blue to white over a duration of 2 seconds:

```
div {
  height: 200px;
  width: 200px;
  background-color: blue;
  animation-name: disappear;
  animation-duration: 2s;
}

@keyframes disappear {
  from {
    background-color: blue;
  }
  to {
    background-color: white;
  }
}
```

## animation-iteration-count
Defines how many times an animation runs.

### Syntax
```
animation-iteration-count: <value>;
```
where `<value>` can be one of the following:

* Number value: 3, 300
* `inifinite` will run animation on endless loop
__Note__: providing one value will apply to all animation-name values. Additional comma separated values will apply correspondingly.

### Example
Run animation fadeoutfadein two times:
```
div {
  height: 200px;
  width: 200px;
  background-color: blue;
  animation-duration: 2s;
  animation-name: fadeoutfadein;
  animation-iteration-count: 2;
}

@keyframes fadeoutfadein {
  0% {
    background-color: blue;
  }
  50% {
    background-color: white;
  }
  100% {
    background-color: blue;
  }
}
```

## animation-name
Defines a comma-separated list of animations to apply to the given selector.

### Syntax
```
animation-name: <value>;
```
where `<value>` is a `@keyframes` rule, which contains the properties that will be animated.

```
div {
  animation-name: fade;
}

@keyframes fade {
  /* properties: values; */
}
```

### Example
Give the `animation-name` a value of disappear:
```
div {
  height: 200px;
  width: 200px;
  background-color: blue;
  animation-duration: 2s;
  animation-name: disappear;
}

@keyframes disappear {
  from {
    background-color: blue;
  }
  to {
    background-color: white;
  }
}
```

## animation-play-state
Defines whether an animation is running or paused.

### Syntax
```
animation-play-state: <value>;
```

where <value> can be one of the following:
* `paused`: the animation is paused.
* `running`: the animation is running.

### Example
Set animation state to running:
```
div {
  height: 200px;
  width: 200px;
  background-color: blue;
  animation-name: disappear;
  animation-duration: 2s;
  animation-play-state: running;
}

@keyframes disappear {
  from {
    background-color: blue;
  }
  to {
    background-color: white;
  }
}
```

Pause the animation on `div` click:
```
div {
  height: 200px;
  width: 200px;
  background-color: blue;
  animation-name: disappear;
  animation-duration: 4s;
  animation-play-state: running;
}

@keyframes disappear {
  from {
    background-color: blue;
  }
  to {
    background-color: white;
  }
}

```

```
// Target div
const box = document.querySelector('div');
// Pause transition on click
box.addEventListener('click', () => {
  box.style.animationPlayState = 'paused';
});
```

## animation-timing-function
Specifies how intermediate values are calculated throughout the duration of an animation, determining the pacing of the animation. This CSS property influences the speed curve of the animation, controlling its acceleration and deceleration.

### Syntax
```
animation-timing-function: value;

```
where value can be one of the following keywords:
* `step-start`: Easing curve for an animation that starts quickly and decelerates.
* `step-end`: Easing curve for an animation that starts slowly and decelerates.
* `linear`: Easing curve for an animation that maintains a constant speed.
* `ease`: Easing curve for an animation that starts and ends smoothly.
* `ease-in`: Easing curve for an animation that starts slowly and accelerates.
* `ease-out`: Easing curve for an animation that starts quickly and decelerates.
* `ease-in-out`: Easing curve for an animation that starts and ends smoothly.
* `cubic-bezier()`: Easing curve defined using cubic Bezier functions.
__Note__: Applied property by property from keyframe to keyframe.

### Example
Applying `ease-in-out` to the animation-timing-function property of a `div` element:
```
div {
  height: 100px;
  width: 100px;
  border-radius: 50%;
  background-color: blue;
  animation-name: slideright;
  animation-duration: 4s;
  animation-iteration-count: infinite;
  animation-timing-function: ease-in-out;
}

@keyframes slideright {
  0% {
    margin-left: 0%;
  }
  50% {
    margin-left: 50%;
  }
  100% {
    margin-left: 100%;
  }
}
```
