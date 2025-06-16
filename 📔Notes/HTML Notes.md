# [HTML Tutorial](https://www.apnacollege.in/path-player?courseid=sigma-8&unit=6848419f13c68876f906b4f8Unit)

## [What is HTML?](https://blog.hubspot.com/blog/tabid/6307/bid/5847/a-marketer-s-guide-to-html5.aspx)
**HTML** stands for **HyperText Markup Language**. HTML is the **foundation of every web page**. It is the **standard language used to create and structure content on the web**. It is **not a case sensitive language**.

### Key Points about HTML

- **HyperText**: Refers to the ability to link to other documents or web pages.

- **Markup Language**: Uses tags to "mark up" content so browsers can display it correctly.

---

## How to see HTML code in web page?
To see the HTML code of a web page, you can use the **developer tools** in web browser. Here is how to do it:

1) **Right-click** on any part of the web page.

2) Select **"Inspect"** or **"Inspect Element"**.

3) The **Developer Tools** panel will open, highlighting the HTML element you clicked on.
 ---

## HTML Elements
HTML (HyperText Markup Language) elements are the building blocks of web pages. Each element usually consists of a **start tag**, **content**, and an **end tag**. Some standard elements that browser recognizes:

- *Paragraph:* `<p>This is a paragraph</p>`

- *Heading:* `<h1>This is the Largest Heading</h1>`

- *Image:* `<img src='image.png' alt='This is an image'>`

 There are **two types** of element:

1) **Block Elements:** Takes up the full width available (whole block). Examples:
	
	- Heading elements
	
	- Paragraph element

2) **Inline Elements:** Takes up only necessary width. Examples:
	
	- Image element
	
	- Anchor element

---

## HTML Tags
The **component** used to designed the structure of websites are called **HTML tags**.**Tag** is a **container** for some **content** or **other tags**.
An **HTML tag** consists of **angle brackets** and a **tag name**. There are **three types** of tag:

- **Opening tag:** `<tagname>`

- **Closing tag:** `</tagname>`

- **Self-closing tag (void tag):** `<tagname />` (or just `<tagname>` in HTML5) 
 ![[Screenshot From 2025-06-11 18-30-19.png]]

### Some common HTML tags

#### 📄 **Document Structure**

| Tag          | Description               | Example                  |
| ------------ | ------------------------- | ------------------------ |
| `<!DOCTYPE>` | Document type declaration | `<!DOCTYPE html>`        |
| `<html>`     | Root element              | `<html> ... </html>`     |
| `<head>`     | Metadata container        | `<head> ... </head>`     |
| `<title>`    | Page title                | `<title>My Page</title>` |
| `<body>`     | Page content              | `<body> ... </body>`     |

#### ✍️ **Text and Formatting**

| Tag           | Description      | Example                                 | Facts                                                  |
| ------------- | ---------------- | --------------------------------------- | ------------------------------------------------------ |
| `<h1>`–`<h6>` | Headings         | `<h1>Hello</h1>`                        | It has six different level                             |
| `<p>`         | Paragraph        | `<p>This is a paragraph.</p>`           | Doesn't count extra spaces                             |
| `<b>`         | Bold emphasis    | `<b>Important</b>`                      | Also called 'strong'                                   |
| `<i>`         | Italic emphasis  | `<i>Emphasized</i>`                     | Also called 'em'                                       |
| `<u>`         | Underline        | `<>Underlined text</u>`                 |                                                        |
| `<br>`        | Line break       | `First line<br>Second line`             | It is a void tag                                       |
| `<hr>`        | Horizontal line  | `<hr>`                                  | It is a void tag                                       |
| `<sup>`       | Superscript text | `<sup>This is a superscript text</sup>` | It make the text smaller and lifted                    |
| `<Sub>`       | Subscript text   | `<sub>This is a subscript text</sub>`   | It make the text smaller and at the foot of other text |

#### 🔗 **Links & Media**

