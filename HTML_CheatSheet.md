# HTML Tags


# Format

## Doctype Tag
declares the document type for browsers
```html
<!DOCTYPE html>
```

## html Tag
prime tag to start writing html file code
```html
<html>contains all data and tags of the html file</html>
```

## Head Tag
Container for metadata
```html
<head>Head text</head>
```
example: 
<head>Head Text</head>

## Title Tag
The title of your project - present inside Head tag
```html
<title>title text</title>
```
example: 
<title>title Text</title>

## Body Tag
Container for data and context
```html
<body>body text</body>
```
example: 
<body>body Text</body>

## meta Tag
specify the character set, page description, keywords, author of the document, and viewport settings for SEO
```html
<meta />
```
example: 
<meta name="description" content="Free Web tutorials">

## link Tag
link to external style sheets and files
```html
<link rel="stylesheet" href="" />
```
example: 
<link rel="stylesheet" href="./test.css" />text

## style Tag
used to define style information for a single document - inline css
```html
<style>/*CSS commands*/</style>
```

# HTML Semantics

## header Tag
Specifies a header for a document or section
```html
<header>header text</header>
```

## main Tag
Specifies the main content of a document
```html
<main>contents</main>
```

## footer Tag
Defines a footer for a document or section
```html
<footer>footer text</footer>
```

## article Tag
Defines independent, self-contained content
```html
<article>article context</article>
```

## navigation Tag
Defines navigation links
```html
<nav><a href="/html/">HTML</a> | <a href="/css/">CSS</a> | <a href="/js/">JavaScript</a></nav>
```

## section Tag
Defines a section in a document
```html
<section>section context</section>
```

## aside Tag
Defines content aside from the page content
```html
<aside>aside context</aside>
```

## figure Tag
Specifies self-contained content - Embeds annotated images, illustrations, photos, code, etc.
```html
<figure></figure>
```

## figure Tag
For adding a caption/annotation to the figure tag
```html
<figcaption></figcaption>
```

## picture tag
Responsive image insertion,allows developers to provide different images for different contexts.
```html
<picture><source></source></picture>
```

## Image Tag
just like picture tag it ios used to add images
```html
You can add image if it is stored in your working space like this:
```html
<img src="img_girl.jpg" width="400" height="400" />
```
Or you can add image directly from your browser like this:
```html
<img
  src="https://cdn.mos.cms.futurecdn.net/hFm4iWXhbw4c4rdcMH8tUD.jpg"
  width="400"
  height="400"
