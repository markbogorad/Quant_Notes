up:: [[Computer Science MOC]]
tags:: #Programming  
# Cascading Style Sheets (CSS)
- Styles [[HTML]] code
- Cascading --> implies a waterfall effect
	- What you do early will apply to future movements
## Basic Structure
```
selector {
  property: value;
  property: value;
}


- For example:


/* CSS */
body {
  background-color: lightblue;
}

h1 {
  color: navy;
  margin-left: 20px;
}
```
- A selector is what you are styling
- Property is the subsection (ex background color)
- Value is the CSS specific style you choose
## Main Attributes
-  `href` attribute (short for "hypertext reference") specifies the **URL** of the page or resource that the link or anchor element points to. It is most commonly used with the `<a>` (anchor) and `<link>` tags.
- `rel` attribute specifies the **relationship** between the current document and the linked document/resource. It is commonly used with the `<link>` and `<a>` tags.
- `style` attribute is used to apply inline CSS styles directly to an HTML element. This attribute contains CSS properties and values.
	- Ex: `<p style="color: blue; font-size: 20px;">This is a styled paragraph.</p>`
- `class` attribute is used to assign one or more class names to an HTML element. These class names can then be referenced in CSS and [[JavaScript]] to apply styles or manipulate elements.
## Weaving into [[HTML]]
```
<html>
<head>
  <style>
    body {
      background-color: lightblue;
    }
    h1 {
      color: navy;
      margin-left: 20px;
    }
  </style>
</head>
<body>
  <h1>Hello World</h1>
</body>
</html>

```

## External CSS Linking
```
<html>
<head>
  <link rel="stylesheet" type="text/css" href="styles.css">
</head>
<body>
  <h1>Hello World</h1>
</body>
</html>

```