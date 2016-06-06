---
layout: default
title: Responsive Web Design
---

# Responsive Web Design

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