| Tag        | Description         | Example                             |
| ---------- | ------------------- | ----------------------------------- |
| `<a>`      | Hyperlink           | `<a href="url">Link</a>`            |
| `<img>`    | Image (void)        | `<img src="img.jpg" alt="...">`     |
| `<video>`  | Video embed         | `<video src="vid.mp4"></video>`     |
| `<audio>`  | Audio embed         | `<audio src="sound.mp3"></audio>`   |
| `<iframe>` | Embed page or media | `<iframe src="page.html"></iframe>` |

#### 📋 **Forms & Input**

| Tag          | Description        | Example                                 | Facts                                                                               |
| ------------ | ------------------ | --------------------------------------- | ----------------------------------------------------------------------------------- |
| `<form>`     | Form container     | `<form>...</form>`                      |                                                                                     |
| `<input>`    | Input field (void) | `<input type="text">`                   |                                                                                     |
| `<label>`    | Input label        | `<label for="name">Name</label>`        | **For** attribute value should be equal to **id** attribute value of input          |
| `<textarea>` | Multi-line input   | `<textarea></textarea>`                 | The predefined area = 100 * 2. We can change it using **cols** & **rows** attribute |
| `<select>`   | Dropdown           | `<select><option>...</option></select>` |                                                                                     |
| `<button>`   | Button             | `<button>Submit</button>`               |                                                                                     |

#### 🧱 **Layout and Structure**

| Tag         | Description           | Example                  | Facts                          |
| ----------- | --------------------- | ------------------------ | ------------------------------ |
| `<div>`     | Block-level container | `<div>...</div>`         | It is content division element |
| `<span>`    | Inline container      | `<span>text</span>`      | It is content division element |
| `<section>` | Thematic grouping     | `<section>...</section>` |                                |
| `<article>` | Independent content   | `<article>...</article>` |                                |
| `<nav>`     | Navigation links      | `<nav>...</nav>`         |                                |
| `<header>`  | Section/page header   | `<header>...</header>`   |                                |
| `<footer>`  | Section/page footer   | `<footer>...</footer>`   |                                |

#### 🗒️ Lists

| Tag    | Description       | Example           | Facts                                                            |
| ------ | ----------------- | ----------------- | ---------------------------------------------------------------- |
| `<ul>` | Unordered list    | `<ul>...</ul>`    | Creates bullet type list (dot, circle, disk, square)             |
| `<ol>` | Ordered list      | `<ol>...</ol>`    | Create list with number, alphabet, roman numbers                 |
| `<li>` | Show list element | `<li>Orenge</li>` | Also called 'list'. It should be inside of `<ol>` or `<ul>` tags |

#### 📊 **Tables**

| Tag       | Description        | Example              | Facts              |
| --------- | ------------------ | -------------------- | ------------------ |
| `<table>` | Table container    | `<table>...</table>` |                    |
| `<tr>`    | Table row          | `<tr>...</tr>`       |                    |
| `<td>`    | Table cell         | `<td>Cell</td>`      |                    |
| `<th>`    | Table header cell  | `<th>Heading</th>`   |                    |
| `<thead>` | Table head group   | `<thead>...</thead>` | Semantics in table |
| `<tbody>` | Table body group   | `<tbody>...</tbody>` | Semantics in table |
| `<tfoot>` | Table footer group | `<tfoot>...</tfoot>` | Semantics in table |

#### ⚙️ **Meta and Scripts**

| Tag        | Description       | Example                                    |
| ---------- | ----------------- | ------------------------------------------ |
| `<meta>`   | Metadata (void)   | `<meta charset="UTF-8">`                   |
| `<link>`   | External resource | `<link rel="stylesheet" href="style.css">` |
| `<style>`  | Internal CSS      | `<style>body {}</style>`                   |
| `<script>` | JavaScript        | `<script>console.log()</script>`           |

---

