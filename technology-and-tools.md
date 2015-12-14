# Technology and tools

## Frameworks

Frameworks can be useful, but be wary of using them by default. Think carefully about the problem you're solving by using a particular framework, and about the cost of using it to your team, and to your users.

Frameworks have some Pros. They:

* can make complex things simple(r);
* are often Well maintained and well tested.

Frameworks also have some Cons. They:

* add a dependency to your project;
* can be overkill for the problem you are trying to solve;
* can be painful to upgrade;
* are solving someone else's problem, not yours.

## HTML

* Use the appropriate element: semantics matter. Buttons should be `<button>`s, and links should be `<a href="">`s, not styled `<div>`s or `<span>`s.
* Use as little markup as possible. Rather than adding an extra element, see if it's possible to add CSS to an existing element instead.

### HTML5

* Use HTML5 elements like `nav` and `main`.
* Use new form features like `<input typ="email" >` and the `required` attribute.

These give you extra semantics and improve accessibility.

### Accessibility

Many people browse the web using assistive technology such as screen readers, or use a keyboard to move around pages instead of a mouse or trackpad.

Using semantically correct HTML elements gives you a lot of baked-in accessibility, but you can add WAI-ARIA (Web Accessibility Initiative Accessible Rich Internet Applications) markup to provide extra information about your page, such as landmark `role`s to allow users to jump between sections of your site.

### Metadata

### Images

* Use the right format
* Use the right size

### Templating

## CSS

CSS should be kept in a few, minified, external CSS files. Don't use inline style blocks or write inline CSS.

Write CSS like [SMACSS](http://www.smacss.com/). CSS is organised into: Base; Layout; (lots of) Modules; States. Kepp nesting shallow, and never use IDs for styling.

Make sites Responsive by default as a Future Friendly measure.

Prefer to move into HTML, CSS, and JS sooner rather than later and build [Front-end Style Guides](http://styleguides.io/) (something like [Pattern Lab](http://patternlab.io/)) that evolve into pages and templates.

* don't use `!important`
* don't use IDs
* do use the cascade
* don't over-qualify selectors
* do use friendly formatting
* do use CSS for animation instead of JavaScript
* do write as little CSS as possible

### Naming conventions

* Names that make sense to you, future you, and your team.
* Describe the purpose, not the properties.

### Frameworks

* roll your own framework, but borrow from the best.
* bootstrap et al
* de-bootstrapping: learn from the pieces and make your own.

### Preprocessors

Keep it simple: variables, imports, mixins, better Media Queries.

## JavaScript

Write unobtrusive, js-hinted, JS. Keep all JS in a few, minified, external files.Don't use inline script blocks or write inline JS. Only include [jQuery](http://jquery.com/) when really necessary; prefer vanilla JavaScript code and [micro-frameworks](http://microjs.com/).

[Cut the Mustard](http://responsivenews.co.uk/post/18948466399/cutting-the-mustard) to serve less capable browsers just the core, lighter and faster, experience, rather than send them lots of code they will struggle to run.

Use as little JS as you can, and optimise it a lot.

* JSHint, JSCS
* non-jQ animation

### Libraries and Frameworks

* jQuery vs JS

jQuery Pros

* Avoid bugs (even in modern browsers)
* CDNs

jQuery Cons

* [Parse and execution time can be slow](http://timkadlec.com/2014/09/js-parse-and-execution-time/)
*


### Things that compile to JavaScript

## Task runners

## Testing

### Test Frameworks

### PageSpeed and WebPageTest

## Version Control

## Code quality and readability

#### Linting and Hinting

Friendly formatting.

#### Style Guides
