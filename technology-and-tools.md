# Technology and tools

Friendly formatting.

## Frameworks

* Don't use them by default.
* Who does this help? Me or my users?

Pros

* Makes complex things simple(r)
* Well maintained, well tested

Cons

* Adds a dependency
* Can be overkill
* Can be painful to upgrade
* Solving their problem(s), not yours

## HTML

* Use the right element


### HTML5

### Accessiblity

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
* use the cascade
* don't over-qualify selectors
* use friendly formatting
* non-jQ animation

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

#### Style Guides
