# June-13th-Blog-Developer-Portfolio-Site-with-CSS-Float
A simple static website layout showcasing a developer's portfolio.

# Introduction
I have been learning web development for the last month or so. In that period, I have digested many HTML and CSS concepts that I am now applying in my first project built from scratch (It’s public, find it [here](https://github.com/Mutuma-Gitonga/June-13th-Blog-Developer-Portfolio-Site-with-CSS-Float) on my GitHub profile). 

Although it is a simple static web layout project, it is significantly fulfilling working it to completion. Therefore, strap in as I take you through my development process stepwise. But first, I will highlight the tools I used in the process.
# Tools
**Text-editor:** Sublime Text was my tool of choice for its brilliant code completion and colored highlights. 

**Git:** I used git in the iTerm2 terminal, but a Git Bash terminal would still do. Of course, git aids in tracking and committing code file changes (version control) to the local repository and pushing them to remote repositories.

**Distributed version control software:** GitHub. I pushed my code to GitHub for future reference. For your information, I am writing this article as I reference my GitHub commit history. 

**Google and Stack Overflow:** Google and Stack Overflow are always necessary, helping me get unstuck in the face of code problems, including today.
## Step 1: Creating an Empty Skeleton HTML file
The first step is creating a skeleton HTML file upon which to add other relevant HTML elements and later CSS styles. Below is the code on the same.

```
<!DOCTYPE html>
<html>
<head>
	<title></title>
</head>
<body>

</body>
</html>
``` 
## Step 2: Title Element Content and The Relevant Meta Elements in the Head Element
Next is typing in a meaningful name for the HTML page within the title element (to be shown on the browser tab). In addition, there is the inclusion of four meta name attributes, that is, *description*, *keywords*, *author*, and *viewport *specifications of the document. 

Remember that such meta tags are critical for search engine optimization, precisely the first three in this case. On its part, the viewport tag aids in optimizing a website, especially for mobile viewing. 

According to MDN, attribute value *device-width* means the page occupies 100% of the viewport width, while an *initial scale* of 1 sets page zoom levels at 100%.
Below is the code on the same.

```
<head>
	<title></title>
	<title>Developer Portfolio CSS Float</title>

	<meta name="description" content="A simple website layout created using CSS Float property. Clone it from https://github.com/Mutuma-Gitonga/June-13th-Blog-Developer-Portfolio-Site-with-CSS-Float">

	<meta name="keywords" content="CSS float, web layout, HTML, CSS, CSS template">

	<meta name="viewport" content="width=device-width, initial-scale=1.0">

	<meta name="author" content="Mutuma Gitonga">
</head>
``` 
## Step 3: Adding div Elements to Create the Necessary Body Sections
Div is a block element that makes it easy to divide an HTML page into sections. Block elements take the entire width of the page in contrast to inline elements that only occupy the necessary width. 

This task aims to divide the page into three parts: a header section, a main section, and a footer. The div element provides non-semantic page division since its content has no meaning to either a developer or a browser. 

Classes are equally added to div elements for eventual CSS styling. See the code snippet below.

```
<body>
	<div class="header">

	</div>


	<div class="clearfix">
		<div class="column image">

		</div>


		<div class="column content">

		</div>


		<div class="column menu">

		</div>		
	</div>


	<div class="footer">

	</div>
</body>
```
## Step 4: Adding Relevant HTML Content to the Created div Body Element Sections 
In the “header” class div container, a heading is added is added as shown in the code snippet below.

```
<div class="header">

		<h1>John Smith, FrontEnd Developer</h1>
</div>
``` 
The main section div container has a style class called “clearfix” (use any other class name you wish). Within this “clearfix” div container are three other div elements with the class labels “column image,” “column content,” and “column menu.”

Notice that these three div elements have two class names each, with the first name “column” being shared among the three. The shared first name is used for floating the three div elements to the left, as will be seen later in the styling section.  

Following this, relevant contents are added to the three div elements as in the code snippet below.

```
<div class="clearfix">
		<div class="column image">

			<img src="laptop.jpg" alt="laptop with code">
		</div>


		<div class="column content">

			<h1>Project 1: HTML and CSS Website</h1>

			<p>Employed HTML and CSS fundamentals to create a static website. Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod
			tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam,
			quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo
			consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse
			cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non
			proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
		</div>


		<div class="column menu">

			<ul>
				<li><a href="#portfolio">Portfolio</a></li>
				<li><a href="#blog">Blog</a></li>
				<li><a href="#github">Github</a></li>
			</ul>
		</div>		
</div>
In the same light, appropriate content is added in the footer div container as shown in the code below.
<div class="footer">

		<h2>Contact Me</h2>

		<ul>
			<li><a href="mailto: someone@example.com">Send Email</a></li>
			<li><a href="tel:555779455">Message me on Cell</a></li>
		</ul>
</div>
``` 
## Step 5: Global Styles Using Internal CSS
In this step, the style element is declared in the head element. In this internal CSS section, two global styles (applying to the entire document) are added.
```
<style>
		* {
			box-sizing: border-box;
		}

		body {
			background-color: white;
		}
</style>
```
The “box-sizing: border-box” property value ensures element padding and border width are included in the specified element width. On the other hand, the “background-color: white” property value sets the document body background color to white.
## Step 6: Styling the “header” class div Element 
Now, five styles are added to the “header” class div element including its background color, padding, font-size, font-weight, and text-alignment.
```
.header {
			background-color: lightsteelblue;
			padding: 20px;
			font-size: 1.4em;
			font-weight: bold;
			text-align: center;
		}
```
## Step 7: Styling the Main Section div elements
Here, the three div elements with “column image”, “column content”, and “column menu” classes have their styles specified.
Foremost, the “column” shared class specifies the three div elements float to the left and a specific padding for each one as in the snippet below.
```
.column {
			float: left;
			padding: 20px;
		}
```
Next, the widths of the three floated div elements in relation to the page width are specified. As the code indicates, the image class occupies 15%, the content class 60%, and the menu class 25%. Notice that it totals 100% of the page width.
```
.image {
	width: 15%;
} 
.content {
    width: 60%;
}
.menu {
	width: 25%;
}
```
### Special Note
I had a problem setting the image to occupy its specified 15% width strictly. I defined it as 15% in the CSS selector, only for it to overflow beyond its confines into the content container or sometimes into the menu container. 

On researching the problem online, I found an article that suggested setting the image’s width and height to 100% and including the object-fit property. 

Therefore, I added the suggested properties as inline CSS styles in the image element as in the snippet that follows.
```
<img src="laptop.jpg" alt="laptop with code" style="width: 100%; height: 100%; object-fit: contain;">
```
Implementing the above inline style ensures the image fits within its specified container width (in this case, 15%) without becoming disproportional.  

At this juncture, the descendant selector “.menu ul” selects the unordered list and removes bullets using the list-style-type property as indicated in the code snippet below.
```
.menu ul {
			list-style-type: none;
		}
```
Equally, the descendant selector “.menu li” selects individual list elements and applies four styles to the each of the list items as shown in the code snippet below. 
```
.menu li {
			background-color: coral;
			font-size: 1.5em;
			margin-bottom: 20px;
			padding: 30px;

		}
```
For a special touch, there is inclusion of a style to change the menu list elements background color on a mouse-over.
```
.menu li:hover {
			background-color: orange;
		}
```
Now, the descendant selector “.menu a” is added to change two anchor element properties, that is, “text-decoration:none” to remove underline and “color:white” to alter the anchor element color to white. 
```
.menu a {
			text-decoration: none;
			color: white;
		}
```
This final style impacts the page’s main section, preventing an overflowing floated element from introducing scroll bars.
```
.clearfix::after {
			content: "";
			clear: both;
			display: table;
		}
```
## Step 8: Styling the Footer div Element
Foremost, the “footer” class selector defines four element styling properties for the div element including background color, padding, font size, and text alignment.
```
.footer {
			background-color: lightsteelblue;
			padding: 20px;
			font-size: 1.5em;
			text-align: center;
		}
```
Secondly, the descendant selector “.footer ul” removes unordered list’s bullets and sets its padding to zero to center align the list in relation to the heading 2 element above it.
```
.footer ul {
			list-style-type: none;
			padding: 0px;
		}
```
Lastly, the descendant selector “.footer a” defines three properties which remove the link underline, embolden the text, and change its color to blue.
```
.footer a {
			text-decoration: none;
			font-weight: bold;
			color: blue;
		}
```
## Step 9: Reducing the Footer div Element Bottom Margin
At this point, I was delighted about my creation, but my obsessive compulsion could not help but notice the larger-than-necessary footer div element bottom margin. 

Therefore, I chose to specify a bottom margin for the main section to solve the problem. The snippet below indicates the solution.
```
.column {
			margin-bottom: 20px;
		}
```
However, the same effect could have been achieved by adding a top margin to the footer div element like so:
```
.footer {
			margin-top: 20px;
		}
```
## Step 10: Creating an External Stylesheet instead of Using Internal CSS 
As the last step, I chose to create an external CSS file and link it to the almost purely HTML document rather than using internal CSS. 

While learning about web development, I have come across many articles suggesting that using an external stylesheet is cleaner and more efficient, especially when styling multiple HTML pages or files. 

Although my project has only one HTML file, I thought it’s wise to adopt this best practice as early as now.
# Conclusion
In this article, we have walked through ten steps to creating a static web layout employing the CSS float property. 

I believe the development process is detailed but simple enough to understand HTML elements’ declaration and CSS styling. 

Enjoyed the piece? React and comment. Cheers!
