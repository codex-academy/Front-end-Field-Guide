---
layout: default
title: Performance
---

# Performance

Research is showing that [latency, not bandwidth, is the toughest constraint affecting network requests](https://www.igvita.com/2012/07/19/latency-the-new-web-performance-bottleneck/). The load time of a web page is [more affected by number of network requests than the size of the file](http://www.nateberkopec.com/2015/11/05/page-weight-doesnt-matter.html).

That means that when we're building a website, we prefer fewer, larger, HTTP requests to many, smaller, ones. It's a bit of a balancing act, though.

## Inline, Internal, and External CSS and JS

You can write inline CSS by adding it HTML elements

```html
<p style="color: red;">Help!</p>`
```

by adding it on a page

```html
<style>p { color: red; }</style>
```

or by including it as an external file

```html
<link rel="stylesheet" href="style.css" />
```

Similar things are true for where you add your JavaScript. You can write JS inline

```html
<p onClick="help()">Help!</a>
```
by adding it on a page

```html
<script>console.log('Help!');</script>
```

or by including it as an external file

```html
<script src="help.js"></script>
```

For both CSS and JavaScript, the last way is by far the best: including as an external file. It lets you write modular, reusable, code. The first two methods mean you have to make updates in multiple places, and might struggle to keep things consistent.

## Caching

The fastest request for a resource (like an image, a CSS file, or a JavaScript file) is the one that doesn't get made: if the file is served from the cache instead of from the network. Setting far future expiry dates on caches can work well when combined with updating the filenames when the contents change.

## Concatenation, Minification, Gzip

So that we serve fewer files to the user, we can concatenate assets into one or two CSS and JavaScript files. To reduce file sizes, we can use minification (the process of removing extra whitespace and line breaks, and more), usually as part of a build process. To make these files even smaller, we can enable gzip on our server: this sends a compressed resource that's then decompressed once it reaches the user.
