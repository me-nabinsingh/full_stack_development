# SASS
__SASS (Syntactically Awesome Style Sheets)__ is a preprocessor scripting language that extends CSS. It provides additional features and capabilities to make writing CSS more efficient and maintainable. SASS files are compiled into regular CSS before being used by web browsers.

__Note__: SASS has two syntaxes: SCSS (.scss) and indented syntax (.sass). SCSS (Sassy Cascading Style Sheets) is the most commonly used and is similar to CSS, allowing code to be written with curly braces and semicolons. The indented syntax is less common and uses indentation and newlines instead of curly braces and semicolons. Both syntaxes are supported, and the examples are available in both formats.

### SASS Example
```
.container
  width: 100%
  margin: 0 auto
  padding: 20px

.title
  font-size: 24px
  color: #333
```

### SCSS Example
```
.container {
  width: 100%;
  margin: 0 auto;
  padding: 20px;
}

.title {
  font-size: 24px;
  color: #333;
}
```

## Key Features
### Variables
SASS allows for the definition of reusable variables, making it easy to store and reuse values in stylesheets.
```
$primary-color: #007bff;
$font-size: 16px;

.container {
  background-color: $primary-color;
  font-size: $font-size;
}

.heading {
  color: $primary-color;
  font-size: $font-size + 4px;
}
```
### Nesting
SASS allows nesting of selectors inside one another, providing a cleaner and more readable structure.
```
.container {
  width: 100%;

  .header {
    background-color: #007bff;
    color: #fff;
  }

  .content {
    padding: 20px;

    .section {
      margin-bottom: 20px;
    }
  }
}
```

### Mixins
SASS supports mixins, which are reusable blocks of styles that can be included in different selectors, promoting code reuse.
```
@mixin button {
  padding: 10px 20px;
  background-color: #007bff;
  color: #fff;
  border: none;
}

.button {
  @include button;
}

.special-button {
  @include button;
  font-weight: bold;
}
```

### Partials and Import
SASS allows the splitting of stylesheets into smaller modular files called partials. These partials can be imported into other SASS files using the @import syntax. By prefixing partial filenames with an underscore (_partial.scss), it indicates that they are not meant to be compiled into a separate CSS file. This modular approach, often referred to as partials, helps organize styles and promote reusability in SASS development.


```
// _variables.scss (Partial)
$primary-color: #007bff;
$font-size: 16px;

// main.scss (Main file)
@import 'variables';

.container {
  background-color: $primary-color;
  font-size: $font-size;
}

// _buttons.scss (Partial)
.button {
  padding: 10px 20px;
  background-color: $primary-color;
  color: #fff;
  border: none;
}

// main.scss (continued)
@import 'buttons';

.special-button {
  font-weight: bold;
  @extend .button;
}
```

### Extensions and Inheritance
SASS provides the ability to extend and inherit styles, reducing code duplication.
```
// Base styles for buttons
.button {
  padding: 10px 20px;
  background-color: #007bff;
  color: #fff;
  border: none;
}

// Extend the base button styles for a special button
.special-button {
  @extend .button;
  font-weight: bold;
}

// Extend the base button styles for a disabled button
.disabled-button {
  @extend .button;
  opacity: 0.5;
  cursor: not-allowed;
}
```


### Operators
Operators in SASS are symbols that perform mathematical operations on values. They include arithmetic operators ( `+`, `-`, `*`, `/`), comparison operators (`==`, `!=`, `>`, `<`), and logical operators (`and`, `or`, `not`). They enable dynamic calculations and conditional logic within SASS stylesheets.
```
// Define variables
$width: 200px;
$padding: 20px;
$font-size: 16px;

// Perform calculations using operators
.container {
  width: $width + 50px;
  padding: $padding / 2;
  font-size: $font-size * 1.2;
}

// Use comparison operator
.success {
  color: green;
  background-color: if($width > 300px, yellow, white);
}
```
