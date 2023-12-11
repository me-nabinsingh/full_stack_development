# Selectors

Selectors are used to style HTML elements according to their type and/or attributes.

All markups can be selected with the `*` selector:

```
* {
  /* declarations here */
}
```

### Selecting by Type
The element selector selects HTML elements based on the element name.

```
element-name {
  /* declarations here */
}
```

The `element-name` must be a valid HTML element.

In the following example, all of the `<p>` elements on the page will be centered with a red text color:

```
p {
  text-align: center;
  color: red;
}
```

### Selecting by Attribute
The `class` selector selects elements that are assigned a `class` attribute, it can be used across multiple elements, and begins with a period, `.`. Similarly, the `id` selector selects an HTML element that has an `id` attribute. In contrast, the `id` selector can only be applied once and begins with the hashtag symbol, `#`.


```
#id-name {
  /* declarations here */
}

.class-name {
  /* declarations here */
}

element[attribute='value'] {
  /* declarations here */
}
```

The `id` of an element is unique within a page, so the `id` selector is used to select one unique element. An element can be selected with a specific `id`, by using a hash (`#`) character, followed by `id-name`.

Multiple `class` values can be assigned to a single element. Elements are selected by `class` with a period (`.`) character, followed by` class-name`. Unlike id values, `class` values can be duplicated on a page with different elements.


The following rules select elements based on `id`, `class`, and other attributes:

```
#para1 {
  text-align: center;
  color: red;
}

.center {
  text-align: center;
  color: red;
}

li[title='red'] {
  background-color: red;
  color: #fff;
}
```

It can also be specified that only certain HTML elements with a given class should be styled. For example, here, only `<p>` tags with a `class` of `"center"` will have its text center-aligned:

It can also be specified that only certain HTML elements with a given class should be styled. For example, here, only `<p>` tags with a class of "center" will have its text center-aligned:

```
p.center {
  text-align: center;
  color: red;
}
```

