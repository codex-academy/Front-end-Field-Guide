---
layout: default
title: HTML
---

# HTML

* Use the right element: semantics matter. Headings should use `<h1>` down to `<h6>`, buttons should be `<button>`s,  links should be `<a href="">`s not styled `<div>`s or `<span>`s, and lists should be `ul`s or `ol`s.
* Use as little markup as possible. Rather than adding an extra element, see if it's possible to apply CSS to an existing element instead.
* Use HTML5 elements like `nav` and `main`.
* Use HTML5 form features like `<input type="email" >` and the `required` attribute.
* Add extra information to your pages using structured metadata, such [Schema.org](http://schema.org/) markup. This allows services to parse and read your data more correctly, and can [enhance the display of your site in search results ](https://developers.google.com/structured-data/).

## Accessibility

Many people browse the web using assistive technology such as screen readers, or use a keyboard to move around pages instead of a mouse or trackpad.

Using semantically correct HTML elements gives you a lot of baked-in accessibility, but you can add WAI-ARIA (Web Accessibility Initiative Accessible Rich Internet Applications) markup to provide extra information about your page, such as landmark `role`s (such as `main` and `aside`) to allow users to jump between sections of your site.

Make sure that every form input has a label, attached using the `for` attribute or with the input nesting inside the label. Only use `placeholder` to provide extra information, not as a replacement for a label.

Leave control in the hands of the user: don't open links in new tabs, and don't disable zooming using the `meta` `viewport` tag.

## Images

Images take up most of the size of a web page. It's important to [use the right format](http://designingforperformance.com/optimizing-images/#choosing-an-image-format) for the type of image, and to provide the smallest size that you can using [responsive images](https://responsiveimages.org/).

Every image must have an have an `alt` attribute that describes the image. It provides alternate content for assistive technology users, and it's the text that displays if the image fails to load.

Look at using the `srcset`and `sizes` attributes for `img` to provide different size images for different size screens. If you need to show different pictures (such as different crops of the same image) at different screen sizes, look at the `picture` element.
