General Questions
=================

**What did you learn yesterday/this week?**

I started to reading about *webpack* and it's configurations. Also I learned how to integrate style-files into js and import it into html page. It's awesome.
Now I wanna write my own version of *Facemash* to our work-party and use *webpack* and *react* together.

**What excites or interests you about coding?**

I feel myself a wizard or even a God =). If I want to make snowflakes fall bottom-upwards, I'll write a few lines of code and it will so.

**What is a recent technical challenge you experienced and how did you solve it?**

Now I'm trying to write some components library for our project. I think it should be based on React and Webpack. It allows us to make independent chunks of code, which can be easily include on any page or script.


**What UI, Security, Performance, SEO, Maintainability or Technology considerations do you make while building a web application or site?**

It's a hard question.

It depends from goals the project is going to deal with. If it is our inner project only for administrative purposes, then I will not think about SEO at all. Another way, if it public project and it has to collect a lot of traffic, SEO will be one of the main targets. I'll try to make server rendering, add correct meta-tags and so on. It is all based on project purposes.

In terms of UI, I mostly doing small POCs (proof of concepts), I try to keep things as simple as possible.

What about security I know that I can't trust anything given from the user. Most of security rules have to be written on server side, but I still should remember about XSS. XSS should have two main things: the place **from** attacker can input dangerous data and a place **where** this data will be written in a page.

In term of maintainability, it falls to basics. Proper documentation, clean code, source control, bug tracker.

**Talk about your preferred development environment.**

As for me I'm comfortable to work on my Mac. It's like Linux but with human face =). My favorite IDE is Webstorm from Jetbrains. Guys did a great work and their product is really smart. It has nice plugin system, theming and of course a lot of intelligence.

As task runner I prefer Gulp rather then Grunt. I don't like a huge configs, it's more easy to make deal with streams for me.

**Which version control systems are you familiar with?**

I worked with Subversion and Git. I didn't spend a lot of time with Subversion, we almost didn't use branches and tags. But with Git I'm working since this year and I'm using branches, tags, cherry-picks and so on. I have a few repos on Github =).

**Can you describe your workflow when you create a web page?**

- We have to deal with requirements.
- Then we must consider what components will be on the page.
- What logic and design this components should have.
- git init.
- npm init.
- Html and Css markup.
- Coding time.
- Testing time.
- Building time.
- Deploying;

**If you have 5 different stylesheets, how would you best integrate them into the site?**

For each page we have to concat and minify this files. But we also should make some inline *Critical CSS* that renders on first screen.

**Can you describe the difference between progressive enhancement and graceful degradation?**

PE - Embracing the future from the point of best practices.
GD - practice of building your web functionality so that it provides a certain level of user experience in more modern browsers, but it will also degrade gracefully to a lower level of user in experience in older browsers.

**How would you optimize a website's assets/resources?**

- Minify.
- Concat (sprites for icons or small images).
- Push it to the CDN's.

**How many resources will a browser download from a given domain at a time?**

It depends on browser: Chrome and FF - 6, IE - 8. I think 6 is a good average.

So the limits are per domain and in theory we can use CDN with wildcard \*.foo.com.

**Name 3 ways to decrease page load (perceived or actual load time).**

- Reduce requests count.
- Gzip all traffic.
- Use CDN.

**If you jumped on a project and they used tabs and you used spaces, what would you do?**

I'll use tabs =).

**Describe how you would create a simple slideshow page.**

It can be done in multiple ways. I can use JS to manipulate DOM and can use CSS. In CSS case I should use radio-buttons and labels.

**If you could master one technology this year, what would it be?**

React and Webpack. It seams a nice couple.

**Explain what ARIA and screenreaders are, and how to make a website accessible.**

ARIA-attributes allows incapacitated persons to use screenreaders. It parses a page and make from it logical structure with headers, footers, prompts and so on.
To make site accessible you should use semantic markup and ARIA-attributes.

**Explain some of the pros and cons for CSS animations versus JavaScript animations.**

Pros:
- GPU acceleration (for JS you should use `translate3d` to do the same)
- Calculations in different stream

Cons:
- Can't control state
- Performance (GSAP is better) 
- Limited effects
