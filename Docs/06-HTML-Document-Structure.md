# Chapter 6 – HTML Document Structure

> Every HTML document follows a standard structure. Understanding why each line exists is more important than memorizing the template.

---

# Basic HTML Document

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Frontend Masterclass</title>
</head>

<body>
    <h1>Hello World</h1>
</body>
</html>
```

---

# Overall Structure

```text
Document
│
├── head
│
└── body
```

- `head` → Information about the document (metadata)
- `body` → Visible content

---

# <!DOCTYPE html>

Purpose:

- Enables **Standards Mode**
- Prevents browsers from entering **Quirks Mode**

Important:

- It is **not an HTML element**.
- It is **not part of the DOM**.

---

# <html>

The root element of every HTML document.

Example:

```html
<html lang="en">
```

Everything else is a child of this element.

## lang Attribute

Helps:

- Screen readers
- Search engines
- Translation tools
- Browser language detection

---

# <head>

Contains metadata.

Examples:

- Character encoding
- Title
- CSS links
- JavaScript files
- Meta tags
- Favicon

Visible content should **not** be placed inside `<head>`.

---

# <meta charset="UTF-8">

Specifies the character encoding.

Without UTF-8, special characters and emoji may not render correctly.

Examples:

- ₹
- 😀
- 你好
- नमस्ते

---

# <meta name="viewport">

```html
<meta
  name="viewport"
  content="width=device-width, initial-scale=1.0">
```

Purpose:

- Enables responsive layouts.
- Matches the viewport width to the device width.
- Sets the initial zoom level.

---

# <title>

Defines the document title.

Displayed in:

- Browser tab
- Bookmarks
- Browser history
- Often search results

Difference:

| title | h1 |
|-------|----|
| Metadata | Visible heading |
| Appears in tab | Appears on page |

---

# <body>

Contains everything normally visible to the user.

Examples:

- Headings
- Paragraphs
- Images
- Forms
- Navigation
- Sections
- Buttons

---

# Browser Flow

```text
DOCTYPE
    ↓
Standards Mode
    ↓
<html>
    ↓
<head>
    ↓
Metadata
    ↓
<body>
    ↓
DOM
    ↓
CSSOM
    ↓
Render Tree
    ↓
Layout
    ↓
Paint
```

---

# React Connection

React components ultimately render elements inside the document body.

Example:

```jsx
function App() {
    return <main>Hello</main>;
}
```

React does not replace the document structure—it renders into a DOM container inside the body.

---

# Interview Questions

### Why do we use `<!DOCTYPE html>`?

To render the page in Standards Mode.

### Is DOCTYPE part of the DOM?

No.

### Why use the `lang` attribute?

Accessibility, SEO, and language detection.

### Difference between `title` and `h1`?

`title` describes the document.
`h1` is the main visible heading.

### Can visible elements be placed inside `<head>`?

No.

---

# Common Mistakes

❌ Forgetting the viewport meta tag.

❌ Confusing `title` with `h1`.

❌ Thinking DOCTYPE is an HTML tag.

❌ Omitting the `lang` attribute.

---

# Summary

- Every HTML document has one root element.
- `head` stores metadata.
- `body` stores visible content.
- DOCTYPE enables Standards Mode.
- UTF-8 ensures correct character decoding.
- The viewport tag is essential for responsive design.
