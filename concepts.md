# Concepts

## One Web

Websites should be built so that people can access them quickly and easily, regardless of the device they're using (which will mean different input methods and capabilities), the type of connection they are on, or any disabilities they have. That means building things with **Progressive Enhancement**, and embracing the [fluid nature of the web](http://alistapart.com/article/dao).

Robust websites should be built with a separation of concerns: HTML for structured content; CSS for presentation; JavaScript for behaviour. The JavaScript should add any extra markup it needs.

## Progressive Enhancement

A basic, functional, experience is delivered to everyone; JavaScript is not required for any key functionality. Feature tests in JavaScript are used to load in additional CSS and JS enhancements for browsers that pass the tests. It's important that these are treated as an enhancement rather than a fallback: we build a solid foundation and layer on enhancements. Different browsers will be served different experience; they will be consistent and may be quite similar, but will not be identical.

Rather than grading browsers, we [grade components](https://www.filamentgroup.com/lab/grade-the-components.html). This provides each browser with the best experience it can handle. We use [Strong Progressive Enhancement](http://alexmaughan.com/weak-vs-strong-progressive-enhancement/#content).

### Cutting the Mustard

[Cutting the Mustard](http://responsivenews.co.uk/post/18948466399/cutting-the-mustard) (when referring to JavaScript) was coined by the team working on the responsive redesign of the BBC news website. They provide a basic experience for all browsers: they serve HTML, images, and CSS. Then, for browsers that are modern enough, they serve the enhanced, JavaScript-powered version. By doing this, they avoid sending less capable browsers code that they will struggle to run. They use the following test:

```javascript
if('querySelector' in document
   && 'localStorage' in window
   && 'addEventListener' in window) {
   // bootstrap the javascript application
}
```

They picked those criteria based on the things the features that their app used. If you cut the mustard in your own project, you should test for features that you'll be using.

There are levels of optimisation to apply. Your site should support every browser, but the amount of time you spend optimising for particular browsers and feature sets should depend on your audience.

## Responsive Web Design

The term Responsive web design was coined by [Ethan Marcotte](http://unstoppablerobotninja.com/) back in May of 2010 in [an article for A List Apart](http://alistapart.com/article/responsive-web-design). He put forward three keys aspects:

1. a fluid grid;
2. flexible images;
3. media queries.

These things together let us make fluid, squishy, websites that will be happy whatever screen size they're displayed on.

In practical terms, this means:

1. use `%`s instead of `px` when specifying widths of containers;
2. add `max-width: 100%; height: auto;` to let your images shrink to their containers, and use `srcset` or the `picture` elements to provide the browser with different sized images;
3. use media queries to change the presentation (like font size and layout) of your web page, depending on the size of the user's screen. Use your content to decide the breakpoints in fluid units like `em`s, rather than device-specific breakpoints in `px`.

## Mobile First

Luke Wroblewski has written extensively on [his site](http://www.lukew.com/), and in [his book](http://www.lukew.com/resources/mobile_first.asp), about designing Mobile First. Start with a small screen, and make your content, design, and development decisions there. The thinking behind it is that focusing on mobile gives us the strongest set of constraints and forces us to make difficult decisions early.

Doing Mobile First Responsive Web Design brings some additional benefits: easier support for devices that don't support media queries, usually older mobile devices. Your initial styles are loaded without any media queries. Then, more advanced styles are loaded in using media queries as a qualifier (e.g. `media (min-width: 30em)`).

## Future Friendly

Being [Future Friendly](https://www.futurefriendly.co.za/) is all about accepting the unknown, unpredictable, nature of building things for the web. We don't know what browser, screen size, network speed, or input type a person will be using. All we know is that we don't know. Future Friendly was put forward as a way to handle this overwhelming diversity:

* Acknowledge and embrace unpredictability.
* Think and behave in a [future-friendly](https://www.futurefriendly.co.za/) way.
* Help others do the same.

Sites should be Responsive by default as a Future Friendly measure.

## Performance

Research is currently showing that [latency, not bandwidth, is the toughest constraint affecting network requests](https://www.igvita.com/2012/07/19/latency-the-new-web-performance-bottleneck/). The load time of a web page is [more affected by number of network requests than the size of the file](http://www.nateberkopec.com/2015/11/05/page-weight-doesnt-matter.html).

That means that when we're building a website, we prefer fewer, larger, HTTP requests to many, smaller, ones. It's a bit of a balancing act, though.

### Inline, Internal, and External CSS and JS

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

### Caching

The fastest request for a resource (like an image, a CSS file, or a JavaScript file) is the one that doesn't get made: if the file is served from the cache instead of from the network. Setting far future expiry dates on caches can work well when combined with updating the filenames when the contents change.

### Concatenation, Minification, Gzip

So that we serve fewer files to the user, we can concatenate assets into one or two CSS and JavaScript files. To reduce file sizes, we can use minification (the process of removing extra whitespace and line breaks, and more), usually as part of a build process. To make these files even smaller, we can enable gzip on our server: this sends a compressed resource that's then decompressed once it reaches the user.

## Process

### Front-end Style Guides


We shouldn't be designing websites as pages anymore: we should be designing systems of components. A popular way to think about this is to use Brad Frost's [Atomic Design](http://patternlab.io/about.html). A site is divided into tiny pieces that are combined into components, then those components are combined into bigger components. A useful way to look at the system is: Atoms, Molecules, Organisms, Ecosystems. Anna Debenham has an excellent set of [Style Guide-related resources](http://styleguides.io/).

Starting from this point, and using [Style Guide Driven Development](http://blog.bitovi.com/style-guide-driven-development/) can be very powerful, and help everyone on the team have their head in the right space for designing and developing for the multi-device world.

Ideally, a Style Guide should be part of your application. The folks at Lonely Planet have done this with [Rizzo](http://rizzo.lonelyplanet.com/). If you can't do this for your application, the next best thing is for the Style Guide and application to use the same CSS and JS files.
