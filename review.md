# 201 Review

## Intro to HTML and JavaScript

* Describe how HTML, CSS, and JS files are “parsed” in the browser.
As the browser parses the HTML, it sends requests back to the server for any CSS files it has found from <link> elements, and any JavaScript files it has found from <script> elements, and from those, then parses the CSS and JavaScript.
In layers! First, the HTML is read and loaded by the browser, ensuring that at least this basic human readable site can load. Next, CSS rules are applied, either from within the style tag of the HTML page or a linked CSS sheet. Finally, JavaScript script is loaded much the same way, running from the script tag or from an external .js file.
  
* How can you find images to add to a Website?
A google image search with the Creative Commons License filter set will work, though there are many open source image sites like Unsplash available too.
  
* What is JavaScript?
A programming language that adds dynamic functionality to websites and applications
  
* How do you create a String vs a Number in JavaScript?
In quotes! Numbers count as numbers outside of quotes, where they work like any other string. Strings get concatenated if you try and to arithmetic on them in JavaScript.
To make a string, enclose it with quotes "string"
No quotes is a number
  
* What is a Variable and why are they important in JavaScript?
a variable is a container that stores values
the contents of the container are stored in the machine’s memory and can be retrieved later by function calls
the value of the variable can be assigned and then changed later
  
* What is an HTML attribute?
HTML attributes are modifiers to HTML tags that give them more specific functions, like sizing an image or coloring text. They’re added inside the tag in the form of <tag attribute= ></tag>.

* What is the Difference between article and section element tags?
<section> is used for separating parts of a page by function
<article> is used for separating bits of independently meaningful content
however an <article> can be divided into <section> (s) or a <section> can include multiple <article> (s)  
  
* How does metadata influence Search Engine Optimization?
One way is by having the description of the site include keywords relating to the content. When users search for those keywords, your site will appear higher on the list.
The information in the metadata is used when displaying search engine results as the page “title” and “content”
however there are additional unused elements of the <meta> tag that are no longer used by search engines because of bad website/creator behavior
  
* How is the meta HTML tag used when specifying metadata? 
The meta tag can include multiple attributes like name and content that can give more specificity to the site authorship and purpose.
the <meta> tag can be used to define the author, describe the content, and specify the character set of the page
  
* Why should you use an h1 element over a span element to display a top level heading?
The functionality of a top level heading is built into h1, and a browser is smart enough to render the content of a h1 to appear as such even before applying any CSS rules. Any of that could be accomplished with span, but you’d have to do it manually and why bother when you could rely on the browser to give you the same functionality more easily?
  
* What are the benefits of using semantic tags in our HTML? 
Automatic application of styling rules in a easy and consistent way, and a ‘content agnostic’ approach is more clear to read and maintain.
  
### References
  
* <https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/How_the_Web_works>
* <https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/What_will_your_website_look_like>
* <https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/JavaScript_basics>
  
  
## Basics of HTML, CSS & JS
  
* Why is it important to use semantic elements in our HTML?
It's important that your code is clear to read and understand is essential for clean and condense code.  
  
* When using the <abbr> element, what attribute must be added to provide the full expansion of the term?
When using abbr, you should use the full expansion of the abbriviated term as an attribute to keep the meaning clear for future users of the code. 
  
* What are ways we can apply CSS to our HTML?
Inline, internal and external stylesheets
  
* Why should we avoid using inline styles?
Its inefficent for maintenance. It makes it more difficult to read in the html
  
* List 4 types of Javascript operators
arithmetic, assignment, comparison and logical
  
### References
  
* <https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML>
* <https://developer.mozilla.org/en-US/docs/Learn/CSS/First_steps/How_CSS_is_structured>
* <https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/JavaScript_basics>
  
  
## HTML Lists
  
* When should you use an ordered list vs an unorder list in your HTML document?
Use an ordered list if you need something listed in steps or with hierarchy, otherwise you can use an unordered list
  
