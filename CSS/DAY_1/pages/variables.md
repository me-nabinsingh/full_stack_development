# Variables
CSS variables are custom properties that are defined in one place and used in multiple places throughout the stylesheet.

### Syntax
CSS variables are used in two principle steps:
1. Define the custom variable inside a selected element
```
element {
  --custom-variable: red;
}
```

2. Use the `var()` function to allow `--custom-variable` to be assigned to a property in multiple elements:
```
elementA {
  background-color: var(--custom-variable);
}

.elementBWithClass {
  background-color: var(--custom-variable);
}

#elementCWithId {
  background-color: var(--custom-variable);
}
```

#### Example
```
.divB {
  --custom-bg-color-saffron: #f4c430;
  background-color: var(--custom-bg-color-saffron);
  position: relative;
  margin: 2em;
  width: 35em;
  height: 35em;
}
```