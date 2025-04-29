## Q: What is the role of DOCTYPE in HTML?
Ans: DOCTYPE(Document Type) declaration specifies the "**version**" of HTML.
### Example:
```html
<DOCTYPE html>
```
"**Version no:5**"
- DOCTYPE tells the browser which version of HTML it is and how to interpret the code.
****************************
## Q: What are the Meta Tags? What are the 5 types of meta tags?
Ans: Meta tags in HTML are elements used to provide "**metadata or additional information**" about a web page.
### There are 5 types of meta tags:
1. charset: ("**Character Encoding**") helps browsers to interpret the different characters in the document. The **charset="UTF-8"** attribute ensures the characters from **different languages** will be displayed correctly in the browser.
2. viewport: ("**Responsive Design**") is crucial for creating mobile-friendly, **responsive web designs** for various screen size.
3. description: ("**Description for SEO**") provides decription of the content of this page. Search engines may use this for search results.
4. keywords: ("**keywords for SEO**") used to be important for search engines, but it's now of less important.
5. author: ("**Author info**") can be used to specify the author of the document.
```html
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
  <meta name="description" content="Technical interview preparation">
  <meta name="keywords" content="React, JS, HTML">
  <meta name="author" content="Joydeb Biswas">
</head>
```
**********************************************
## Q: What is the difference between <div> and <span> element?
Ans: 
- The "**div**" (division) element in HTML is a **container** that is used to **group and structure* the content on a webpage.
- The "**span**" element in HTML is an **inline container** used to apply **styles or scripting* to specific of text or content.
- "**div**" is **block-level** element and "**span**" is an **inline element**.
```html
  <div>
    <h1>Main Heading</h1>
    <p>Interview <span style="color: blue;">Happy</span></p>
  </div>
```
**************************************************
## Q: What are Semantic Elements in HTML? Is div a semantic element?
Ans: Semantic elements in HTML are elements that provide **meaning to the content** they contain. Meaning you can tell what is present inside the element by see the element name.
### Top 5 Sementic elements:
1. header
2. main
3. section
4. footer
5. address
```html
<body>
  <header>
    <h1>Webside Header</h1>
  </header>
  <main>
    <section id="section1">
      <h2>Section 1</h2>
    </section>
  </main>
  <aside>
    <h2>Aside Content</h2>
  </aside>
  <footer>
    <address>India</address>
  </footer>
</body>
```
- "**div**" is not a semantic element, because div is a general-purpose structural element. It doesn't give any meaning to the content.
******************************************************************
### 10 semantic elements:
1. **progress**: Displays the progress of a task.
2. **nav**: Contains navigation links for a webpage.
3. **time**: Represents a specific period in time or a date.
4. **mark**: Highlights parts of the text for reference or emphasis.
5. **summary**: Provides a summary, caption, or legend for a **details** element.
6. **meter**: Represents a scalar measurement within a known range (like a gauge).
7. **figure**: Contains content like images, illustrations, diagrams etc. along with a caption.
8. **details**: Represents additional information or controls that can be toggled open or closed.
9. **aside**: Contains content that is related to the main content but can be considered separate.
10. **article**: Represents a self-contained composition in a document, such as a blog post or a news article
*********************************************************************
1. header -> Used for introductory content like logo, title, nav, etc.
```html
<header>
  <h1>My Website</h1>
  <nav>
    <a href="/">Home</a>
    <a href="/about">About</a>
  </nav>
</header>

```
2. main -> Represents the main content of the webpage.
```html
<main>
  <h2>Welcome to My Website</h2>
  <p>This is the primary content of the page.</p>
</main>

```
3. section -> A thematic grouping of content, often with a heading.
```html
<section>
  <h2>Our Services</h2>
  <p>We offer web development and design services.</p>
</section>

```
4. footer -> Defines footer for a section or page. Can include contact info, links, etc.
```html
<footer>
  <p>&copy; 2025 My Website</p>
</footer>

```
5. address -> Provides contact info for the author/owner.
```html
<address>
  Contact us at: <a href="mailto:info@example.com">info@example.com</a>
</address>

```
6. progress -> Shows task completion progress.
```html
<label for="upload">Uploading file:</label>
<progress id="upload" value="70" max="100">70%</progress>
```
7. nav -> Defines navigation links.
```html
<nav>
  <ul>
    <li><a href="/">Home</a></li>
    <li><a href="/blog">Blog</a></li>
  </ul>
</nav>
```
8. time -> Represents date or time.
```html
<time datetime="2025-04-29">April 29, 2025</time>
```
9. mark -> Highlights text.
```html
<p>Don't forget to <mark>submit your form</mark> before Friday.</p>
```
10. summary + details -> summary is the visible part, and details toggles extra info.
```html
<details>
  <summary>More info</summary>
  <p>This section contains extra details you can show or hide.</p>
</details>
```
11. meter -> Represents a measurement in a known range.
```html
<label for="disk">Disk usage:</label>
<meter id="disk" value="0.6">60%</meter>

```
12. figure + figcaption ->Used for self-contained media like images, diagrams, charts.
```html
<figure>
  <img src="image.jpg" alt="Nature">
  <figcaption>A beautiful nature photo</figcaption>
</figure>

```
13. aside -> Contains related content (like ads, links, tips).
```html
<aside>
  <h3>Related Posts</h3>
  <ul>
    <li><a href="/post1">How to learn HTML</a></li>
  </ul>
</aside>

```
14. articale -> For independent content like blog posts or news.
```html
<article>
  <h2>Top 5 HTML5 Tips</h2>
  <p>Learn how to write semantic HTML easily.</p>
</article>

```
**************************************************************
## Q: What are 3 differences between Block-level and Inline Elements?
1. Block-level elements create "**blocks**" of content.
#### Example: 
```html
<div>, <p>, <h1>, <ul>, <li>, <form> 
```
2. By default block-level elements start on a new line.
3. You can set both "**width**" and "**height**" for a block-level elements.
----------------------------------------------------------------------
1. inline elements length depends on their "**content length**"
#### Example:
```html
<span>, <a>, <strong>, <em>, <img>, <input>, <br>
```
2. Inline elements do not start on a new line.
3. You can't set width and height for inline element.
*******************************************************************

