---
layout: default
title: CSS
---

# CSS

CSS should be kept in a few, minified, external CSS files. Don't use inline style blocks or write inline CSS. (There is an exception to this guideline: when your CSS is very, very, small and can be included in the document so that the page has one less HTTP request)

It can help to use a style guide to keep your code consistent and readable. Check your code for errors and complexity using something like [CSS Lint](http://csslint.net/) (there's [an example file](./.csslintrc) in this Guide). Use [SMACSS](http://www.smacss.com/) as a guideline for writing your CSS. Organise your files into: Base; Layout; (lots of) Modules; States.

## Guidelines

* Use CSS in places of images where possible.
* Keep selectors simple (use `nav a` instead of `nav ul li a`), and don't over-qualify them (use `.news` instead of `div.news`)
* Use shorthand. Use `padding: 1em 2em` instead of individual padding properties.
* Don't use ID selectors or `!important`.
* Use CSS for animation instead of JavaScript. position, scale, rotation, and opacity can all be [animated cheaply by the browsers](http://www.html5rocks.com/en/tutorials/speed/high-performance-animations/).
* Use names that make sense to you, future you, and your team. Describe the purpose, not the properties or presentation.
*  Use Progressive Enhancement for newer CSS features. If you set colour using `rgba`, set it using `rgb`on the line before.

## Preprocessors

[Sass](http://sass-lang.com/), [Less](http://lesscss.org/), and other preprocessors can be helpful for writing CSS. Remember to keep it simple, though. Think about just using variables, imports, mixins, and (the more friendly way of using) Media Queries.
