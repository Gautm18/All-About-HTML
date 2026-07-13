# Chapter 4 – Evolution of HTML (HTML 1.0 → HTML5 → Living Standard)

> To understand modern HTML, we first need to understand the problems each version tried to solve.

---

# Timeline

```text
1989  → World Wide Web proposed
1991  → HTML 1.0
1995  → HTML 2.0
1997  → HTML 3.2
1999  → HTML 4.01
2008+ → HTML5
Today → HTML Living Standard
```

---

# HTML 1.0

Purpose:
- Share scientific documents.
- Link documents using hyperlinks.

Features:
- Headings
- Paragraphs
- Lists
- Links

No CSS, JavaScript, forms, audio, or video.

---

# HTML 2.0

Problem:
Websites needed user interaction.

Solution:
Introduced Forms.

Example:

```html
<form>
  <input>
  <button>Submit</button>
</form>
```

---

# HTML 3.2

Developers wanted visually rich pages.

Introduced presentational elements like:

```html
<font>
<center>
<b>
<i>
```

Problem:
HTML started mixing structure with presentation.

---

# HTML 4.01

Major goal:
Separate structure from presentation.

Instead of:

```html
<font color="red">Warning</font>
```

Use:

```html
<p class="warning">Warning</p>
```

```css
.warning {
  color: red;
}
```

CSS became responsible for appearance.

---

# Problems Before HTML5

Common layouts looked like:

```html
<div id="header"></div>
<div id="menu"></div>
<div id="content"></div>
<div id="footer"></div>
```

Issues:
- Poor accessibility
- Poor SEO
- No semantic meaning
- Heavy use of plugins for video/audio

---

# HTML5

Goals:

- Better semantics
- Better accessibility
- Native multimedia
- Better forms
- Browser APIs
- Consistent parsing

Major additions:

- header
- nav
- main
- section
- article
- footer
- video
- audio
- canvas
- localStorage
- New form input types

---

# Living Standard

HTML no longer evolves through large version releases.

Instead, it is continuously maintained as a Living Standard.

This allows browsers and specifications to improve incrementally.

---

# React Connection

React renders HTML elements regardless of the framework.

Using semantic HTML in React improves:

- Accessibility
- SEO
- Maintainability

Example:

```jsx
<main>
  <article>
    <h1>React Basics</h1>
  </article>
</main>
```

---

# Interview Questions

### Why was HTML5 introduced?

To modernize the web with semantics, multimedia support, improved forms, accessibility, and browser APIs.

### Why are <font> and <center> deprecated?

Because presentation belongs to CSS.

### Why don't we have HTML6?

Because HTML follows the Living Standard model.

---

# Common Mistakes

❌ HTML5 only introduced new tags.

❌ HTML5 is only about video and audio.

❌ Semantic HTML directly improves rankings.

---

# Summary

- HTML evolved to solve real-world problems.
- HTML5 focused on semantics, accessibility, and modern web applications.
- HTML is now maintained as a Living Standard instead of versioned releases.
