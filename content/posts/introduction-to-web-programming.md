# Introduction to Web Programming

## Goals

Throughout this course students will build a website from scratch using standard web frameworks including HTML, CSS, and Javascript. To create content for their website students will add text, images, and other assets though HTML and an interactive program (e.g. a game, drawing program, weather forecaster, neural network bot) using the P5.js Javascript framework.

## Tools

- A text editor (e.g. Atom) and a web browser or a Glitch.com account (recommended)
- A downloaded version of the P5.js Javascript library or a P5.js editor account (recommended)

## Chapter One

### The structure of a webpage
In its most basic form a website is just a folder with an index.html file, a styles.css file and a script.js file.

The `index.html` file contains all of the __content__ of a website - the words, pictures, links, and basic formatting. It is written in Hypertext Markup Language (HTML) which consists of tags that allow a web browser (like Google Chrome or Safari) to interpret the words you write as specific elements on a web page (like links, buttons, and input forms).

The `styles.css` (Cascading Style Sheet) file is where you define the __appearance__ of your website like what colors the background and text should be, where elements should be positioned on the page, and how the webpage should react to different screen sizes (for example, you would typically like your website to look different when viewed on a smartphone than when it is viewed on a laptop).

The `script.js` file is where you can add more __interactivity__ and complex animations to your website. It is written in the Javascript programming language which gives you the ability to add powerful features to your website. Almost all web games (like slither.io) and web applications (like google drive) are created using Javascript.

To bring this all together: if, for example, you would like to create a website that display images of your artwork you could add a list of images to your `index.html` file then resize and arrange the images in a grid in your `styles.css` file and, finally, using your `script.js` file you could add an animation to zoom in and center each image when its clicked on.

## Chapter Two
### Creating a basic webpage

Create a folder on your computer and name it `my-website`. Inside of this folder create a file named `index.html`.

Your `index.html` file is the centerpiece of your website. It is where you link your `styles.css` and `script.js` files together with the main content of your website.

The `index.html` file contains two main sections: the __head__ where we store metadata about our website like it’s title and the location of our .css and .js files and the __body__ where all of the website’s main content lives (the text, images, buttons, navigation bars, etc.)

To get started open your blank `index.html` file and type

``` html
<html>

	<head>

	</head>

	<body>

	</body>

</html>
```

You will notice that each tag (`<html>`) has a corresponding closing tag with a backslash at the beginning (`</html>`). This is important to remember as that is how your web browser will know where one tag ends and another starts.

If you save this file and drag it into your browser you will see a blank webpage. You can keep this page open and any changes you make to your `index.html` file will automatically appear as soon as you refresh the page.

Now lets add a couple more elements to our index.html file

``` html
<html>

	<head>
		<title>My new website</title>
	</head>

	<body>
		<h1>Welcome to my website!</h1>
	</body>

</html>
```

You should notice that the text that you added to the body of your file showed up on the webpage! We put this text inside of `<h1>` tags. The `<h1>` tag is the largest of the heading tags but there are also `<h2>`, `<h3>`, `<h4>`, `<h5>`, and `<h6>` tags which all decrease in size as the numbers get larger. These tags should be used to create titles and other important text on your webpage. 

You might have also noticed that the browser tab your website is opened in now displays “My new website”. You can change this by changing the text inside of the `<title>` tags.

## Chapter Three
### Make it stylish

Now that you have a simple website started lets add a `styles.css` file so that we can start tweaking the design of the site.

In your `my-website` folder create a new blank file named `styles.css` and open it up in your text editor.

To tweak the design of a specific element of your web page using CSS you can select it using the tag name without angle brackets ( < > ).

``` CSS
body {
	background-color: black;
	color: white; 
}

h1 {
	color: green;
}
```

Here we are making the background color of the entire web page black, setting the default text color to white and setting the text color of `<h1>` tags to green. Feel free to experiment and change these colors to anything you like.

The attributes that you would like to apply to each element should be placed between an opening and closing curly bracket ( { } ) and each line should end with a semicolon ( ; ).


CSS has a bunch of built in properties aside from color and background-color that we will cover later on but for now save your `styles.css` file and open your `index.html` file again.


Before we can see these colors on our web page we need to link this `styles.css` file to our `index.html` file from earlier by adding a new line telling the HTML file where it can find our CSS file. 

