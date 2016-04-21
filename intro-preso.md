# *Front-end Overview*

---

# One Web
# Responsive Web Design
# Performance
# Frameworks

---

# *One Web*

^ device, connection, disabilities

---

## **One Web**
# Device

^ different input methods and capabilities

---

## **One Web**
# Connection

^ WiFi, cell signal

---

## **One Web**
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

# *Responsive Web Design*

---

## Responsive Web Design

# fluid grid

---

## **Responsive Web Design**

# flexible images

---

## **Responsive Web Design**

# media queries

---

## **fluid grid**

# `%` instead of `px`

^ when specifying widths of containers

---

## **flexible images**

# add `max-width: 100%; height: auto;`

^ to let your images shrink to their containers, and use `srcset` or the `picture` elements to provide the browser with different sized images;

---

## **media queries**

## @media (min-width: 60em) {<br>...<br>}


^ like font size and layout
breakpoints

---

# Mobile First

^ Start with a small screen, and make your content, design, and development decisions there. The thinking behind it is that focusing on mobile gives us the strongest set of constraints and forces us to make difficult decisions early.

---

# *Performance*

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

# External is best

# modular, reusable, code

---

# Concatenation
# Minification
# Gzip

---


# *Frameworks*

^ Pros and Cons

---

## Frameworks: Pros

# can make complex things simpler

---

## Frameworks: Pros

# often well maintained and well tested

---

## Frameworks: Cons

# add a dependency to your project

---

## Frameworks: Cons

# can be overkill for the problem you are trying to solve

---

## Frameworks: Cons

# can be painful to upgrade

---

## Frameworks: Cons

# can have a steep learning curve

---

## Frameworks: Cons

# are solving someone else's problem, not yours

---

# Roll your own framework, but borrow

# Bootstrap
# Foundation

---

# fef.projectcodex.co

---

# *Front-end Overview*