## HTML Attributes
HTML **attributes** provide **additional information** about HTML elements. They are always included **in the opening tag** and follow this pattern:
```
<tagname attribute="value">Content</tagname>
```

###  Common HTML Attributes

| Attribute | Description                       | Example                              |
| --------- | --------------------------------- | ------------------------------------ |
| `id`      | Unique identifier for an element  | `<div id="header">`                  |
| `class`   | Class name for CSS/JavaScript     | `<p class="intro">`                  |
| `style`   | Inline CSS style                  | `<h1 style="color:red;">`            |
| `title`   | Tooltip on hover                  | `<a title="Go to homepage">Home</a>` |
| `lang`    | Language of the element's content | `<html lang="en">`                   |

#### 🔗 Anchor (`<a>`) Tag Attributes

| Attribute | Description                                | Example                          |
| --------- | ------------------------------------------ | -------------------------------- |
| `href`    | URL to link to                             | `<a href="https://example.com">` |
| `target`  | Where to open the link (`_blank`, `_self`) | `<a target="_blank">`            |
| `rel`     | Relationship (e.g. `nofollow`, `noopener`) | `<a rel="noopener">`             |

#### 🖼️ Image (`<img>`) Tag Attributes

| Attribute        | Description         | Example                   |
| ---------------- | ------------------- | ------------------------- |
| `src`            | Image URL           | `<img src="image.jpg">`   |
| `alt`            | Alternative text    | `<img alt="Description">` |
| `width`/`height` | Size in pixels or % | `<img width="100">`       |

#### 📽️ Video (`<video>`) Tag Attributes

| Attribute                 | Description                     | Example                             | Facts                                              |
| ------------------------- | ------------------------------- | ----------------------------------- | -------------------------------------------------- |
| `controlslist`            | Select controls                 | `<video controlslist="nodownload">` | The allowed values are `nodownload, nofullscreen ` |
| `disablepictureinpicture` | Disable picture-in-picture mode | `<video disablepictureinpicture>`   | It is a Boolean attribute                          |
| `height`                  | Height adjustment               | `<video hight="250px">`             |                                                    |
| `width`                   | Width adjustment                | `<video width="250px">`             |                                                    |
| `loop`                    | Automatic playback              | `<video loop>`                      |                                                    |
| `muted`                   | Automatic mute                  | `<video muted>`                     |                                                    |
| `src`                     | Source for the video            | `<video src="video.mp4">`           | Also use `<source>` tag inside `<video>` tag       |

### Table attributes

| Attribute | Description                                    | Example                  | Facts                               |
| --------- | ---------------------------------------------- | ------------------------ | ----------------------------------- |
| `border`  | Specifies width of the border around the table | `<table border="black">` | Use CSS instead                     |
| `colspan` | Number of columns a cell should span           | `<th colspan="2">`       | How many columns a cell should span |
| `rowspan` | Number of rows a cell should span              | `<td rowspan="2">`       | How many rows a cell should span    |

#### 📋 Form Input Attributes
**Form** element has only one attribute which is **for**. Its value indicates where form data should go.

| Attribute     | Description                           | Example                            | Facts                                 |
| ------------- | ------------------------------------- | ---------------------------------- | ------------------------------------- |
| `type`        | Input type (`text`, `password`, etc.) | `<input type="text">`              |                                       |
| `name`        | Field name for submission             | `<input name="username">`          | Every same name element is connected. |
| `placeholder` | Hint text inside input                | `<input placeholder="Enter name">` |                                       |
| `value`       | Pre-filled value                      | `<input value="John">`             |                                       |
| `required`    | Makes field mandatory                 | `<input required>`                 |                                       |
| `disabled`    | Disables input                        | `<input disabled>`                 |                                       |
| `readonly`    | Read-only input                       | `<input readonly>`                 |                                       |
| `checked`     | Pre-check radio/checkbox              | `<input type="checkbox" checked>`  |                                       |

