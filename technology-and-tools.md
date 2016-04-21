# Technology and tools

## Frameworks

Frameworks can be useful, but be wary of using them by default. Think carefully about the problem you're solving by using a particular framework, and about the cost of using it to you, your team, and your users.

Frameworks have some Pros. They:

* can make complex things simpler;
* are often well maintained and well tested.

Frameworks also have some Cons. They:

* add a dependency to your project;
* can be overkill for the problem you are trying to solve;
* can be painful to upgrade;
* can have a steep learning curve;
* are solving someone else's problem, not yours.

Roll your own framework, but borrow from the best. Look at [Bootstrap](http://getbootstrap.com/), [Foundation](http://foundation.zurb.com/), and other frameworks for ideas.

## HTML

* Use the appropriate element: semantics matter. Headings should use `<h1>` down to `<h6>`, buttons should be `<button>`s,  links should be `<a href="">`s not styled `<div>`s or `<span>`s, and lists should be `ul`s or `ol`s.
* Use as little markup as possible. Rather than adding an extra element, see if it's possible to apply CSS to an existing element instead.
* Use HTML5 elements like `nav` and `main`.
* Use HTML5 form features like `<input type="email" >` and the `required` attribute.
* Add extra information to your pages using structured metadata, such [Schema.org](http://schema.org/) markup. This allows services to parse and read your data more correctly, and can [enhance the display of your site in search results ](https://developers.google.com/structured-data/).


### Accessibility

Many people browse the web using assistive technology such as screen readers, or use a keyboard to move around pages instead of a mouse or trackpad.

Using semantically correct HTML elements gives you a lot of baked-in accessibility, but you can add WAI-ARIA (Web Accessibility Initiative Accessible Rich Internet Applications) markup to provide extra information about your page, such as landmark `role`s (such as `main` and `aside`) to allow users to jump between sections of your site.

Make sure that every form input has a label, attached using the `for` attribute or with the input nesting inside the label. Only use `placeholder` to provide extra information, not as a replacement for a label.

Leave control in the hands of the user: don't open links in new tabs, and don't disable zooming using the `meta` `viewport` tag.

### Images

Images take up most of the size of a web page. It's important to [use the right format](http://designingforperformance.com/optimizing-images/#choosing-an-image-format) for the type of image, and to provide the smallest size that you can using [responsive images](https://responsiveimages.org/).

Every image must have an have an `alt` attribute that describes the image. It provides alternate content for assistive technology users, and it's the text that displays if the image fails to load.

Look at using the `srcset`and `sizes` attributes for `img` to provide different size images for different size screens. If you need to show different pictures (such as different crops of the same image) at different screen sizes, look at the `picture` element.

## CSS

CSS should be kept in a few, minified, external CSS files. Don't use inline style blocks or write inline CSS. (There is an exception to this guideline: when your CSS is very, very, small and can be included in the document so that the page has one less HTTP request)

It can help to use a style guide to keep your code consistent and readable. Check your code for errors and complexity using something like [CSS Lint](http://csslint.net/) (there's [an example file](./.csslintrc) in this Guide). Use [SMACSS](http://www.smacss.com/) as a guideline for writing your CSS. Organise your files into: Base; Layout; (lots of) Modules; States.

### Guidelines

* Use CSS in places of images where possible.
* Keep selectors simple (use `nav a` instead of `nav ul li a`), and don't over-qualify them (use `.news` instead of `div.news`)
* Use shorthand. Use `padding: 1em 2em` instead of individual padding properties.
* Don't use ID selectors or `!important`.
* Use CSS for animation instead of JavaScript. position, scale, rotation, and opacity can all be [animated cheaply by the browsers](http://www.html5rocks.com/en/tutorials/speed/high-performance-animations/).
* Use names that make sense to you, future you, and your team. Describe the purpose, not the properties or presentation.
*  Use Progressive Enhancement for newer CSS features. If you set colour using `rgba`, set it using `rgb`on the line before.


### Preprocessors

[Sass](http://sass-lang.com/), [Less](http://lesscss.org/), and other preprocessors can be helpful for writing CSS. Remember to keep it simple, though. Think about just using variables, imports, mixins, and (the more friendly way of using) Media Queries.

## JavaScript

Write unobtrusive JS. Keep all JS in a few, minified, external files. Don't use inline script blocks or write inline JS. Only include [jQuery](http://jquery.com/) when really necessary, since [parse and execution time of large JS files can be slow](http://timkadlec.com/2014/09/js-parse-and-execution-time/). Prefer vanilla JavaScript code and [micro-frameworks](http://microjs.com/). Before including a library to polyfill a feature, considering the cost to your users.

It can help to use [a style guide](http://jscs.info/) to keep your code consistent and readable (there's [an example file](./.jscsrc) in this Guide). Check your code for errors and complexity using something like [JS Hint](http://jshint.com/) (there's [an example file](./.jshintrc) in this Guide).

## Testing

It's very important that your code is tested: you want to be sure that your code does what you think it does. Use a framework that you're comfortable with, and test as much of the code as is sensible.

Use tools to help with other types of testing:

* [PageSpeed](https://developers.google.com/speed/pagespeed/insights/) to generate a checklist of things to improve;
* [WebPageTest](http://www.webpagetest.org/) to generate stats and measure performance;
* [pa11y](http://pa11y.org/) to check accessibility.
