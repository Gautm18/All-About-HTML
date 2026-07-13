# Chapter 3 – Browser Rendering Pipeline (DOM → Pixels)

## Rendering Pipeline

```text
HTML
↓
DOM
+
CSS
↓
CSSOM
↓
Render Tree
↓
Layout
↓
Paint
↓
Composite
↓
Pixels on Screen
```

## CSSOM
The CSS Object Model is the browser's parsed, in-memory representation of CSS rules.

## DOM vs CSSOM

| DOM | CSSOM |
|------|--------|
| Structure | Styles |
| HTML | CSS |

## Render Tree

The Render Tree combines the DOM and CSSOM.

Elements with `display:none` are excluded.

Elements with `visibility:hidden` are included because they still occupy layout space.

## Layout

Calculates:

- Width
- Height
- Position
- Margin
- Padding

## Paint

Draws:

- Text
- Borders
- Backgrounds
- Images

## Composite

Combines layers into the final frame, often using GPU acceleration.

## React Connection

```text
State Update
↓
Reconciliation
↓
Real DOM Update
↓
Layout
↓
useLayoutEffect
↓
Paint
↓
Composite
↓
useEffect
```

`useLayoutEffect` runs after Layout but before Paint, allowing DOM measurements such as:

```javascript
element.offsetWidth
element.offsetHeight
element.getBoundingClientRect()
```

## Performance

Prefer animating:

- transform
- opacity

Avoid frequent animation of:

- width
- height
- top
- left

## Interview Questions

- What is CSSOM?
- What is the Render Tree?
- Difference between Layout and Paint?
- Why is `display:none` excluded from the Render Tree?
- Why does `useLayoutEffect` exist?

## Summary

- DOM = Structure
- CSSOM = Styles
- Render Tree = DOM + CSSOM
- Layout = Geometry
- Paint = Pixels
- Composite = Final frame