/>
```
Output of 2nd method:
<img src="https://cdn.mos.cms.futurecdn.net/hFm4iWXhbw4c4rdcMH8tUD.jpg"  width="400" height="400">

## SVG
Container for SVG graphics
```html
<svg src=""></svg> 
```

## video tag
For embedding videos into a website.
```html
<video poster=" " autoplay loop controls ><source></source></video>
```
poster is the path to an image that’s displayed before the video plays.

example:
```html
<video controls src="movie.mp4" type="video/mp4">Video type not supported by this browser!</video>
```

## audio tag
For embedding audio into a website.
```html
<audio><source></source></audio>
```

## source tag
used to add source location in picture, audio or video tags. 
```html
<source></source>
```

## Anchor
Link to url/a section of webpage/
```html
<a href="url">link text</a> 
<a href="#yourSection">link text</a>
```
to open as a new tab:
```html
<a href="url" target="_blanl">link text</a>
```


# Headings

## Heading 1 - strongest
```html
<h1>heading1</h1>
```
example: <h1>heading1</h1>

## Heading 2 
```html
<h2>heading2</h2>
```
example: <h2>heading2</h2>

## Heading 3 
```html
<h3>heading3</h3>
```
example: <h3>heading3</h3>

## Heading 4
```html
<h4>heading4</h4>
```
example: <h4>heading4</h4>

## Heading 5 
```html
<h5>heading5</h5>
```
example: <h5>heading5</h5>

## Heading 6
```html
<h6>heading6</h6>
```
example: <h6>heading6</h6>


# Font 

## emphasize
```html
<em> emphaize </em>
```
examples: <em> emphaize </em>

## italic
```html
<i> italics </i>
```
examples: <i> italics </i>

## bold
```html
<b> emphaize </b>
```
examples: <b> bold </b>

## underlined
```html
<u> emphaize </u>
```
examples: <u> underlined text </u>

## strong
```html
<strong> strong </strong>
```
examples: <strong>strong</strong>

## small
```html
<small>small</small>
```
examples: <small>small</small>

## strikethrough
```html
<strike> striked text </strike>
```
examples: <strike> striked text </strike>

## Break
used to break to the next line
```html
<br />
```

## Horizontal Ruler
used to add a horizontal ray as a devidor
```html
<hr />
```

# Form

## Forms Tag
container to create HTML forms
```html
<form action="" method="" target=""></form>
```

## inputs Tag 
defines input control - depending on the attribute 'type' (covered below)
```html
<input type="" /> 
```

## Label
defines a label for a form element, according to 'for' attribute
```html
<label for=""></label> 
```

## fieldset
group related elements in a form
```html
<fieldset></fieldset> 
```

## legend
defines caption for fieldset tag
```html
<legend></legend> 
```

## datalist
specifies list of pre-defined options for an input tag ```<output></output>``` used to represent result of a calculation (for using this tag, you will have to use oninput attribute within form tag)
```html
<datalist><option value="">..</option></datalist> 
```

## optgroups
used to group related options
```html
<optgroup></optgroup>
```

# Inputs

## Text input
Defines single line text input field

```html
<input type="text" /> 
```
example:
<input type="text" />

## Text input
defines a multiple line input field

```html
<textarea rows="" cols=""></textarea> 
```
example:
<textarea rows="" cols=""></textarea> 

## number input
defines numeric input field

```html
<input type="number" /> 
```
example:
<input type="number" />

## Password - Protected input
Defines password field
```html
<input type="password" /> 
```
example:
<input type="password" /> 

## Dropdown
defines dropdown list in the form OR defines an option in the dropdown list
```html
<select></select> 
OR
<option value=""></option> 
```

## Button
Defines a clickable button
```html
<button></button> 
```

## Checkbox input
Defines a checkbox
```html
<input type="checkbox" /> 
```
example:
<input type="checkbox" />

## radio input
defines a radio button  
```html
<input type="radio" /> 
```
example:
<input type="radio" /> 

## slider input
slider control 
```html
<input type="range" /> 
```
example:
<input type="range" /> 

## color input
used for input fields that should contain a color 
```html
<input type="color" />
```
example:
<input type="color" />

## Date input
input field should contain date 
```html
<input type="date" /> 
```
example:
<input type="date" />

## Month input
select month and year 
```html
<input type="month" /> 
```
example:
<input type="month" /> 

## week input
select week and year
```html
<input type="week" /> 
```
example:
<input type="week" />  

## time input
select time(without timezone)
```html
<input type="time" /> 
```
example:
<input type="time" />  

## Email input
email type input field
```html
<input type="email" /> 
```
example:
<input type="email" />

## telephone no. input
defines telephone number field
```html
<input type="tel" /> 
```
example:
<input type="tel" /> 

## link input
url address type input field
```html
<input type="url" /> 
```
example:
<input type="url" /> 

## file input
defines file select field and browse button
```html
<input type="file" /> 
```
example:
<input type="file" /> 

## image input
upload image 
```html
<input type="image" /> 
```
example:
<input type="image" /> 

## search bar input
define search field
```html
<input type="search" /> 
```
example:
<input type="search" /> 

## reset input
defines a reset button that will reset all form values to their default values 
```html
<input type="reset" /> 
```
example:
<input type="reset" /> 

## submit input
defines button for submitting form data 
```html
<input type="submit" /> 
```
example:
<input type="submit" /> 


# Table

## Table elements
used to create a tabular data format
```html
<table></table>
Define a table

<tr></tr>
Define a table row

<th></th>
Define a table heading

<td></td>
Define a table data
```

## Table implementation
```html
<table>
  <tr>
    <th>Month</th>
    <th>Savings</th>
  </tr>
  <tr>
    <td>January</td>
    <td>$100</td>
  </tr>
  <tr>
    <td>Febuary</td>
    <td>$200</td>
  </tr>
</table>
```
example:
<table>
  <tr>
    <th>Month</th>
    <th>Savings</th>
  </tr>
  <tr>
    <td>January</td>
    <td>$100</td>
  </tr>
  <tr>
    <td>Febuary</td>
    <td>$200</td>
  </tr>
</table>


# Lists

## List elements

```html
<ul></ul>
Defines an unordered list

<ol></ol>
Defines an ordered list

<li></li>
Defines a list item

<dl></dl>
Defines a description list

<dt></dt>
Defines a term in a description list

<dd></dd>
Describes the term in a description list
```

## Unordered List

```html
<ul>
  <li>Item 1</li>
  <li>Item 2</li>
  <li>Item 3</li>
</ul>
```
examples:
<ul>
  <li>Item 1</li>
  <li>Item 2</li>
  <li>Item 3</li>
</ul>


## Ordered List

```html
<ol>
  <li>Item 1</li>
  <li>Item 2</li>
  <li>Item 3</li>
</ol>
```
examples:
<ol>
  <li>Item 1</li>
  <li>Item 2</li>
  <li>Item 3</li>
</ol>


# Scripting Tags

## Canvas Tag
Used with either the canvas scripting API or the WebGL API to draw graphics and animations.
```html
<canvas></canvas> 
```

## noscript tag
Defines a section of HTML to be inserted if a script type on the page is unsupported or if scripting is currently turned off in the browser.
```html
<noscript></noscript> 
```


# Bonus:

## Emojis

```html
<p style="font-size:48px">&#128512; &#128516; &#128525; &#128151;</p>
```
example:
<p style="font-size:48px">&#128512; &#128516; &#128525; &#128151;</p>

For much deeper dive into the HTML Tags, I suggest you visit: https://www.w3schools.com/tags/tag_u.asp