# Welcome 🌍 to HTML 📄

### [🔙 Back To Main Readme](../../../README.md) 👈

## Table of Contents

- [Welcome 🌍 to HTML 📄](#welcome--to-html-)
    - [🔙 Back To Main Readme 👈](#-back-to-main-readme-)
  - [Table of Contents](#table-of-contents)
  - [1️⃣ HTML Basics](#1️⃣-html-basics)
  - [2️⃣ HTML Document Structure](#2️⃣-html-document-structure)
  - [3️⃣ HTML Elements \& Tags](#3️⃣-html-elements--tags)
    - [🛎️ **Common HTML Elements:**](#️-common-html-elements)
    - [⚠️ **Nesting Rules**](#️-nesting-rules)
  - [4️⃣ HTML Attributes](#4️⃣-html-attributes)
  - [5️⃣ Semantic HTML](#5️⃣-semantic-html)
  - [6️⃣ HTML Forms](#6️⃣-html-forms)
  - [7️⃣ HTML Tables](#7️⃣-html-tables)
  - [8️⃣ HTML Media](#8️⃣-html-media)
  - [9️⃣ HTML Meta Tags](#9️⃣-html-meta-tags)
  - [1️⃣0️⃣ HTML Comments](#1️⃣0️⃣-html-comments)
  - [1️⃣1️⃣ HTML Accessibility](#1️⃣1️⃣-html-accessibility)
  - [1️⃣2️⃣ HTML Validation](#1️⃣2️⃣-html-validation)
  - [1️⃣3️⃣ HTML Best Practices](#1️⃣3️⃣-html-best-practices)
  - [1️⃣4️⃣ HTML5 Features](#1️⃣4️⃣-html5-features)
    - [🔙 Back To Main Readme 👈](#-back-to-main-readme--1)

---

## 1️⃣ HTML Basics

**HTML (HyperText Markup Language)** is the standard markup language for creating web pages `it is not a programming language`:
- Uses **tags** to structure content (e.g., `<h1>`, `<p>`)
- Files use `.html` extension
- Basic template:
  ```html
  <!DOCTYPE html>
  <html lang="en">
  <head>
      <meta charset="UTF-8">
      <title>Page Title</title>
  </head>
  <body>
      <!-- Content goes here -->
  </body>
  </html>
  ```

---

## 2️⃣ HTML Document Structure

| Part               | Description                                                                 |
|--------------------|-----------------------------------------------------------------------------|
| `<!DOCTYPE html>`  | Declares HTML5 document type                                                |
| `<html>`           | Root element wrapping all content                                           |
| `<head>`           | Contains meta-information (title, stylesheets, scripts)                    |
| `<body>`           | Contains visible content (headings, paragraphs, images, links)             |
| `<title>`          | Sets the browser tab title (placed in `<head>`)                            |

---

## 3️⃣ HTML Elements & Tags

### 🛎️ **Common HTML Elements:**

| Element         | Description                          | Example                     |
|-----------------|--------------------------------------|-----------------------------|
| `<h1> to <h6>`  | Headings (h1 = largest)              | `<h1>Main Title</h1>`       |
| `<p>`           | Paragraph                            | `<p>This is a paragraph</p>`|
| `<a>`           | Hyperlink                            | `<a href="https://example.com">Link</a>` |
| `<img>`         | Image (self-closing)                 | `<img src="image.jpg" alt="Description">` |
| `<ul>/<ol>`     | Unordered/Ordered list               | `<ul><li>Item</li></ul>`    |
| `<div>`         | Block container                      | `<div class="container"></div>` |
| `<span>`        | Inline container                     | `<span class="highlight"></span>` |

### ⚠️ **Nesting Rules**
- Always close tags properly: `<tag>content</tag>`
- Self-closing tags: `<img>`, `<br>`, `<input>`
- Avoid overlapping: `<p><strong>Text</p></strong>` ❌  
  Correct: `<p><strong>Text</strong></p>` ✅

---

## 4️⃣ HTML Attributes

Provide additional information about elements:
- Syntax: `<tag attribute="value">`
- Common attributes:
  - `id`: Unique identifier (`#id` in CSS)
  - `class`: Groups elements (`.class` in CSS)
  - `href`: Link destination (`<a href="url">`)
  - `src`: Source URL for media (`<img src="image.jpg">`)
  - `alt`: Alternative text for images (accessibility)
  - `style`: Inline CSS (avoid for maintainability)
  - `data-*`: Custom data attributes (`data-user="john"`)

---

## 5️⃣ Semantic HTML

- Use meaningful tags for better accessibility & SEO
- Mostly all the below tags is same as `<div>` tag but it has a semantic meaning


| Tag             | Purpose                                      |
|-----------------|----------------------------------------------|
| `<header>`      | Introductory content (logo, navigation)     |
| `<nav>`         | Navigation links                            |
| `<main>`        | Primary content of the page                 |
| `<article>`     | Self-contained content (blog post, news)    |
| `<section>`     | Thematic grouping of content                |
| `<aside>`       | Sidebar or complementary content            |
| `<footer>`      | Footer (contact info, copyright)            |
| `<figure>`      | Wraps images/diagrams with `<figcaption>`   |

---

## 6️⃣ HTML Forms

Collect user input:
```html
<form action="/submit" method="POST">
  <label for="name">Name:</label>
  <input type="text" id="name" name="name" required>
  
  <label for="email">Email:</label>
  <input type="email" id="email" name="email">
  
  <label for="message">Message:</label>
  <textarea id="message" name="message"></textarea>
  
  <button type="submit">Send</button>
</form>
```

**Output:**

<form action="/submit" method="POST">
  <label for="name">Name:</label>
  <input type="text" id="name" name="name" required>
  
  <label for="email">Email:</label>
  <input type="email" id="email" name="email">
  
  <label for="message">Message:</label>
  <textarea id="message" name="message"></textarea>
  
  <button type="submit">Send</button>
</form>

**Make Sure to**

- Use proper methods: `GET` (for fetching data), `POST` (for submitting data), `PUT`, `DELETE`
- Use proper action URL (server endpoint)
- Use `<label>` for form element descriptions
- Use `required` attribute for mandatory fields
- Use type submit for submit button to submit the form

**Common Input Types:**
- `text`, `email`, `password`, `number`, `date`, `checkbox`, `radio`, `file`
- Check Types [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input)

---

## 7️⃣ HTML Tables

Display tabular data:
```html
<table>
  <thead>
    <tr>
      <th>Name</th>
      <th>Age</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>John</td>
      <td>25</td>
    </tr>
  </tbody>
</table>
```
**Output:**

<table>
  <thead>
    <tr>
      <th>Name</th>
      <th>Age</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>John</td>
      <td>25</td>
    </tr>
  </tbody>
</table>

**Table Structure:**
- `<table>`: Container for the table
- `<thead>`: Table header row
- `<tbody>`: Table body content
- `<tr>`: Table row
- `<th>`: Table header cell
- `<td>`: Table data cell

---

## 8️⃣ HTML Media

Embed multimedia content:
- **Images:** `<img src="cat.jpg" alt="A cute cat" width="300">`
  - `src`: Image URL
  - `alt`: Description for screen readers, this is important for accessibility
  - `width`, `height`: Dimensions in pixels
- **Video:** 
  ```html
  <video controls>
    <source src="video.mp4" type="video/mp4">
    Your browser doesn't support videos.
  </video>
  ```
    - `controls`: Show video controls (play, pause)
    - `autoplay`, `loop`: Additional attributes
- **Audio:** 
  ```html
  <audio controls>
    <source src="audio.mp3" type="audio/mpeg">
  </audio>
  ```
    - `controls`: Show audio controls
    - `autoplay`, `loop`: Additional attributes

---

## 9️⃣ HTML Meta Tags

- Provide metadata about the page (placed in `<head>`)
- Common meta tags:
  - `charset`: Character encoding (`UTF-8`)
  - `viewport`: Responsive design settings (`width=device-width`)
  - `description`: Page description (for SEO)
  - `keywords`: Page keywords (for SEO)
  - `author`: Page author
  - `robots`: Search engine instructions (`noindex`, `nofollow`)
- This is important for SEO and accessibility

```html
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="description" content="Free web tutorials">
<meta name="keywords" content="HTML, CSS, JavaScript">
<meta name="author" content="John Doe">
```

---

## 1️⃣0️⃣ HTML Comments

Add notes invisible to users:
```html
<!-- This is a comment -->
<p>Visible content</p>
```

---

## 1️⃣1️⃣ HTML Accessibility

Make content usable for everyone:
- Use semantic tags (`<nav>`, `<button>` instead of `<div>`)
- Add `alt` text to images
- Use ARIA roles when needed (`role="navigation"`)
- Ensure proper contrast ratios
- Label form elements with `<label>`

---

## 1️⃣2️⃣ HTML Validation

Check markup for errors:
- [W3C Validator](https://validator.w3.org/)
- VS Code extensions (e.g., HTMLHint)
- Always validate before deployment!

---

## 1️⃣3️⃣ HTML Best Practices

- Use lowercase for tags/attributes: `<div class="box">` ✅
- Quote attribute values: `<input type="text">` ✅
- Indent nested elements (2 or 4 spaces)
- Avoid deprecated tags: `<center>`, `<font>` ❌
- Separate content (HTML), presentation (CSS), and behavior (JavaScript)
- Use external CSS/JS files for styling and scripts
- Use comments to explain complex code
- Use semantic tags for better accessibility and SEO
- Validate your HTML code
- Use accessibility features (alt text, ARIA roles)
- Use responsive design (viewport meta tag)

---

## 1️⃣4️⃣ HTML5 Features

| Feature          | Description                          |
|------------------|--------------------------------------|
| `<canvas>`       | Draw graphics via JavaScript         |
| `<svg>`          | Vector graphics                      |
| Geolocation API  | Access user's location               |
| Local Storage    | Store data locally                   |
| Web Components   | Create reusable custom elements      |

---

### [🔙 Back To Main Readme](../../../README.md) 👈