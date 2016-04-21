## Agenda

# Concepts
# Technology and Tools

---

# Concepts

---

## Concepts

# One Web
# Responsive Web Design
# Performance

---

# **One Web**

^ device, connection, disabilities

---

## One Web
# Device

^ different input methods and capabilities

---

## One Web
# Connection

^ WiFi, cell signal

---

## One Web
# Disabilities

^ blind web users, old people, people with injury

---

# Progressive Enhancement

---

# The Triangle

^ HTML for structured content
CSS for presentation
JavaScript for behaviour

---

# A basic, functional, experience is delivered to everyone

---

# Different browsers will be served different experiences

---

# Feature tests in JS
# load in enhancements

^ for browsers that pass the tests

---

# Cutting the Mustard

---

```javascript
if('querySelector' in document
   && 'localStorage' in window
   && 'addEventListener' in window) {
   // bootstrap the javascript application
}
```

---

# Support vs Optimisation

---

# **Responsive Web Design**

---

## Responsive Web Design

# fluid grid

---

## Responsive Web Design

# flexible images

---

## Responsive Web Design

# media queries

---

## fluid grid

# `%` instead of `px`

^ when specifying widths of containers

---

## flexible images

# add `max-width: 100%; height: auto;`

^ to let your images shrink to their containers, and use `srcset` or the `picture` elements to provide the browser with different sized images;

---

## media queries

```css
@media (min-width: 60em) {
  /* styles for wide screen */
}
```

^ like font size and layout
breakpoints

---

# Mobile First

^ Start with a small screen, and make your content, design, and development decisions there. The thinking behind it is that focusing on mobile gives us the strongest set of constraints and forces us to make difficult decisions early.

---

# **Performance**

---

# latency harsher than bandwidth

^ load time is more affected by number of network requests than the size of the file

---

# Inline, Internal, and External CSS

---

# Inline

```html
<p style="color: red;">Help!</p>`
```

---

# Internal

```html
<style>p { color: red; }</style>
```

---

# External

```html
<link rel="stylesheet" href="style.css" />
```

---

# Inline, Internal, and External JS

---

# Inline

```html
<p onClick="help()">Help!</a>
```

---

# Internal

```html
<script>console.log('Help!');</script>
```

---

# External

```html
<script src="help.js"></script>
```

---

# External best

# modular, reusable, code

---

# Concatenation, Minification, Gzip

---

# Technology and Tools

---

## Technology and Tools

# Frameworks
# HTML, CSS, JavaScript
# Testing
