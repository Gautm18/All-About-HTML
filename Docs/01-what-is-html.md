# Chapter 1 – What is HTML?

## Definition
HTML (HyperText Markup Language) is a **markup language** used to describe the structure and meaning (semantics) of web content.

> HTML describes **what** content is, not **how** it looks.

---

## Why HTML Exists

Computers understand bytes, not the meaning of content. HTML adds semantic information using tags so browsers can understand the role of each piece of content.

Example:

```html
<h1>Frontend Masterclass</h1>
<p>Hello World</p>
```

---

## HTML Breakdown

- **Hyper** → Hyperlinks connect one document to another.
- **Text** → Originally designed for structured documents.
- **Markup** → Uses tags to describe the meaning of content.
- **Language** → Has a defined syntax and grammar.

---

## HTML is NOT a Programming Language

Programming languages provide:
- Variables
- Loops
- Conditions
- Functions
- Algorithms

HTML does none of these.

Example:

```html
<p>Hello World</p>
```

This describes a paragraph; it does not execute logic.

---

## HTML vs CSS vs JavaScript

| HTML | CSS | JavaScript |
|------|-----|------------|
| Structure | Presentation | Behavior |

Think of a human:

- HTML → Skeleton
- CSS → Appearance
- JavaScript → Behavior

---

## Why Semantic HTML Matters

Instead of:

```html
<div id="header"></div>
```

Use:

```html
<header></header>
```

Semantic elements improve:
- Accessibility
- SEO
- Maintainability
- Readability

---

## Browser Perspective

```text
HTML
↓
Parser
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

## Interview Questions

### Why is HTML called a Markup Language?
Because it uses tags to describe the meaning and structure of content rather than executing logic.

### Is HTML a programming language?
No.

### Why was HTML invented?
To allow linked documents to be shared over the web.

### Can HTML work without CSS?
Yes. Browsers apply default styles.

### Can HTML work without JavaScript?
Yes. HTML pages, links, and forms still function.

---

## Summary

- HTML defines structure.
- CSS defines appearance.
- JavaScript defines behavior.
- HTML is semantic, not procedural.
- Browsers convert HTML into the DOM before rendering.
