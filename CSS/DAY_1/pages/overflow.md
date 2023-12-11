# Overflow
The `overflow` property controls what happens to content that spills, or overflows, outside its box.

The most commonly used values are:
* `hidden` When set to this value, any content that overflows will be hidden from view.
* `scroll`: When set to this value, a scrollbar will be added to the element’s box so that the rest of the content can be viewed by scrolling.
* `visible`: When set to this value, the overflow content will be displayed outside of the containing element. Note, this is the default value.
* `auto`: content will be clipped if it does not fit in the containing block, and a scrollbar will appear if it does.

### Syntax 
```
overflow: <value>;

```

### Example
Clip any content that overflows without providing a scrollbar to view overflow content.

```
.view-box {
  overflow: hidden;
}
```

## overflow-x
Defines how a block level element should handle content that goes beyond its x-axis boundary.

### Syntax
```
overflow-x: <value>;
```

### Example
Provide a scrollbar and clip any content that overflows.
```
.view-box {
  overflow-x: scroll;
}
```

## overflow-y
Defines how a block level element should handle content that goes beyond its y-axis boundary.

```
overflow-y: <value>;
```

### Example
Provide a scrollbar only if overflow contents exists.

```
.view-box {
  overflow-y: auto;
}
```
