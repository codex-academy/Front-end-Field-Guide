# Concepts

## One Web

Websites should be built so that people can access them quickly and easily, regardless of the device they're using, the type of connection they are on, or any disabilities they have. That means building things with **Progressive Enhancement**.

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

Don't use device-specific breakpoints. Let your content decide your breakpoints.

Build squishy things.

## Mobile First

Content first, navigation second.

## Future Friendly

* Acknowledge and embrace unpredictability.
* Think and behave in a [future-friendly](https://www.futurefriendly.co.za/) way.
* Help others do the same.

## Performance

* Prefer fewer, larger HTTP requests to many, smaller, ones.

### Inline, Internal, and External (CSS and JS)

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
