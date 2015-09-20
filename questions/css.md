CSS Questions
=============

**What is the difference between classes and ID's in CSS?**

First of all you should not place elements with same ID in page more then once. That's why you can select only one element by ID. Classes more flexible in that case. You can make multiple selections by class name.
ID selector starts by #-hash sign, class selectors start by "."-dot symbol.

**What's the difference between "resetting" and "normalizing" CSS?**

Normalizing is preserving useful defaults rather then "unstyling" everything. It fixes some common bugs like: 
- display settings for HTML5 elements;
- font inheritance for form element;
- font-size rendering for `pre` element;

**Describe Floats and how they work.**

To understand **float** purpose we can look at print design. In a print layout images may be set the page such that text wraps around them as needed.

In web design elements with `float` css-property are just like images in print layout. Floated elements *remain a part of the flow of the web page*. It's not like elements with absolute position, they are **removed** from web page flow. Absolutely positioned page elements don't affect the position of other elements.

Floated elements can be used to make column layout or horizontal navigation bar.

You have to aware parent collapsing problem. If element contains nothing but floated elements it's height will equal zero. To prevent this case you should clear floating.

Methods to clear floats:

- You can apply `clear: both;` property to element.
- Empty div method is adding `<div style="clear: both;"></div>`. Sometimes developers add `<br/>` tag instead of div, but `<div>` has no side-effects and has no browser default styling.
- Add `overflow: auto` or `overflow: hidden` to parent element to create own block formatting context. That method can add unwanted scroll-bars or hide some elements.
- CSS pseudo `:after` element: 
```css
.clearfix:after { 
   content: "."; 
   visibility: hidden; 
   display: block; 
   height: 0; 
   clear: both;
}
```

**Describe z-index and how stacking context is formed.**

This property represents the position of the element along the z-axis. It's like several layers one above another.

`z-index: 1;` can be integer value (positive or negative) or `auto`. It can be applied to elements with `position: absolute` (relative, fixed). Elements with higher `z-index` will be above another elements with lower `z-index` or without this property.

You should remember the stacking context. It means the hierarchy of stacking context is a subset of hierarchy of HTML elements, because only certain elements can create stacking contexts. If element doesn't create it's own stacking context it will be assimilated by the parent stacking context.
![stacking context](https://developer.mozilla.org/@api/deki/files/913/=Understanding_zindex_04.png)

**Describe BFC(Block Formatting Context) and how it works.**

A block formatting context is a part of a visual CSS rendering of a web page. It is a region in which the layout of block boxes occurs and in which floating elements interact with each other.

A BFC can be created by one of this methods:

- the root element or something contains it.
- floats.
- `position: absolute; /* fixed */`.
- `display: inline-block; /* table-cell, table-caption */`.
- `overflow` other than `visible`.
- `display: flex; /* inline-flex */`.

BFC is important in positioning and clearing floats.

**Explain CSS sprites, and how you would implement them on a page or site.**

CSS-Sprite is method to combine multiple images into one. It reduces the query count, loads many images once, can reduce image size.

To use sprites on the page you can play with `backgroud-position:` property. You should increase or decrease **x** or **y** image offset. Usually you have to set `background-repeat: no-repeat;`.

**How would you approach fixing browser-specific styling issues?**

Usually I apply some hacks on it. You can read more about it on the site [browserhacks.com](http://browserhacks.com).

**How do you serve your pages for feature-constrained browsers?**

Sometimes I'm using vendor prefixes and trying to gather all those code into separate file (ex: ie8.css). 

I prefer to use graceful degradation, that's why I'm making pages for modern browsers and then adding some styles for older ones.

**What are the different ways to visually hide content (and make it available only for screen readers)?**

There are a lot of techniques: 
- use `text-indent: -999999px;`  (some huge number)
- use `height: 0; overflow: hidden;` for element containing text
- ...

There is a good article about CSS Image Replacement on [css-tricks.com](https://css-tricks.com/css-image-replacement/).

**Have you ever used a grid system, and if so, what do you prefer?**

Yep, I used grid system and a lot. More often I made a deal with Twitter Bootstrap. 

Grid systems make my life easier when I'm creating web page. It allows me quickly make markup with columns, sidebars etc.

**Have you used or implemented media queries or mobile specific layouts/CSS?**

Well, media query is a good thing to specify css rules only to some window width (height...). I used it for making responsive pages, that display well in desktop and mobile browsers.