# Module 2 Review Questions and Exercises

## Instructions

1. Click "edit" at the top of the page.
2. Fill in your answers below each question.
3. Save your changes and send a link to your mentor!

*Note: any topics from the first assessment should be reviewed in addition to the questions below!*

## CSS

### Questions

1. What is the box model?  
The CSS box model is essentially a box that wraps around every HTML element. It consists of: margins, borders, padding, and the actual content.
2. What is the difference between block and inline elements?
Basically, an inline element does not cause a line break (start on a new line) and does not take up the full width of a page, only the space bounded by its opening and closing tag. It is usually used within other HTML elements.  A block-level element always starts on a new line and takes up the full width of a page, from left to right. A block-level element can take up one line or multiple lines and has a line break before and after the element.
3. What is responsive design?
Responsive design ensures that your page will look good regardless of device or screen size.  This means hiding elements, resizing elements, or moving elements around based on screen sizes.
4. Which selector is more specific, a tag selector or class selector?
A class selector is more specific because you add a class to an existing tag.
5. What does `box-sizing` do?
The box-sizing property defines how the width and height of an element are calculated: should they include padding and borders, or not.
6. What's the difference between `relative` and `absolute` positioning?
Relative. This type of positioning is probably the most confusing and misused. What it really means is "relative to itself". If you set position: relative; on an element but no other positioning attributes (top, left, bottom or right), it will no effect on it's positioning at all, it will be exactly as it would be if you left it as position: static; But if you do give it some other positioning attribute, say, top: 10px;, it will shift its position 10 pixels down from where it would normally be.  Absolute. This is a very powerful type of positioning that allows you to literally place any page element exactly where you want it. You use the positioning attributes top, left, bottom. and right to set the location. Remember that these values will be relative to the next parent element with relative (or absolute) positioning. If there is no such parent, it will default all the way back up to the <html> element itself meaning it will be placed relatively to the page itself.

### Exercises

1. Write a CSS rule to turn the background color of the link with the `.btn` class blue on hover:

  ```html
  <a href="#" class="btn">Learn more</a>
  ```
  .btn:hover {
              color: blue;
              }

2. Write a CSS rule to give the `.container` a maximum width of `980px` when the browser window is wider than `1200px`:

  ```html
  <div class="container">
    <h1>I'm a heading!</h1>
  </div>
  ```
  @media (min-width: 1200px)
  .container {
             max-width: 980px;
             }

3. Which text would be red in the following example?

  ```html
  <style>
    section p:last-child {
      color: red;
    }
  </style>

  <section>
    <p>First paragraph</p>
    <p>Second paragraph</p>
    <p>Third paragraph</p>- red
  </section>
  <section>
    <p>First paragraph</p>
    <p>Second paragraph</p>
    <p>Third paragraph</p> -red
  </section>
  ```

4. Open this [JSBin](http://jsbin.com/qigiwuhepe/1/edit?html,css,output). Write a CSS rule using floats to make the HTML sample into a four column layout. Paste your udpated link below.
http://jsbin.com/wegoyegisi/edit?html,css,output

## JavaScript

### Questions

1. What is a callback?
A callback is a function that is used inside of another function.  This function gets used as a parameter within said function and executes inside of that.

### Exercises

1. Write a function `filterLongWords()` that takes an array of words and an integer `num` and returns the array of words that are longer than `num`.

2. Write a function `charFreq()` that takes a string and builds a frequency listing of the characters contained in it. Represent the frequency listing as a Javascript object. Try it with something like `charFreq("abbabcbdbabdbdbabababcbcbab")`.

## DOM Scripting

### Questions

1. What does DOM stand for and what is it?
Document Object Model and the DOM is used to access the Document and its Objects.

### Exercises

1. Write a JavaScript statement that finds the element with the ID, `next`, and saves it to a variable called `nextButton`:

  ```html
  <a href="#" id="next" class="btn">Next</a>
  ```

2. Write another line that updates the text of `nextButton` to `"Next image"`.
3. Write another line that adds a click event listener to `nextButton` so that when it's clicked the browser alerts `"Next image coming up."`.

## jQuery

### Questions

1. What is a JavaScript library and why do we use them?
A Javascript library is a bunch of tools that we can use within Javascript to add other layers of functionality.  We need to state that we are using a library to let the program or webpage know that we will be utilizing tools from there.
2. What is jQuery for?
jQuery is used for Document Object Model manipulation.

### Exercises

1. Write a statement to select all elements with the `.btn` class using a jQuery selector and save them to a variable called `buttons`:

  ```html
  <a href="#" id="next" class="btn">Next</a>
  <a href="#" id="beginning" class="btn">Beginning</a>
  <a href="#" id="previous" class="btn">Previous</a>
  ```

2. Write another line that adds a click event to the buttons that logs `'click'` to the console when the button is clicked. Use the jQuery syntax.

## Angular

### Questions

1. How is a framework different than a library?
A library, such as jQuery, is a collection of prewritten code consisting of common tasks that simplify development. Our code is "in charge" and uses a library to retrieve specific functions from the collection.  A framework, like Angular, provides the basic structure of an application. The framework is "in charge" and our code fills in the details.
2. What is a controller?
Controllers contain the business logic that applies functions and values to scope.  It is a javascript object created to modularize the code and break it into specific functionality or jobs.
3. What is a view?
A view is what the user will see when a specific thing is happening.  There is a default view, and other views are called into place when actions occur.  Views make for a smooth webpage as it's not always a complete page reload, it's just the specific "view" reloading.
4. What is a single page application?
A single page application is a page that does not need to switch pages when events happen.  Instead, new views are populated and presented when the actions occur.
5. What is a directive in Angular?
A directive binds angular activity to the HTML.  For example ngRepeat will repeat the instances that are present.  ngClick indicates to do something when the HTML is clicked.
## Git

### Exercises

1. Write a command to create a new branch called `bug-fix`.
git checkout -b "bug-fix"
2. If you're on the `master` branch, write a command to merge a branch called `bug-fix` into the `master` branch.
git merge "bug-fix"
