# Internal Stylesheet
HTML allows you to write CSS code in its own dedicated section with a` <style>` element nested inside of the `<head>` element. The CSS code inside the `<style>` element is often referred to as an internal stylesheet.

To create an internal stylesheet, a `<style>` element must be placed inside of the `<head>` element.
```
<head>
  <style>


  </style>
</head>
```

After adding opening and closing `<style>` tags in the head section, you can begin writing CSS code.

```
<head>
  <style>
    p {
      color: red;
      font-size: 20px;
    }
  </style>
</head>
```