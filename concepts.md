# Concepts

## One Web

Websites should be built so that people can access them quickly and easily, regardless of the device they're using, the type of connection they are on, or any disabilities they have. That means building things with **Progressive Enhancement**, and embracing the [fluid nature of the web](http://alistapart.com/article/dao).

## Progressive Enhancement

A basic, functional, experience is delivered to everyone; JavaScript is not required for any key functionality. Feature tests in JavaScript are used to load in additional CSS and JS enhancements that the browser can handle. Different browsers will be served different experience; they will be consistent and may be quite similar, but will not be identical.

Front-end performance and accessibility are important, so running regular performance and accessibility audits is recommended.

[Grade components, not browsers](https://www.filamentgroup.com/lab/grade-the-components.html).

### Cutting the Mustard

[Cutting the Mustard](http://responsivenews.co.uk/post/18948466399/cutting-the-mustard) (when referring to JavaScript) was coined by the team working on the responsive redesign of the BBC news website. They provide a basic experience for all browsers, serving HTML, images, and CSS. Then, for browsers that are modern enough, they serve the enhanced, JavaScript-powered version. They do this using the following test:

```javascript
if('querySelector' in document
   && 'localStorage' in window
   && 'addEventListener' in window) {
   // bootstrap the javascript application
}
```

They picked those critera based on the things the features that their app used. If you cut the mustard in your own project, you might just test for `querySelector` and `addEventListener` support.

The important thing to note is that the are levels of optimisation to apply. Your site should support every browser, but the amount of time you spend optimising for particular browsers and feature sets should depend on your audience.

## Responsive Web Design

The term Responsive web design was coined by [Ethan Marcotte](http://unstoppablerobotninja.com/) back in May of 2010 in [an article for A List Apart](http://alistapart.com/article/responsive-web-design). He put forward three keys aspects:

1. a fluid grid;
2. flexible images;
3. media queries.

These things together let us make fluid, squishy, web sites that will be happy whatever screen size they're displayed on.

In practical terms, this means:

1. use `%`s instead of `px` when specifying widths of containers;
2. add `max-width: 100%; height: auto;` to let your images shrink to their containers, and use `srcset` or the `picture` elements to provide the browser with different sized images;
3. use media queries to change type size and layout depending on the size of the screen.

An important thing to remember is not to use device-specific breakpoints. Use your content to decide the breakpoints, and specify them in fluid units like `em`s.

## Mobile First

Luke Wroblewski has written extensively on [his site](http://www.lukew.com/), and in [his book](http://www.lukew.com/resources/mobile_first.asp), about designing Mobile First. Start with a small screen, and make your content, design, and development decisions there. The thinking behind it is that focusing on mobile gives us a strongest set of constraints and forces us to make the difficult decisions.

Doing Mobile First Responsive Web Design brings some additional benefits: easier support for devices that don't support media queries, usually older phones. Your initial styles are loaded without any media queries. Then, more advanced styles are loaded in use media queries as a qualifier (e.g. `media (min-width: 30em)`).

## Future Friendly

Being [Future Friendly](https://www.futurefriendly.co.za/) is all about accepting the unknown, unpredictable, nature of building things for the web. We don't know what device or network a person will be using, or whether they're using any assistive technology. All we know is that we don't know. Future Friendly was put forward as a way to handle this overwhelming diversity:

* Acknowledge and embrace unpredictability.
* Think and behave in a [future-friendly](https://www.futurefriendly.co.za/) way.
* Help others do the same.

## Performance

Research is currently showing that [latency, not bandwidth, is the toughest constraint affecting network requests](https://www.igvita.com/2012/07/19/latency-the-new-web-performance-bottleneck/). The load time of a web page is [more affected by number of network requests than the size of the file](http://www.nateberkopec.com/2015/11/05/page-weight-doesnt-matter.html).

That means that when we're building a website, we prefer fewer, larger, HTTP requests to many, smaller, ones. It's a bit of a balancing act, though.

### Inline, Internal, and External (CSS and JS)

You can write inline CSS by adding it HTML elements (`<p style="color: red;">Help!</p>`), by adding it on a page (`<style>p { color: red; }</style>`), or by including it as an external file (`<link rel="stylesheet" href="style.css" />`).

Similar things are true for where you add your JavaScript. You can write JS inline (`<p onClick="help()">Help!</a>`), by adding it on a page (`<script>console.log('Help!');</script>`), or by including it as an external file (`<script src="help.js"></script>`).

For both CSS and JavaScript, the last way is by far the best. It lets you write modular, reusable, code. The first two methods mean you have to make updates in multiple places, and might struggle to keep things consistent.

### Caching

### Concatenation, Minification, Gzip

## User Experience

* Auto-playing anything. Let users control their own experience.

### Heuristics

### Usability Testing

## Process

Style Tiles

### Front-end Style Guides

[Pattern Lab, Atomic Design](http://patternlab.io/about.html).

Atoms, Molecules, Organisms, Ecosystems.

[Style Guide Driven Development](http://blog.bitovi.com/style-guide-driven-development/)
