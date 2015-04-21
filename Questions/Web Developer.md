# Web Developer questions

## General

* Name 3 ways to decrease page load (perceived or actual load time).
* How would you optimize a website's assets/resources?
* Can you describe the difference between progressive enhancement and graceful degradation?
* If you have 5 different stylesheets, how would you best integrate them into the site?
* What tools do you use to test your code's performance?
* How many resources will a browser download from a given domain at a time?
    * What are the exceptions?

* Describe how you would create a simple slideshow page.
* What is Flash of Unstyled Content? How do you avoid FOUC?
* Explain what ARIA and screenreaders are, and how to make a website accessible.

* What kind of things must you be wary of when design or developing for multilingual sites?
* Explain the importance of standards and standards bodies.

* If you could master one technology this year, what would it be?

## HTML

* What does a doctype do?
* What's the difference between standards mode and quirks mode?
* What's the difference between HTML and XHTML?
* Are there any problems with serving pages as application/xhtml+xml?

* Why is it generally a good idea to position CSS `<link>`s between `<head></head>` and JS `<script>`s just before `</body>`? 
   * Do you know any exceptions?

* What is progressive rendering?
* Describe the difference between a cookie, sessionStorage and localStorage.
* Describe the difference between `<script>`, `<script async>` and `<script defer>`.

* How do you serve a page with content in multiple languages?

* What are data- attributes good for?
* Consider HTML5 as an open web platform. What are the building blocks of HTML5?
* What are some new HTML5 markup elements?
* What are web workers and why do we need them ?
* How can we add and remove data from local storage?
* What is the lifetime of local storage?
* What is the difference between local storage and cookies?
* What is difference between session storage and local storage?

## CSS

* What is the difference between classes and ID's in CSS?
* What's the difference between "resetting" and "normalizing" CSS? Which would you choose, and why?
* Describe Floats and how they work.
* Describe z-index and how stacking context is formed.
* What are the various clearing techniques and which is appropriate for what context?
* Explain CSS sprites, and how you would implement them on a page or site.
* What are your favourite image replacement techniques and which do you use when?
* How would you approach fixing browser-specific styling issues?
* Explain some of the pros and cons for CSS animations versus JavaScript animations.

* How do you serve your pages for feature-constrained browsers?
* What techniques/processes do you use?

* What are the different ways to visually hide content (and make it available only for screen readers)?
* Have you ever used a grid system, and if so, what do you prefer?
* Have you used or implemented media queries or mobile specific layouts/CSS?
* Any familiarity with styling SVG?
* How do you optimize your webpages for print?
* What are some of the "gotchas" for writing efficient CSS?

* What are the advantages/disadvantages of using CSS preprocessors?
* Describe what you like and dislike about the CSS preprocessors you have used.

* How would you implement a web design comp that uses non-standard fonts?
* Explain how a browser determines what elements match a CSS selector.
* Explain your understanding of the box model and how you would tell the browser in CSS to render your layout in different box models.
* What does `* { box-sizing: border-box; }` do? What are its advantages?
* List as many values for the display property that you can remember.
* What's the difference between inline and inline-block?
* What's the difference between a relative, fixed, absolute and statically positioned element?
* The 'C' in CSS stands for Cascading. How is priority determined in assigning styles (a few examples)? How can you use this system to your advantage?
* What existing CSS frameworks have you used locally, or in production? How would you change/improve them?
* Have you played around with the new CSS Flexbox or Grid specs?
* How is responsive design different from adaptive design?
* Have you ever worked with retina graphics? If so, when and what techniques did you use?
* Is there any reason you'd want to use translate() instead of absolute positioning, or vice-versa? And why?

## Javascript

* Explain event delegation
* Explain how this works in JavaScript
* Explain how prototypal inheritance works
* How do you go about testing your JavaScript?
* What do you think of AMD vs CommonJS?

* Explain why the following doesn't work as an IIFE: 

```
function foo(){ }();.
```

* What needs to be changed to properly make it an IIFE?

* What's the difference between a variable that is: `null`, `undefined` or undeclared?
* How would you go about checking for any of these states?

* What is a closure, and how/why would you use one?
* What's a typical use case for anonymous functions?
* How do you organize your code? (module pattern, classical inheritance?)
* What's the difference between host objects and native objects?
* Difference between: 

```
function Person(){}
```

```
var person = Person()
```

```
var person = new Person()
```

* What's the difference between `.call` and `.apply`?
* Explain `Function.prototype.bind`.
* When would you use document.write()?
* What's the difference between feature detection, feature inference, and using the UA string?
* Explain AJAX in as much detail as possible.
* Explain how JSONP works (and how it's not really AJAX).

* Have you ever used JavaScript templating?
* If so, what libraries have you used?

* Explain "hoisting".
* Describe event bubbling.
* What's the difference between an "attribute" and a "property"?
* Why is extending built in JavaScript objects not a good idea?
* Difference between document load event and document ready event?
* What is the difference between == and ===?
* Explain the same-origin policy with regards to JavaScript.

* Why is it called a Ternary expression, what does the word "Ternary" indicate?
* What is "use strict";? what are the advantages and disadvantages to using it?
* Create a for loop that iterates up to 100 while outputting "fizz" at multiples of 3, "buzz" at multiples of 5 and "fizzbuzz" at multiples of 3 and 5
* Why is it, in general, a good idea to leave the global scope of a website as-is and never touch it?
* Why would you use something like the load event? Does this event have disadvantages? Do you know any alternatives, and why would you use those?
* Explain what a single page app is and how to make one SEO-friendly.
* What is the extent of your experience with Promises and/or their polyfills?

## Network

* What are the different HTTP verbs and how do they differ?

* Traditionally, why has it been better to serve site assets from multiple domains?
* Do your best to describe the process from the time you type in a website's URL to it finishing loading on your screen.
* What are the differences between Long-Polling, Websockets and Server-Sent Events?

Explain the difference between the following:
   * Expires
   * Date
   * Age
   * If-Modified-

Explain the following request and response headers:
   * Do Not Track
   * Cache-Control
   * Transfer-Encoding
   * ETag
   * X-Frame-Options
 

