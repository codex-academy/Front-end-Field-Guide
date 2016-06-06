---
layout: default
title: JavaScript
---

# JavaScript

Write unobtrusive JS. Keep all JS in a few, minified, external files. Don't use inline script blocks or write inline JS. Only include [jQuery](http://jquery.com/) when really necessary, since [parse and execution time of large JS files can be slow](http://timkadlec.com/2014/09/js-parse-and-execution-time/). Prefer vanilla JavaScript code and [micro-frameworks](http://microjs.com/). Before including a library to polyfill a feature, considering the cost to your users.

It can help to use [a style guide](http://jscs.info/) to keep your code consistent and readable (there's [an example file](./.jscsrc) in this Guide). Check your code for errors and complexity using something like [JS Hint](http://jshint.com/) (there's [an example file](./.jshintrc) in this Guide).