##### 📝 Type (From Input Attributes) values
In HTML, the `type` attribute of an `<input>` element specifies the kind of data that is expected or how the input should behave. Here are the most commonly used `type` attribute values for `<input>` elements:

| Type             | Description                                       | Facts               |
| ---------------- | ------------------------------------------------- | ------------------- |
| `text`           | Single-line text input                            |                     |
| `password`       | Obscured input for passwords                      |                     |
| `email`          | Input for email addresses (with validation)       |                     |
| `number`         | Numeric input (with optional min/max)             |                     |
| `tel`            | Telephone number input                            |                     |
| `url`            | Input for URLs (with validation)                  |                     |
| `search`         | Search field input                                | Use search element. |
| `date`           | Date picker                                       |                     |
| `time`           | Time picker                                       |                     |
| `datetime-local` | Date and time input (local)                       |                     |
| `month`          | Month and year picker                             |                     |
| `week`           | Week picker                                       |                     |
| `file`           | File upload input                                 |                     |
| `checkbox`       | Checkbox input                                    |                     |
| `radio`          | Radio button input                                |                     |
| `range`          | Slider input for selecting from a range of values |                     |
| `submit`         | Submit button                                     | Use button element. |
| `reset`          | Reset button                                      | Use button element. |
| `button`         | Generic button                                    | Use button element. |
| `hidden`         | Hidden input (not visible to users)               |                     |
| `color`          | Color picker input                                |                     |
| `image`          | Submit button using an image as input             |                     |

#### ⚙️ Other Useful Attributes

|Attribute|Description|Example|
|---|---|---|
|`src` (scripts)|Source for JS/CSS/media|`<script src="script.js">`|
|`defer`|Delays script execution|`<script defer>`|
|`async`|Runs script asynchronously|`<script async>`|
|`autoplay`|Auto-plays video/audio|`<video autoplay>`|
|`controls`|Adds play/pause/etc.|`<audio controls>`|

#### 🧠 Notes

- Attribute **values** must be in **quotes**.

- Some attributes (like `disabled`, `checked`) are **Boolean**, meaning just writing the attribute name enables it.

---

## HTML Boilerplate Code
This is the **standard format or skeleton** of writing HTML code.

```
<!DOCTYPE html>

<html lang="en">

	<head>
		
		<meta charset="UTF-8">
		
		<meta name="viewport" content="width=device-width, initial-scale=1.0">
		
		<title>Document</title>
		
	</head>
	
	<body>
		
		<!-- Actual code -->
		
	</body>
	
</html>
```

---

## HTML Entities
**HTML entities** are special codes used in HTML to represent characters that have reserved meanings or that are not easily typed from a keyboard. They begin with an ampersand (`&`) and end with a semicolon (`;`).

#### Common HTML Entities

| Character | Entity Code | Description               |
| --------- | ----------- | ------------------------- |
| `&`       | `&amp;`     | Ampersand                 |
| `<`       | `&lt;`      | Less-than                 |
| `>`       | `&gt;`      | Greater-than              |
| `"`       | `&quot;`    | Double quote              |
| `'`       | `&apos;`    | Apostrophe (single quote) |
| `©`       | `&copy;`    | Copyright                 |
| `®`       | `&reg;`     | Registered trademark      |
| `€`       | `&euro;`    | Euro sign                 |
| `£`       | `&pound;`   | Pound sign                |
| `¢`       | `&cent;`    | Cent sign                 |
| `¥`       | `&yen;`     | Yen sign                  |
| `→`       | `&rarr;`    | Right arrow               |
| `←`       | `&larr;`    | Left arrow                |
| ` `       | `&nbsp;`    | Non-breaking space        |

##### 🔢 Numeric Entities
You can also use numeric codes:

- Decimal: `&#169;` (for ©)

- Hexadecimal: `&#x00A9;` (for ©)

### When to Use

- To **display special characters** in HTML.

- To **avoid breaking HTML syntax** when using symbols like `<`, `>`, and `&`.

- To ensure **browser compatibility** for less common characters.

