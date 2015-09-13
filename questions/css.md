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