```html
<html>

	<head>
  	<link href="styles.css" rel="stylesheet" type="text/css">
		<title>My new website</title>
	</head>

	<body>
		<h1>Welcome to my website!</h1>
	</body>

</html>

```

Once you’ve added this new line save the file and refresh your web page in the browser. You should see that your website has updated to use your new color scheme!

## Chapter Four

### Give it some class


At this point you have your own website that uses the `<h1>` HTML tag for a page title but what if you want to add more?


Let's add two new lines to our HTML file. This time we’ll use the `<p>` (paragraph) tag. The paragraph tag is the standard tag for most text on a website. In general, all text other than titles and subtitles should be placed inside of a `<p>` tag.

```html
<html>

	<head>
  	<link href="styles.css" rel="stylesheet" type="text/css">
		<title>My new website</title>
	</head>

	<body>
  	<h1>Welcome to my website!</h1>
    <p class="warning">Warning: this page is under construction!</p>
   	<p>This is where you can write about all of your favorite things</p>
	</body>

</html>
	
```

You will notice that we’ve added something else new to one of these paragraph tags - a __class__. All HTML elements can be given a class attribute. On its own a class won’t do anything special but it allows us to target a specific section of our web page in CSS so that we can style it differently than other elements that are using the same tag.


Save your `index.html` file and open up your `styles.css` file.


To target a specific class in CSS write the class name with a period ( . ) in front of it. Then you can apply styles to it the same way you would for a tag.

```css
body {
	background-color: black;
  color: white; 
}

h1 {
	color: green;
}

.warning {
	background-color: red;
  color: white;
  border: 1px solid yellow;
}	
```

While we have the `styles.css` file open we can add a few more CSS attributes to make our page look a bit more modern.

```css
body {
	background-color: black;
  color: white;
  margin-left: 10%;
  margin-right: 10%;
  margin-top: 2%;
  margin-bottom: 2%;
}

h1 {
	color: green;
  text-align: center;
}

.warning {
	background-color: red;
  color: white;
  border: 1px solid yellow;
  text-align: center;
  padding: 1%;
}
```

The `margin` attributes add __space between__ HTML elements and the edges of the web page. Moving web page content away from the far edges of the screen typically makes your site easier to read. The `text-align` attribute can be set to either left, right, or center and this determines where __text is placed__ on the web page. Lastly, the `padding` attribute is very similar to margin except that this adds __space inside__ of an HTML element. In this case this makes the background section of our warning element larger.


Save your files and refresh your web page to see all of the changes!

## Chapter Five
### Hypertext


The H in HTML stands for hypertext (dynamic, interactive text). This is one of the most important innovations of the internet - it's what sets a web page apart from a book! Let's take advantage of this feature and add some links and images to our website.


To add a link to our web page we can use the `<a>` tag. The `<a>` tag takes an `href` attribute where you can specify the URL you would like to attach. Any text that you add before the closing `</a>` tag will turn into a hyperlinked text. Try adding this new line to your index.html file.

```html
<html>

	<head>
		<link href="styles.css" rel="stylesheet" type="text/css">
		<title>My new website</title>
	</head>

  <body>
		<h1>Welcome to my website!</h1>
		<p class="warning">Warning: this page is under construction!</p>
  	<p>This is where you can write about all of your favorite things</p>
  	<p>Click <a href="https://bitspacechicago.com">here</a> to visit my favorite website</p>
	</body>

</html>
```

To add an image to your website first create a new folder named images inside of your `my-website` folder. Any image that you would like to add to your website should be downloaded and placed in this folder. Once you’ve found an image you like you can add it to your website using the `<img>` tag.

_Note: make sure your image’s filename doesn’t contain a space. If it does, web browsers will not be able to load your image correctly._

```html
<html>

	<head>
  	<link href="styles.css" rel="stylesheet" type="text/css">
		<title>My new website</title>
  </head>

	<body>
  	<h1>Welcome to my website!</h1>
    <p class="warning">Warning: this page is under construction!</p>
   	<p>This is where you can write about all of your favorite things</p>
    <p>Click <a href="https://bitspacechicago.com">here</a> to visit my favorite website</p>
   	<img src="images/grumpy-cat.jpg" alt="a picture of a frowning cat">
	</body>

</html>
```

The `<img>` tag takes two attributes. The first is `src` which is the location of your image in relation to your `index.html` file. The second attribute is `alt` which is a description of your image that will be shown in the event your image can’t be loaded. The alt attribute also allows those that are blind or that have impared vision to effectively navigate your website using a screen reader!

