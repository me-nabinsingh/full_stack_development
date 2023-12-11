# Pseudo-elements
A CSS pseudo-element is a keyword added to a selector that lets you style a specific part of the selected element(s).

### Syntax
```
selector::pseudo-element {
  property: value;
}
```

For example, `::first-line` can be used to change the font of the first line of a paragraph.

```
/* The first line of every <p> element. */
p::first-line {
  color: blue;
  text-transform: uppercase;
}
```

Double colons (`::`) are used for pseudo-elements. This distinguishes pseudo-elements from pseudo-classes that use single colon (`:`) in their notation.

You can use only one pseudo-element in a selector. The pseudo-element must appear after all the other components in the complex or compound selector in which it appears. 


### List of pseudo-elements
* `::after` - In CSS, `::after` creates a pseudo-element that is the last child of the selected element. It is often used to add cosmetic content to an element with the content property. It is inline by default.

* `::backdrop` - The `::backdrop` CSS pseudo-element is a box the size of the viewport, which is rendered immediately beneath any element being presented in the top layer.


* `::before` - In CSS, `::before` creates a pseudo-element that is the first child of the selected element. It is often used to add cosmetic content to an element with the content property. It is inline by default.


* `::cue` - The `::cue` CSS pseudo-element matches WebVTT cues within a selected element. This can be used to style captions and other cues in media with VTT tracks.


* `::cue-region` - The `::cue-region` CSS pseudo-element matches WebVTT cues within a selected element. This can be used to style captions and other cues in media with VTT tracks.


* `::first-letter` - The `::first-letter` CSS pseudo-element applies styles to the first letter of the first line of a block container, but only when not preceded by other content (such as images or inline tables).


* `::first-line` -The `::first-line` CSS pseudo-element applies styles to the first line of a block container.


* `::file-selector-button` - The `::file-selector-button` CSS pseudo-element represents the button of an `<input>` of `type="file"`.


* `::marker` - The `::marker` CSS pseudo-element selects the marker box of a list item, which typically contains a bullet or number. It works on any element or pseudo-element set to display: list-item, such as the` <li>` and `<summary>` elements.

* `::placeholder` - The `::placeholder` CSS pseudo-element represents the placeholder text in an `<input>` or `<textarea>` element.
* `::selection` - The `::selection` CSS pseudo-element applies styles to the part of a document that has been highlighted by the user (such as clicking and dragging the mouse across text).