* How do you change the bullet style of unordered list items?
Alter the list-style property
  
### References
  
* <https://developer.mozilla.org/en-US/docs/Web/HTML>
  
  
## CSS Box Model
  
* List and describe the four parts of an HTML elements box as referred to by the box model
margin - the outermost layer wrapping the content.
padding - sits around the content as white space
border - wraps the content and any padding
content - the area where your content is displayed
  
### References
  
* <https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/The_box_model>
  
  
## Arrays, Operators and Expressions, Conditionals, and Loops
  
* What data types can you store inside of an Array?
numbers, strings, boolean, characters, objects
  
* List five shorthand operators for assignment in javascript and describe what they do.
1. = this is just assigning a variable to a vallue
2. += this is adding directly to variable instead of reassigning and adding to it
3. -= this is doing the same as above but subtracting instead
4. %= this assigns the remainder
5. /= this is the same as above but with division

### References

* <https://developer.mozilla.org/en-US/docs/Learn/JavaScript/First_steps/Arrays>
* <https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Expressions_and_Operators>
* <https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Building_blocks/conditionals>
* <https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Building_blocks/Looping_code>
  
  
## HTML Links
  
* The href attribute contains what information?
href specifies the URL the link goes to. If the href attribute is not present, the <a> tag will not be a hyperlink.
  
* What are some ways we can ensure links on our pages are accessible to all readers?
Links can be made accessible by describing your link clearly, not using the URL for the link text.
Use concise and meaningful text for links.
Do not capitalize all letters in links.
Avoid using URLs for link text.
Do not use the word "link" as part of the link text.
Do not use tooltips/screentips to add additional information.
  
### References
  
* <https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/Creating_hyperlinks>
  

## CSS Layout
  
* What is meant by “normal flow”?
Normal flow is the way that Block and Inline elements are displayed on a page before any changes are made to their layout.

* What are a few differences between block-level and inline elements?
Block elements always start from a new line. Inline elements never start from a new line. Block elements cover space from left to right as far as it can go. Inline elements only cover the space as bounded by the tags in the HTML element.
block: starts on a new line, takes up all the space available. inline: flows around other content, takes up as much space as it needs
  
* *Static positioning* is the default for every html element.
  
* What is a key difference between fixed positioning and absolute positioning?
absolute positioning fixes an element in place relative to its nearest positioned ancestor
fixed positioning usually fixes an element in place relative to the visible portion of the viewport.

### References
  
* <https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Normal_Flow>
* <https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Positioning>
* <https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Colors/Applying_color>
* <https://developer.mozilla.org/en-US/docs/Learn/CSS/Styling_text/Fundamentals>
  
  
## JS Functions
  
* Describe the difference between a function declaration and a function invocation.
declaration: declares creation of all functions and variables in JS. invocation: executes code 
  
* What is the difference between a parameter and an argument?
parameter: the name listed in the definition of the function. argument: values passed to the function
  
### References
  
* <https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Building_blocks/Functions>
  
  
## HTML Media
  
* Provide an example of when the figure element would be useful in an HTML document.
A figure element is self-contained and can be moved away from the main flow of the document
  
* Describe the difference between a gif image and an svg image.
Dimensions of a gif are fixed and the gif will pixilate if you zoom in or change the dimensions, but this doesn't happen with a svg. An svg would be good to use for an image or picture that you may not know the size and it can scale up smoothly

  
 ### References
  
* <https://developer.mozilla.org/en-US/docs/Learn/HTML/Multimedia_and_embedding>
* <https://developer.mozilla.org/en-US/docs/Learn/HTML/Multimedia_and_embedding/Images_in_HTML>
* <https://developer.mozilla.org/en-US/docs/Web/Media/Formats/Image_types>
* <https://developer.mozilla.org/en-US/docs/Web/Media/Formats/Image_types#choosing_an_image_format>
  

## Start Week 2...
  