To wrap things up let’s add a new section to our `styles.css` file to resize and center our image on the page.

```css
body {
	background-color: black;
  color: white;
  margin-left: 10%;
  margin-right: 10%;
  margin-top: 2%;
  margin-bottom: 2%;
}

h1 {
	color: green;
  text-align: center;
}

img {
	display: block;
  margin: auto;
  width: 50%;
}

.warning {
	background-color: red;
  color: white;
  border: 1px solid yellow;
  text-align: center;
  padding: 1%;
}
```

The `width` attribute allows us to resize the image to a specific percentage of our screen size. In this case we are resizing our image to fill up half of the screen. Displaying the image as a block element gives us the ability to align it horizontally. Finally, setting the image’s margin to auto will position the image in the center of the screen horizontally. 

## Chapter Six

### Introduction to Javascript Programming


Up until now we’ve been writing HTML and CSS code which are both markup languages. From this point forward we will be learning Javascript which is a full blown programming language. This will increase the complexity of the code slightly as we now have access to variables, loops, conditional statements, and more but this also means that we will have the power to create much more powerful programs.


To write Javascript for our website we will be using the P5.js framework. This allows us to easily create animations and interactive games.


To get started with P5.js we need to import the framework from our `index.html` file just like we did with our CSS file. Create a new file named `script.js` in your `my-website` folder and then add these two new lines to the head of your HTML file.

```html
<html>

	<head>
		<link href="styles.css" rel="stylesheet" type="text/css">
  	<script src="https://cdn.jsdelivr.net/npm/p5@1.0.0/lib/p5.js"></script>
  	<script src="script.js"></script>
  	<title>My new website</title>
	</head>

	<body>
		<h1>Welcome to my website!</h1>
  	<p class="warning">Warning: this page is under construction!</p>
  	<p>This is where you can write about all of your favorite things</p>
  	<p>Click <a href="https://bitspacechicago.com">here</a> to visit my favorite website</p>
	</body>

</html>
```

Additionally, let’s add a new section to our `styles.css` file to center our javascript canvas on the web page just like we did for images.

```css
body {
	background-color: black;
  color: white;
  margin-left: 10%;
  margin-right: 10%;
  margin-top: 2%;
  margin-bottom: 2%;
}

h1 {
	color: green;
	text-align: center;
}

img {
	display: block;
  margin: auto;
  width: 50%;
}


canvas {
  display: block;
  margin: auto;
  margin-top: 2%;
}


.warning {
  background-color: red;
  color: white;
  border: 1px solid yellow;
  text-align: center;
  padding: 1%;
}
```

Now that we have everything set up we can open our `script.js` file and get started.


P5.js programs are primarily written inside of two important, built in functions. The `setup()` function is only run __once__ when the program first starts. The `draw()` function runs continuously in a __loop__ the entire time the program is running. Open up your `script.js` file and add these two functions.

```javascript
function setup() {

}

function draw() {

}	
```

The first thing we need to do is create a canvas that will store and display our project. This is done using the `createCanvas()` function which takes width and height arguments. For these arguments we can use a built in variable from the P5.js framework - `windowWidth` which is automatically set to the width of your browser window. While we’re at it, let’s add a new function to resize our canvas whenever the browser window is resized.

```javascript
function setup() {
	createcanvas(windowWidth/2, windowWidth/2);
}

function draw() {

}

function windowResized() {
	resizeCanvas(windowWidth/2, windowWidth/2);
}
```

Now we have a Javascript canvas using P5.js that is automatically resized to a square that is half the width of our browser window and is automatically centered on our screen using CSS.

## Chapter Seven

### Interactivity


First, let's set the background color of our javascript canvas so that we can see it more clearly. To do this we can use the built-in function `background()`. The background function takes an RGB color which is made up of three numbers, each between 0 and 255. The first number determines how much red is in the color, the second number determines how much green is in the color, and the third number determines how much blue is in the color. For example  0, 0, 0 is black, 255, 255, 255 is white, 0, 0, 255 is blue, and  238, 130, 238 is purple.


Choose your favorite color and set the background to it.

```javascript
function setup() {
	createCanvas(windowWidth/2, windowWidth/2);
}

function draw() {
	background(238, 130, 238);
}

function windowResized() {
	resizeCanvas(windowWidth/2, windowWidth/2);
	background(238, 130, 238);
}
```
