# Chapter 7 – The `<head>` Element Deep Dive

> The `<head>` contains metadata and resource references that help the browser understand the document before rendering the visible page.

---

## What is the `<head>`?

The `<head>` stores **metadata** (data about the document), not visible UI.

Common contents:

- Meta tags
- Page title
- CSS files
- JavaScript files
- Favicon
- SEO information
- Resource hints

---

## Browser Parsing Order

```text
DOCTYPE
   ↓
<html>
   ↓
<head>
   ↓
Read Metadata
   ↓
Discover Resources
   ↓
<body>
   ↓
DOM Construction
```

The browser parses the `<head>` first because it contains information required to correctly process and render the page.

---

## Why Parse `<head>` First?

The browser needs to know:

- Character encoding
- Viewport settings
- Document title
- CSS files
- JavaScript files
- Icons

As soon as it discovers external resources, it can begin downloading them.

---

## What Belongs Inside `<head>`?

```html
<head>
  <meta charset="UTF-8">
  <meta name="viewport"
        content="width=device-width, initial-scale=1.0">

  <title>Frontend Masterclass</title>

  <link rel="stylesheet" href="style.css">

  <script defer src="app.js"></script>
</head>
```

---

## What Should NOT Be Inside `<head>`?

```html
<head>
  <h1>Hello</h1>
  <button>Click</button>
</head>
```

Visible content belongs inside `<body>`.

---

## Browser Internals

```text
<head>
   │
   ├── Read charset
   ├── Read viewport
   ├── Read title
   ├── Discover CSS
   ├── Discover JavaScript
   └── Discover icons
```

The browser can begin fetching resources while it continues parsing.

---

## React Connection

A React application's `index.html` still contains a normal `<head>`.

React mounts inside a container in the `<body>` and does not replace the purpose of the `<head>`.

---

## Interview Questions

### Why is `<head>` parsed before `<body>`?

Because it contains metadata and resource references needed before rendering.

### Can visible elements be placed inside `<head>`?

No.

### Does `<head>` become part of the DOM?

Yes.

### What is metadata?

Information about the document rather than visible page content.

---

## Common Mistakes

- Putting UI elements inside `<head>`
- Thinking `<head>` is only for `<title>`
- Forgetting `charset` or `viewport`

---

## Summary

- `<head>` contains metadata.
- Browsers parse it before the body.
- Resource discovery starts here.
- Visible content belongs inside `<body>`.
