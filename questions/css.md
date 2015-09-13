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

You have to aware parent collapsing problem. If element contains nothing but floated elements it's height will equal zero. 