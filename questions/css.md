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

- You can apply `clear: both;` property to element;
- Empty div method is adding `<div style="clear: both;"></div>`. Sometimes developers add `<br/>` tag instead of div, but `<div>` has no side-effects and has no browser default styling;
- Add `overflow: auto` or `overflow: hidden` to parent element to clear flow context. That method can add unwanted scroll-bars or hide some elements;
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

You should remember the stacking context. It means the hierarchy of stacking context