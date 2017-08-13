# Module 1 Review Questions and Exercises

## Instructions

1. Click "edit" at the top of the page.
2. Fill in your answers below each question.
3. Save your changes and send a link to your mentor!

## HTML

### Questions

1. What is HTML and what is it used for? -Hypertext Markup Language.  It is used to create webpages featuring different sized headings, paragraphs, web forms, and other objects.  TLDR it is used to create Documents on the Web, as well as define the layout or structure.

2. What is the difference between an ID and a class?
The ID selector is used once to identify a specific element to be modified.  The class selector typically includes multiple elements and will allow for you to change or format that whole component.  TLDR ID is unique to a single element wheras Class covers many.

3. What does it mean to write "semantic" HTML?
To be semantic means that the HTML code is clean and organized, as well as makes sense.  This includes things such as Indentations with nesting, as well as using classes and ID's so that you can make more sense of what is going on.

### Exercises

1. Write a paragraph tag with a class of "highlight" and content "Watch out!".
<p class="highlight"> Watch out! </p>

2. Write an HTML image tag to show an image called `profile-picture.jpg`.
<img src="profile-picture.jpg" alt="Profile Picture" height="50px" width="50px">

3. Write a link tag that links to http://google.com.
<a href="http://google.com">Google</a>

5. Write an complete standard HTML document outline (including a DOCTYPE, and `<html>`, `<head>`, and `<body>` tags).

```
<!DOCTYPE HTML>
  <html>
    <head>
      <meta charset="UTF-8">
      <script src="main.js"></script>
      <link rel="stylesheet" type="text/css" href="main.css">
    </head>
  <body>
  </body>
  </html>
```

6. Inside of the code for the previous exercise, write the appropriate tag to link to a script file called `main.js`.
See #5
7. Inside of the code for the previous exercise, write the appropriate tag to link to a stylesheet file called `main.css`.
See #5

8. Write a numbered list in HTML and list three of your favorite books.
<ol>
  <li>Harry Potter Series</li>
  <li>Inheritance Series </li>
  <li>A world of Ice and Fire </li>
</ol>

9. Fix the indentation of the following HTML sample:

  ```html
  <div>
      <ul>
         <li>Item 1</li>
         <li>Item 2</li>
         <li>Item 3</li>
      </ul>
  </div>
  ```

## CSS

### Questions

1. What is CSS and what is it used for?
CSS stands for Cascading Style Sheets.  CSS is used to change the look and formatting of HTML pages.  This is done using items such as background colors, images, borders, page orientation, etc.  CSS is called Cascading style sheets because declarations made at the top will cascade down throughout the rest of the page for selected items, UNLESS changed further down.

2. What is the CSS box model?
The box model works as follows (from center working outward):
  -Content is the core - it is your center
  -Surrounding the content you have padding.
  -Surrounding padding you have your border.
  -Surrounding your border you have your margins.

3. What's the difference between margin and padding?
Padding creates space between the information inside of the content section and it's border, this can lead to a cleaner look where letters are no longer cut off by bordering for example.  Margin creates space between the border and OTHER content.  This allows the content to look cleaner by creating some space away from other items or the sides of pages.


### Exercises

1. Write a CSS rule to make the text of all `h1` tags red.
h1 {
    text-color:red;
   }

2. Write a CSS rule to make the background color of the link with `class="btn"` blue:
.btn a
    {
    color: blue;
    }
  ```html
  <a href="#" class="btn">Learn more</a>
  ```

3. Write a CSS rule to give the first paragraph in the following HTML a font size of `20px`, but not the second paragraph.

.jumbotron p
        {
        font-size:20px;
        }
  ```html
  <header class="jumbotron">
    <p>Hello, World!</p>
  </header>

  <p>Welcome to this awesome website!</p>
  ```

## JavaScript

### Questions

1. What is a function? What are they used for?
A function is a section of code that when combined, completes a task.  You can call functions after declared in order to complete a task.

2. What is the difference between `==` and `===`?
`==` will compare two items and try to make a conversion of type.  `===` compares two items and is STRICT, with no conversion.

3. What is the difference between global and local scope variables?
Global scope is for your entirety of your code.  Local scope is contained to within the function it is declared for.  Example:
```
x=0;

function dogTreat(){
                    x=1;
                    return;
                   }
The x=1 is a LOCAL variable.  The x=0 is a global.
```

4. What is a boolean value?
boolean logic returns a value of True OR False.

