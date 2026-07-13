# Chapter 5 – Semantic HTML

> Semantic HTML means using elements that describe the purpose and meaning of content instead of generic containers.

---

# What is Semantic HTML?

Semantic HTML uses meaningful elements.

Example:

Instead of:

```html
<div id="header"></div>
<div id="navigation"></div>
<div id="footer"></div>
```

Use:

```html
<header></header>
<nav></nav>
<footer></footer>
```

---

# Why Semantic HTML?

## 1. Accessibility

Screen readers understand landmarks such as:

- header
- nav
- main
- footer

making navigation easier.

---

## 2. SEO

Semantic elements help search engines better understand the structure of a page.

> Semantic HTML improves understanding, but it does not guarantee higher rankings.

---

## 3. Maintainability

This:

```html
<header>
    <nav></nav>
</header>
```

is easier to understand than:

```html
<div class="header">
    <div class="nav"></div>
</div>
```

---

## 4. Team Communication

Developers can quickly identify page sections without relying on class names.

---

# Semantic vs Non-Semantic

| Non-Semantic | Semantic |
|--------------|----------|
| div | header |
| div | nav |
| div | main |
| div | section |
| div | article |
| div | aside |
| div | footer |

---

# Important Semantic Elements

## header

Represents introductory content.

A page may contain multiple `header` elements.

---

## nav

Represents a major navigation section.

Multiple `nav` elements are allowed if each represents a meaningful navigation region.

---

## main

Represents the primary content of the document.

A document should contain only **one** `main` element.

---

## section

Groups related content under a common theme.

Ideally, a section should contain a heading.

---

## article

Represents self-contained content.

Examples:

- Blog post
- News article
- Product review
- Forum post

An article should make sense on its own.

---

## aside

Represents content related to, but separate from, the main content.

Examples:

- Sidebar
- Related articles
- Advertisements

---

## footer

Represents footer information for a page, article, or section.

Multiple footers are valid.

---

## figure & figcaption

```html
<figure>
    <img src="cat.jpg" alt="Sleeping cat">
    <figcaption>Sleeping Cat</figcaption>
</figure>
```

---

## time

Represents machine-readable dates or times.

```html
<time datetime="2026-07-13">
July 13, 2026
</time>
```

---

# Section vs Article

| Section | Article |
|----------|----------|
| Groups related content | Self-contained content |
| Similar to a chapter | Similar to a newspaper story |

Example:

```html
<section>
    <h2>Latest News</h2>

    <article>News 1</article>
    <article>News 2</article>
</section>
```

---

# Should You Stop Using div?

No.

Use `div` whenever no semantic element accurately represents the content.

Example:

```html
<header>
    <div class="logo">Logo</div>
    <nav>...</nav>
</header>
```

---

# React Connection

Semantic HTML is equally important in React.

Example:

```jsx
<main>
    <section>
        <article>
            <h2>React Basics</h2>
        </article>
    </section>
</main>
```

React renders HTML elements; accessibility and semantics still matter.

---

# Interview Questions

### Why was Semantic HTML introduced?

To improve accessibility, maintainability, and document structure.

### Is `div` deprecated?

No.

### Can a page have multiple `header` elements?

Yes.

### Can a page have multiple `main` elements?

No.

### Difference between `section` and `article`?

- `section` groups related content.
- `article` is self-contained.

---

# Common Mistakes

❌ Replacing every `div` with `section`

❌ Multiple `main` elements

❌ Using `section` only for styling

❌ Thinking semantic HTML changes appearance

---

# Summary

- Semantic HTML describes meaning.
- It improves accessibility and document structure.
- Use semantic elements when appropriate.
- Use `div` when no semantic element fits.
