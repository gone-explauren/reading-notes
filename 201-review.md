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
  
## JavaScript Objects
* How would you describe an object to a non-technical friend?
An object in JS, like an object in the real world has features or properties that make it unique, like size and shape and color, etc.
  
* What are some advantages to creating object literals?
Object literals are good to use when you want to transfer data in a request to a server. It is more efficient to use object literals that sending several single items
  
* How do objects differ from arrays?
Objects store data using *key value pairs*

* Give an example for when you would need to use bracket notation to access an object’s property instead of dot notation.
Use bracket notation when property identifiers are a string or a var that is a string

* What is a constructor?
A constructor is a way to *initialize objects* which allows the object code to be reused. It doesn’t require changing object code for many instances of similar object.
  
* How does the term **this** differ when used in an object literal versus when used in a constructor?
**this** in an object literal refers to the specific features in that object. In a constructor, **this** can be used to refer back to an object and differintiate between it and other objects
  
### References:
* <https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Objects/Basics>
* <https://betterprogramming.pub/intermediate-javascript-whats-the-difference-between-primitive-values-and-object-references-e863d70677b>
* <https://ui.dev/beginners-guide-to-javascript-prototype>
  
## Intro to DOM
*What is the DOM?
DOM = Document Object Model. Allows programs to change doc structure, style, content, etc.

* Briefly describe the relationship between the DOM and JavaScript.
We are able to access and manipulate the DOM using JavaScript
  
* Explain why we need domain modeling.
Domain modeling allows us a better understanding of functionality
  
### References:
* <https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model/Introduction>
* <https://github.com/codefellows/domain_modeling#domain-modeling>
  
## HTML Tables  
* <tr> is table row, <th> is table header, <td> is table cell, and together these are used to crate the <table>
  
* Why should tables NOT be used for page layouts?
ables should not be used for page layouts because they are not accessible, webpages take longer to load, presentation data and content are mixed which makes redesigns of the site really difficult

### References:
* <https://developer.mozilla.org/en-US/docs/Learn/HTML/Tables/Basics>
  
## CSS - Flexbox
* Flexbox is designed for one-dimensional content. Explain what this means.
One dimensional content means that contents with different sizes can be laid out in the code, and flexbox will fit them to the best layout for the page
  
* Explain the difference between the main axis and cross axis.
*Main axis* can be either row or column. *Cross axis* is ***perpendicular*** to the main axis
  
* How can using certain properties of flexbox negatively impact accessibility?
Row and column reverse can chance the order of things you laid out in the html, which can negatively affect accessibility
  
* What are some advantages of using flexbox over float?
With flexbox, all child elements of a parent have an equal amount of height and width available to them even if they have different amount of content, whereas float allocates based on amount of content which doesn’t always look the best.
  
### References: 
* <https://web.dev/learn/css/flexbox/>
* <https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Flexbox>
* <https://web.dev/learn/css/layout/>
  
## HTML Forms
* List 5 form elements and explain their importance.
  * label : important for identifying what an input is looking for
  * fieldset: for creating groups of widget that share the same purpose
  * legend: for labeling a fieldset that formally describes the purpose of the fieldset
  * input: what actually takes in the value you want from the user
  * select: defines a drop-down list
  
### References:
* <https://developer.mozilla.org/en-US/docs/Learn/Forms>
* <https://developer.mozilla.org/en-US/docs/Learn/Forms/Your_first_form>
* <https://developer.mozilla.org/en-US/docs/Learn/Forms/How_to_structure_a_web_form>
  
## JavaScript Events
* How would you describe events to a non-technical friend?
An event is something that happens on a when you perform certain actions on a webpage (ie click, hover, etc)
  
* When using the addEventListener() method, what 2 arguments will you need to provide?
  * the name of the event 
  * a function to handle the event  
  
* Describe the event object. Why is the target within the event object useful?
The *event object* is the parameter specified with a name. The target is useful because it is a reference to the element the event occured on
  
* What is the difference between event bubbling and event capturing?
*Bubbling* describes how the browser handles events targeted at nested elements, and *capturing* is like bubbling, but it starts the event firing on the least nested element
  
### References:
* <https://developer.mozilla.org/en-US/docs/Learn/JavaScript>
* <https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Building_blocks/Events>
  
## Debugging
* Name some key differences between a Syntax Error and a Logic Error.
  * syntax: usually a spelling error or a typo. syntax errors will also usually be indicated by a red line generated in your ide or text editor
  * logic: the code is syntatically fine but it is not performing what you want it to perform. Usually no indicators are given when there is a logic error
  
* How would you describe the JavaScript Debugger tool and how it works to someone just starting out in software development?
iIt is a problem solving tool that allows you to stop your code at specific points to check values of variables and what is happening at specific points in your code 
  
* Define what a breakpoint is.
A break point is a place in the code that you want to stop the code running
  
* What is the call stack?
The call stack shows you *what code was executed to get to the current line.*
  
