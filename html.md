# HTML Guide
We follow these guidelines to ensure that every engineer produces quality code, consistently.

Strive for your code to be:
* Semantic
* Reusable
* Scalable
* Flexible
* Maintainable
* Understandable
* Optimized
* Accessible

## HTML Style Guide

### BOOLEAN ATTRIBUTES
Boolean attributes should not have a value.
```html
<input type="text" disabled>
```

### CAPITALIZATION
Use only lowercase, unless it's for a string.
```html
<img src="logo.jpg" class="logo" alt="logo">
```

### CLOSING TAGS
Any element with an opening tag needs a closing tag. 
```html
<p>Close this paragraph tag.</p>
```
With HTML5, the trailing slash on self-closing tags is now optional. If you're using HTML5, it's good practice not to use trailing slashes. No need to use code that's not needed.

**No**
```html
<img src="logo.jpg" />
<input type="text" />
<br />
```
**Yes**
```html
<img src="logo.jpg">
<input type="text">
<br>
```

### COMMENTS
Use standard HTML comments liberally to add structure and clarity to your code.
```html
<!-- Start of main content -->
<section class="b-main-content">...</section>
<!-- End of main content -->
```

### DOCTYPES
Use the HTML5 doctype.
```html
<!doctype html>
```

**Resources**
* https://www.w3schools.com/tags/tag_doctype.asp

### ENCODING
Use UTF-8 encoding. This meta tag should be the first element inside the document's `<head>` element.
```html
<meta charset="utf-8">
```

### HTML ENTITIES
Use appropriate HTML entity names or numbers for special characters.
```html
&copy; 2022 Company Name &#8212; All Rights Reserved;
```

**Resources**
* https://www.freeformatter.com/html-entities.html

### HTML TEMPLATING LANGUAGES
Use a HTML templating language like Slim, Haml, or Jade when possible. Ain't nobody got time to write standard HTML and deal with closing tags.

### HTML5 ELEMENTS
Use HTML5 elements where possible. Some such as `<canvas>` and `<video>` have limited browser support at this time. If you use elements with limited support, always be sure to include a fallback. If you're unsure about an elements support, use the resource below.

**Resources**
* http://caniuse.com

### HTML5 FORM VALIDATION
By default, many HTML5 form inputs include validation that is provided by the browser. In many cases the browser implemented messages are not desired and/or your application may have it's own validation and error messaging in place. In order to remove validation (and thereby the default browser messages) use the `novalidate` attribute on the containing form.
```html
<form action="#" method="post" novalidate>
  <label for"email">Email Address:</label>
  <input type="email" placeholder="Enter a valid email address" id="email">
  <button type="submit">Submit</button>
</form>
```

### IMAGE FORMATS
Know the pros/cons of each image format and use whatever best suits your needs. In general at Blink we use:
* .jpg
* .png
* .svg
* .gif

**Resources**
* https://en.wikipedia.org/wiki/Image_file_formats

### INDENTATION
Use 2 spaces for indentation in your editor of choice.

### QUOTES
Use double quotes around attribute values.
```html
<input type="text" class="search">
```

### SEMANTIC MARKUP
Write clean, semantic markup that adds structure and clarity to the code. Just as important, it should also reinforce the meaning of the page content.
```html
<main>
  <section class="about">
    <article>
      <h1>About Us</h1>
      <p>We are a passionate, ambitious, and collaborative team with revolutionary clients.</p>
    </article>
  </section>
</main>
```

**Resources**
* http://www.hongkiat.com/blog/html-5-semantics
* https://css-tricks.com/video-screencasts/100-lets-write-semantic-markup

### TABLES
Tables should only be used for tabular data and never, ever used for page layouts. Below is standard markup for a table. The tags `<thead>` and `<tfoot>` can be omitted if the table doesn't have a header or footer.
```html
<table>
  <thead>
    <tr>
      <th>Merchant</th>
      <th>Product</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Amazon</td>
      <td>15" Macbook Pro</td>
    </tr>
  </tbody>
</table>
```

### TODO COMMENTS
Mark todos and action items with a comment that includes `TODO`. Be sure that `TODO` is always uppercase.
```html
<!-- TODO - refactor later with HTML5 tags -->
<div class="main-content">
  <div class="article">...</div>
</div>
```

### TRAILING WHITESPACE
Remove all trailing whitespace.

### TYPE ATTRIBUTES
**HTML5 Doctype**

When working with HTML5, the `type` attribute is no longer needed for stylesheets and scripts.
```html
<link rel="stylesheet" href="main.css">
<script src="main.js">
```
**Legacy Doctypes**

When working with doctypes older than HTML5, the `type` attribute is required.
```html
<link rel="stylesheet" href="main.css" type="text/css" />
<script src="main.js" type="text/javascript" />
```

### W3C VALIDATION
* Write valid code.
* Remaining errors and warnings should be intentional.

**Resources**
* http://validator.w3.org
