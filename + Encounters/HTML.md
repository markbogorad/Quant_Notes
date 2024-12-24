up:: [[Computer Science MOC]]
tags:: #Programming  
# HTML
- HyperText Markup Language
- Used for front end development
	- Enhanced further by [[CSS]] and [[JavaScript]]
## Elements
- HTML documents are made up of elements. These are defined by **tags**, which are enclosed in angle brackets (`< >`). Most elements have an opening tag (e.g., `<p>`) and a closing tag (e.g., `</p>`), with content between them.
- Think of an element as a function block (except these are for design)
## Tags
- The things in between these tags are called **values** and they go straight on the website
- `<html>`: The root element of an HTML document.
- `<head>`: Contains meta-information about the document, such as the title, links to CSS files, and scripts.
- `<title>`: Sets the title of the webpage, which appears in the browser's title bar or tab.
- `<body>`: Contains the content of the webpage, such as text, images, links, and other elements.
- `<h1>` to `<h6>`: Header tags, used to define headings of different levels.
- `<p>`: Paragraph tag, used to define a block of text.
- `<a>`: Anchor tag, used to create **hyperlinks.**
- `<img>`: Image tag, used to embed images in a webpage.
- `<div>`: Division tag, used to group elements for styling and layout purposes.
- `<span>`: Inline tag, used to apply styles to a part of the text or group inline elements.
- `<video>` and inside these do `<source>`: for video links
## Attributes
- **Tags** can have attributes, which provide additional information about an element. Attributes are included within the opening tag and usually come in name/value pairs, such as `class="classname"` or `src="image.jpg"`. Common attributes include:

- `id`: A unique identifier for an element.
- `class`: A class name that can be used to apply CSS styles to groups of elements.
- `src`: The source URL for images, videos, and other embedded content.
- `href`: The URL for a hyperlink.
- `alt`: Alternative text for images, used for accessibility.

## Typical Document Structure
```
<!DOCTYPE html>
<html>
  <head>
    <title>Sample HTML Page</title>
  </head>
  <body>
    <h1>Welcome to My Website</h1>
    <p>This is a paragraph of text on my website.</p>
    <a href="https://www.example.com">Visit Example.com</a>
  </body>
</html>

```
- Follows a tree structure (indentations)
## Tables
```
</head>
<body>
  <h1>Simple Table</h1>
  <table border="1">
    <tr>
      <th>Header 1</th>
      <th>Header 2</th>
      <th>Header 3</th>
    </tr>
    <tr>
      <td>Row 1, Cell 1</td>
      <td>Row 1, Cell 2</td>
      <td>Row 1, Cell 3</td>
    </tr>
    <tr>
      <td>Row 2, Cell 1</td>
      <td>Row 2, Cell 2</td>
      <td>Row 2, Cell 3</td>
    </tr>
  </table>
</body>
```

## Meta tags
- Metadata --> data that provides information about other data
	- Metadata helps search engines understand the content and context of a web page, which can improve the page's visibility and ranking in search results
- **Meta Tags**: HTML uses meta tags to embed metadata within the document's `<head>` section. These tags provide information about the document that is not directly visible to users.
	- Example: `<meta name="twitter:image" content="https://www.example.com/image.jpg">`
## Path key?value
- That is how key value pairs are done in HTML ([[Dictionaries]])
- Distrust user input `?`
- Protects against [[Injection Attacks]]
## Regexes
- **Metacharacters**: Special characters with specific meanings in regex. Some common metacharacters include:
    - `.` (dot): Matches any single character except a newline.
    - `^`: Matches the start of a string.
    - `$`: Matches the end of a string.
    - `*`: Matches 0 or more repetitions of the preceding element.
    - `+`: Matches 1 or more repetitions of the preceding element.
    - `?`: Matches 0 or 1 repetition of the preceding element.
    - `[]`: Matches any one of the characters inside the brackets (character class).
    - `|`: Acts as a logical OR.
    - `()`: Groups patterns together and captures the matched text.
- **Character Classes**: Define a set of characters to match.
    - `[abc]`: Matches any single character a, b, or c.
    - `[a-z]`: Matches any single lowercase letter.
    - `[^abc]`: Matches any character except a, b, or c.
    - `\d`: Matches any digit (equivalent to `[0-9]`).
    - `\D`: Matches any non-digit.
    - `\w`: Matches any word character (alphanumeric plus underscore).
    - `\W`: Matches any non-word character.
    - `\s`: Matches any whitespace character (spaces, tabs, newlines).
    - `\S`: Matches any non-whitespace character.
- **Quantifiers**: Specify how many instances of a character, group, or character class must be present for a match.
    - `*`: 0 or more times.
    - `+`: 1 or more times.
    - `?`: 0 or 1 time.
    - `{n}`: Exactly n times.
    - `{n,}`: n or more times.
    - `{n,m}`: Between n and m times.
- **Anchors**: Assert positions within the text.
    - `^`: Start of a string or line.
    - `$`: End of a string or line.
    - `\b`: Word boundary.
    - `\B`: Non-word boundary.

### Some examples:
- `h.llo` Matches "hello", "hallo", "hxllo", etc.
- `\d+` Matches one or more digits
- `^[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}$` Matches valid email addresses.
- `\(\d{3}\) \d{3}-\d{4}` Matches phone numbers in the format (123) 456-7890.