5. What is an array?
An array is a collection of slots which contain data i.e. Strings, Numbers, Boolean, which can be accessed beginning with slot 0 and going up to as many items as the array contains.


### Exercises

1. Write a line that declares a variable called `myName` and set its value to your name.
```var myname="Mark Strizalkouski";
```
```
2. Write a loop that logs the numbers 1 through 10 to the console.
for(var i=1;i<=10;i++){
console.log(i);
}
```
```
3. Translate the following pseudocode into JavaScript: if `score` is greater than `3` and `lives` is greater than `0`, alert "You win!".
if (score >3 && lives>0){
                          alert("You win!");
                        }
```
```
4. Write a function `sayHello` that takes one argument, a name, and logs "Hello, <name>!" to the console. Then, call the function below the function definition and pass in your name as the argument.

function sayHello(name){
                       console.log("Hello " + name + "!");
                       {
sayHello("Mark Strizalkouski");
```
5. What would the following script log to the console?

  ```javascript
  var currentSong = "Call Me Maybe";

  function setSong(song) {
    currentSong = song;
  }

  setSong("Friday, Friday");

  console.log(currentSong);
  ```
"Friday, Friday" would be output via console.log

6. What would the following script log to the console?

  ```javascript
  var add = function(a, b) {
    return a + b;
  }

  var result = add(3, 7);

  console.log(result);
  ```
"10" would be output by console.log

7. What would the following script log to the console?

  ```javascript
  var helloGoodbye = function(name) {
    return sayHello(name) + " " + sayGoodbye(name);
  }

  var sayHello = function(name) {
    return "Hello " + name " !";
  }

  var sayGoodbye = function(name) {
    return "Goodbye " + name " !";
  }

  console.log(helloGoodbye("Sarah"));
  ```
The output would be "Hello Sarah !" "Goodbye Sarah !"

8. Write a function `findLongestWord()` that takes an array of words and returns the length of the longest one.
```
function findLongestWord(word){
 var longest = 0;
  for(var i=0;i<word.length;i++){
    if (word[i].length > longest)
       {
        longest = word[i].length;
       }
      }
   return longest;
   }
```
9. Define a function `sum()` that sums all the numbers in an array of numbers. For example, `sum([1,2,3,4])` should return 10.
```

function sum (numbers)    {
var sum = 0;
        for(i=0;i<numbers.length;i++)
                  {
                  sum += numbers[i];
                  
                  }
           return sum;
                }
```
10. Write a function that takes a character (i.e. a string of length 1) and returns true if it is a vowel, false otherwise.
```
function vowel(char){
    return char.toLowercase().charAt(0)=="a" || char.toLowercase().charAt(0)=="e" || char.toLowercase().charAt(0)=="i" ||       char.toLowercase().charAt(0)=="o" || char.toLowercase().charAt(0)=="u";
                 }
```

11. Write the correct line to make `"Woof!"` show up in the console based on this script:

  ```javascript
  var pet = {
    name: "Charles",
    goodDog: true,
    speak: function() {
      console.log("Woof!");
  
    }
  };
  pet.speak();
  
  ```

12. Using the same script as above, write the correct line to log the dog's name to the console.
```
console.log(pet.name);
```

## Command Line

### Questions

1. What is the command line and what is it used for?
command line is a console which allows a user to manipulate things such as files and folders by way of commands.  It is a powerful tool which allows deep access to a user.

2. What does the command `ls` do?
ls lists all directories accessible at that moment in time

3. What does the command `pwd` do?
pwd shows you the file path leading up to your current directory

4. What does the following command do: `cd my-cool-project`
This command changes your directory to the "my-cool-project" folder

### Exercises

1. Write the command to make a new directory called "my-cool-project".
mkdir my-cool-project

2. Write the command to create a file called "index.html".
touch index.html

3. Write the command to delete a file called "main.css".
rm main.css

## Git

### Questions

1. What is Git and what is it used for?
Git is a version and source control.  It is used to control versioning as well as allow others to edit portions of a project in the real world.

2. What's the difference between a local repository and a remote repository?
A local repository is what is located on your local machine, i.e. your HDD.  A remote repository is essentially the HUB for the source code.  It can be pulled down by other uses and then recommitted to, whereas only you work on your local repository.  

### Exercises

1. Write the command that you would use to create a new local Git repository.
git init

2. Write the command to stage a file called `index.html` to be committed.
git add index.html

3. Write the command to view the current status of the git repository.
git status
