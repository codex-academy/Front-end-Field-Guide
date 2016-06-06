---
layout: default
title: Progressive Enhancement
---

# Progressive Enhancement

A basic, functional, experience is delivered to everyone; JavaScript is not required for any key functionality. Feature tests in JavaScript are used to load in additional CSS and JS enhancements for browsers that pass the tests. It's important that these are treated as an enhancement rather than a fallback: we build a solid foundation and layer on enhancements. Different browsers will be served different experiences; they will be consistent and may be quite similar, but will not be identical.

Rather than grading browsers, we [grade components](https://www.filamentgroup.com/lab/grade-the-components.html). This provides each browser with the best experience it can handle. We use [Strong Progressive Enhancement](http://alexmaughan.com/weak-vs-strong-progressive-enhancement/#content).

[caniuse.com](http://caniuse.com/) is a very handy site: it lists browser support for HTML, CSS, and JavaScript features.

## Cutting the Mustard

[Cutting the Mustard](http://responsivenews.co.uk/post/18948466399/cutting-the-mustard) (when referring to JavaScript) was coined by the team working on the responsive redesign of the BBC news website. They provide a basic experience for all browsers: they serve HTML, images, and CSS. Then, for browsers that are modern enough, they serve the enhanced, JavaScript-powered version. By doing this, they avoid sending less capable browsers code that they will struggle to run. They use the following test:

```javascript
if('querySelector' in document
   && 'localStorage' in window
   && 'addEventListener' in window) {
   // bootstrap the javascript application
}
```

They picked those criteria based on the things the features that their app used. If you cut the mustard in your own project, you should test for features that you'll be using. [Modernizr](https://modernizr.com/) can be a useful tool to use for this.

There are levels of optimisation to apply. Your site should support every browser, but the amount of time you spend optimising for particular browsers and feature sets should depend on your audience.pe