### References:
* <https://developer.mozilla.org/en-US/docs/Learn/JavaScript/First_steps/What_went_wrong>
* <https://developer.mozilla.org/en-US/docs/Learn/Common_questions/Tools_and_setup/What_are_browser_developer_tools#the_javascript_debugger>
* <https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/Debugging_HTML>
* <https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Debugging_CSS>
  
## Embedding Audio and Video
* Describe the use of the src and controls attributes in the <video> element.
**src** is the path to the video you're wanting to embed, and **controls** allow users to control video and audio playback.
   
* Why is it important to have fallback content inside the <video> element?
Not all browsers support access to the video element, so fallback content could be a link to the source of the video so the user can access it. 
  
### References:
* <https://developer.mozilla.org/en-US/docs/Learn/HTML/Multimedia_and_embedding/Video_and_audio_content>
* <https://developer.mozilla.org/en-US/docs/Learn/HTML/Multimedia_and_embedding/Other_embedding_technologies>
  
## CSS Grid
* How does Grid layout differ from Flex?
Flex was designed to be one dimensional, but *grid is a 2d layout*

* Grid container, grid item, and grid line are a few important terms to understand when using Grid. Please describe these terms in a few sentences.
  * grid container: a grid layout with rows and columns
  * grid item: child element of the container 
  * grid line: the lines that make the boxes out of the rows and columns 
  
### References:
* <https://css-tricks.com/snippets/css/complete-guide-grid/>

## Responsive Images
* Besides making a site visually appealing across different screen sizes, why should developers make images responsive?
Responsive images save bandwidth by not downloading huge images on page load

* **srcset** allows the browser to choose from a specified set of images of different sizes.  
* Sizes are separated by a comma.

* How is srcset more helpful for responsive images than CSS or JavaScript?
If there is a set of images to choose from (in srcset), there is another image to fallback on if the first choice doesnt work for whatever reason.

### References:
* <https://developer.mozilla.org/en-US/docs/Learn/HTML/Multimedia_and_embedding/Responsive_images>
  
## Canvas
* What does the <canvas> allow a developer to acheive?
<canvas> allows the dev to create 2d graphics in JavaScript
  
* What is the importance of the closing </canvas> tag?
The content between the opening a closing <canvas> tags is fallback content that give the browser other display option if it can’t display the chosen graphic

*Explain what the getContext() method does.
getContext() checks that the browser is compatible with canvas and 2d drawing. If it is not, then the fallback content gets displayed 
  
### References:
* <https://www.javascripttutorial.net/web-apis/javascript-canvas/>
* <https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Drawing_shapes>
* <https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Applying_styles_and_colors>
* <https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Drawing_text>
  
## Chart.js
* What is Chart.js and how it can be brought into your project?
Chart.js gives you the option of using a number of chart types, customizations, and plugins. Do use it, you need to install the chart.js plugin for JavaScript.
  
* List 3 different Chart types you can create using Chart.js.
  * scatter plot, 
  * pie chart, 
  * bar graph

* What are some advantages to displaying data via a chart over a table?
Charts are easier for users to look at and interpret data than tables are. Charts are more visually appealing to users and more customizable, so colors and animations can easily be added 
  
### References:
* <https://www.chartjs.org/docs/latest/> 
* <https://www.webdesignerdepot.com/2013/11/easily-create-stunning-animated-charts-with-chart-js/>
  
## Local Storage
* Why would a developer use local storage for a web application?
Local storage allows you to store the users' data so they can return to the most recent setting without having them forced to sign up for an account. 
  
* What information should not be stored in local storage?
Objects can’t properly be stored in local storage but there is a way to get around this… 
  
* Local storage can store what type of data? How would you convert it to that type before storing?
Local storage can store strings, so in order to properly store objects in Local storage, you have to use JSON.stringify() and JSON.parse()   
  
### References:
* <https://www.smashingmagazine.com/2010/10/local-storage-and-how-to-use-it/>   
* <http://diveinto.html5doctor.com/storage.html>
  
## CSS Animations and Transformations
* What does a CSS transform allow the developer to do to an element?
CSS transform allows the developer to distort a 2D element 

* What does a CSS transition allow the developer to do to an element?
CSS transition allows the developer to alter the appearance or behavior of an element when it’s hovered over or clicked, etc.  
  
* How does a CSS animation differ from a CSS transition?
The difference between CSS transition and Animation is the key frames used to make changes to an element over time in animation

* What are some benefits to using CSS transitions on websites?
Using transitions on a website make it more dynamic and fun for user to interact with 
    
### References:
* <https://learn.shayhowe.com/advanced-html-css/css-transforms/>  
* <https://learn.shayhowe.com/advanced-html-css/transitions-animations/>  
* <https://www.webdesignerdepot.com/2014/05/8-simple-css3-transitions-that-will-wow-your-users>  
* <https://codepen.io/dp_lewis/pen/QWMxRR>  
* <https://codepen.io/retyui/pen/ByoaXV>  
* <https://codepen.io/akshaychauhan/pen/dyBqVo>  
