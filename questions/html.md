Html Questions
==============

**What does a doctype do?**

Doctype is required preamble. It's required for legacy reasons. Browsers use different render mode that is incompatible with some specifications. Doctype shows browsers how to render the page and follow specifications.

**What's the difference between standards mode and quirks mode?**

In *quirks mode* layout emulate nonstandard behavior in Navigator 4 and Internet Explorer 5. In *standards mode* behavior is the behavior described by HTML and CSS specifications.

**What's the difference between HTML and XHTML?**

HTML5 has two parsing modes: HTML and XML. The difference depends on *Content-type* header (for HTML it's *text/html*, for XML - *text/xml+xhtml*);

For *text/html* you should apply following rules:

- start tags are not required for all elements;
- end tags are not required for all elements;
- only **void** elements (*br*, *img*, *link*) can be self-closed;
- tags and attributes are case insensitive;
- attributes don't need to be quoted;
- attributes can be empty (*checked*, *disabled*);
- special characters don't have to be escaped;

For *text/xml+xhtml* you should use opposite rules (some of them):

- non void tags (*p*, *li*) must have end tag;
- any element can be self-closed;

**How do you serve a page with content in multiple languages?**

If you want to use multiple languages, you should add *lang* attribute for *HTML* documents and *xml:lang* for *XHTML* documents. For default language you have to add *lang* attribute to *<html>* tag. If some text blocks on your page are using multiple languages you should add *lang* attribute them as well.

**What kind of things must you be wary of when design or developing for multilingual sites?**

The first think that comes to my mind is text direction. For some languages such as Arabic and Jewish you should use *LTR*. You have to keep in mind it and design site with that point.

Also word length variates in different languages ('buy' and 'купить'). It cans break design as well.

**What are data- attributes good for?**

You can store some values for JavaScript in those custom attributes. It easily accessible from scripts and libraries such as JQuery. *dataset* in *HTMLElement*.

**Consider HTML5 as an open web platform. What are the building blocks of HTML5?**

- more semantic markup;
- new form elements (input type attribute);
- video and audio tags;
- new JS API;
- canvas and SVG;
- new Data storage;
- geolocation API;
- web- and service-workers;

**Describe the difference between a cookie, sessionStorage and localStorage**

The main difference between *cookie* and *local storage* is sending them to the server with each request. localStorage is persistent, but sessionStorage is nonpersistent and scoped only to current window (stores data for one session).

**Describe the difference between script, script async and script defer.**

Tag *script* can be used for internal JavaScript code and for including external scripts by using *src* attribute. Attrbutes *async* and *defer* have to be used only for external scripts.

Attribute *async* specifies that script is executed asynchronously (executes when downloading is finished).

Attribute *defer* specifies that script is executed when page has finished parsing (keeps order).