---

## Semantic Markup
**Semantic markup in HTML** refers to the use of HTML tags that convey the **meaning** or **structure** of the content they contain, rather than just how the content looks. These tags help browsers, search engines, and assistive technologies understand the content better.

### 🔍 **Examples of Semantic HTML Tags**

| Tag                         | Purpose                                                             |
| --------------------------- | ------------------------------------------------------------------- |
| `<header>`                  | Defines introductory content, often contains navigation or headings |
| `<nav>`                     | Represents a section of navigation links                            |
| `<main>`                    | Represents the dominant content of the `<body>`                     |
| `<section>`                 | Defines a section of related content                                |
| `<article>`                 | Represents self-contained content (e.g., blog post, news article)   |
| `<aside>`                   | Content tangentially related to the main content (e.g., sidebar)    |
| `<footer>`                  | Defines footer content (e.g., contact info, copyright)              |
| `<figure>` / `<figcaption>` | Used for images or diagrams with captions                           |
| `<mark>`                    | Highlights text for reference                                       |
| `<time>`                    | Represents a specific time or date                                  |

### ✅ **Benefits of Semantic HTML**

1. **Improved accessibility** for screen readers and assistive technologies.

2. **Better [[SEO]]**, as search engines can better understand the content hierarchy.

3. **Cleaner, more maintainable code**.

4. **Enhanced collaboration**, since other developers can more easily read and understand the structure.

---
## Nesting in HTML
**Nesting** in HTML means placing one element inside another, forming a **parent-child relationship**. This structure helps define the **document hierarchy** and how content is grouped and displayed.

### 🔁 **Basic Example of Nesting**

```
<div>
	<p>
		This is a paragraph <strong>with bold text</strong>.
	</p>
</div>

```

- `<div>` is the **parent**.

- `<p>` is the **child** of `<div>`.

- `<strong>` is a **child** of `<p>`.

### ✅ **Correct Nesting Rules**

1. **Elements must be fully closed** inside their parent:

```
<!-- ✅ Correct --> 
<p>This is <strong>bold</strong> text.</p>  

<!-- ❌ Incorrect --> 
<p>This is <strong>bold</p></strong>
```

2. **Block-level elements should not go inside inline elements**:

```
<!-- ❌ Incorrect --> 
<strong><div>Text</div></strong>  

<!-- ✅ Correct --> 
<div><strong>Text</strong></div>
```

3. **Follow semantic structure**:  
	Use nesting to show structure and meaning (e.g., sections, navigation, headers).

---

## [HTML Emmets](https://docs.emmet.io/cheat-sheet/)
**HTML Emmet** is a shorthand syntax used primarily in code editors like VS Code, Sublime Text, and Atom to write HTML (and CSS) faster. It's like writing a compressed version of HTML that expands into full code when you hit `Tab`.

### ✨ **Basic Emmet Syntax for HTML**

| Emmet Abbreviation | Expands To                             | Explanation                                   |
| ------------------ | -------------------------------------- | --------------------------------------------- |
| `!`                | `Boilerplate code`                     | Creates boilerplate code                      |
| `div`              | `<div></div>`                          | Creates opening & closing tags                |
| `ul>li`            | `<ul><li></li></ul>`                   | Creates parent-child hierarchy                |
| `p>b+i`            | `<p><b></b><i></i></p>`                | Creates elements in same hierarchy (siblings) |
| `p>b>u^i`          | `<p><b><u></u></b><i></i></p>`         | Creates element one step up in hierarchy      |
| `ul>li*3`          | `<ul><li></li><li></li><li></li></ul>` | Duplicates same elements                      |
| `div#header`       | `<div id="header"></div>`              | Creates id attribute                          |
| `div.container`    | `<div class="container"></div>`        | Creates class attribute                       |
| `input:text`       | `<input type="text">`                  | Creates most important attribute              |
| `a:link`           | `<a href="link"></a>`                  |                                               |

---
