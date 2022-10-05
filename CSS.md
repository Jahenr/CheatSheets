<h1> Font Properties </h1>

#Changes the font family of certain words, sentences,
paragraphs, etc.<br>
	&emsp;&emsp;Font-Family<br>
	&emsp;&emsp;&emsp;&emsp;P { font-family: "New Century Schoolbook", Times, serif; }

#Changes text: normal, oblique, and italics.<br>
	&emsp;&emsp;Font-Style<br>
	&emsp;&emsp;&emsp;&emsp;H1 { font-style: oblique; }<br>
	&emsp;&emsp;&emsp;&emsp;P { font-style: normal; }
	

#Used to display font in normal or small-caps.<br>
	&emsp;&emsp;Font-Variant<br>
	&emsp;&emsp;&emsp;&emsp;SPAN { font-variant: small-caps; }
	
#Used to specify the weight of the font.<br>
	&emsp;&emsp;Font-Weight<br>
	&emsp;&emsp;&emsp;&emsp;H1 { font-weight: 800; } or<br>
	&emsp;&emsp;&emsp;&emsp;P { font-weight: normal; }

	
#Used to modify the size of the displayed font.<br>
	&emsp;&emsp;Font-Size<br>
	&emsp;&emsp;&emsp;&emsp;H1 { font-size: large; } or P { font-size: 12pt; }<br>
	&emsp;&emsp;&emsp;&emsp;LI { font-size: 90%; }<br>
	&emsp;&emsp;&emsp;&emsp;STRONG { font-size: larger; }

#Used to combine all properties of fonts.<br>
	&emsp;&emsp;Font<br>
	&emsp;&emsp;&emsp;&emsp;P { font: italic bold 12pt/14pt Times, serif; }
	
	
<h1> Color and Background Properties </h1>

#To Change the color of text.<br>
&emsp;&emsp;Color<br>
&emsp;&emsp;&emsp;&emsp;H1 { color: blue; } or<br>
&emsp;&emsp;&emsp;&emsp;H2 { color: #000080; }<br>

#Sets the background color of an element.<br>
&emsp;&emsp;Background-Color<br>
&emsp;&emsp;&emsp;&emsp;BODY { background-color: white; }<br>
&emsp;&emsp;&emsp;&emsp;H1 { background-color: #000080; }<br>

#Sets the background image of an element.<br>
&emsp;&emsp;Background-Image<br>
&emsp;&emsp;&emsp;&emsp;BODY { background-image: url(/images/foo.gif); }<br>
&emsp;&emsp;&emsp;&emsp;P { background-image: url(http://www.htmlhelp.com/bg.png); }<br>

#Determines how a specified background image is repeated.<br>
&emsp;&emsp;Background-Repeat<br>
#The repeat-x value will repeat the image horizontally while the
repeat-y value will repeat the image vertically.<br>
&emsp;&emsp;&emsp;&emsp;BODY { background: white url(candybar.gif);<br>
&emsp;&emsp;&emsp;&emsp;background-repeat: repeat-x; }<br>

#Determines if a specified background image will scroll with the
content or be fixed with regard to the canvas.<br>
&emsp;&emsp;Background-Attachment<br>
&emsp;&emsp;&emsp;&emsp;BODY { background: white url(candybar.gif);background-attachment: fixed; }<br>

#Used to combine all properties of background.<br>
&emsp;&emsp;Background<br>
&emsp;&emsp;&emsp;&emsp;BODY { background: white url(http://www.htmlhelp.com/foo.gif); }<br>
&emsp;&emsp;&emsp;&emsp;BLOCKQUOTE { background: #7fffd4; }<br>
&emsp;&emsp;&emsp;&emsp;P { background: url(../backgrounds/pawn.png) #f0f8ff fixed; }<br>
&emsp;&emsp;&emsp;&emsp;TABLE { background: red url(leaves.jpg) no-repeat bottom right; }<br>




<h1>Text Properties</h1>

#Defines an additional amount of space between words.<br>
&emsp;&emsp;Word-Spacing<br>
&emsp;&emsp;&emsp;&emsp;p{ word-spacing: 0.4em; }<br>
&emsp;&emsp;&emsp;&emsp;h6{ word-spacing: -0.2em; }<br>

#Defines an additional amount of space between characters.<br>
&emsp;&emsp;Letter-Spacing<br>
&emsp;&emsp;&emsp;&emsp;H1 { letter-spacing: 0.1em; }<br>
&emsp;&emsp;&emsp;&emsp;p{ letter-spacing: -0.1em; }<br>

#Allows text to be decorated through one of five properties:<br>
&emsp;&emsp;Text-Decoration<br>
&emsp;&emsp;&emsp;&emsp;underline, overline, line-through, blink, none.<br>
&emsp;&emsp;&emsp;&emsp;A:link, A:visited, A:active { text-decoration: none; }<br>


#Allows for capitalizing the first letter of each word (capitalize),capitalizing all letters of a word (uppercase),
using all small letters in each word(lowercase), and the inital value(none).<br>
&emsp;&emsp;Text-Transform<br>
&emsp;&emsp;&emsp;&emsp;H1 { text-transform: uppercase; }<br>
&emsp;&emsp;&emsp;&emsp;H2 { text-transform: capitalize; }<br>

#Used to justify text left, center, right, and justify.<br>
&emsp;&emsp;Text-Align<br>
&emsp;&emsp;&emsp;&emsp;H1 { text-align: center; }<br>

#Used to specify the amount of indentation prior to the first line of text<br>
&emsp;&emsp;Text-Indent<br>
&emsp;&emsp;&emsp;&emsp;P { text-indent: 5em; }<br>

#Used to control the spacing between baselines of text.<br>
&emsp;&emsp;Line-Height<br>
&emsp;&emsp;&emsp;&emsp;P { line-height: 200%; }<br>



<h1>Box Properties</h1>

	Margin
#Sets the top margin of an element by specifying a length or a
percentage.<br>
	&emsp;&emsp;Margin-Top<br>
&emsp;&emsp;&emsp;&emsp;BODY { margin-top: 5pt; }<br>

#Sets the right margin of an element by specifying a length or a
percentage.<br>
	&emsp;&emsp;Margin-Right<br>
&emsp;&emsp;&emsp;&emsp;P.narrow { margin-right: 50%; }<br>

#sets the bottom margin of an element by specifying a length or
a percentage.<br>
	&emsp;&emsp;Margin-Bottom<br>
&emsp;&emsp;&emsp;&emsp;DT { margin-bottom: 3em; }<br>

#sets the left margin of an element by specifying a length or a
percentage.<br>
	&emsp;&emsp;Margin-Left<br>
&emsp;&emsp;&emsp;&emsp;ADDRESS { margin-left: 50%; }<br>

#Sets the margins of an element by specifying top, bottom, left
and right margins -- all either specifying length or percentage.<br>
	&emsp;&emsp;Margin<br>
&emsp;&emsp;&emsp;&emsp;BODY { margin: 5em; } /* all margins 5em */<br>
&emsp;&emsp;&emsp;&emsp;P { margin: 2em 4em; } /* top & bottom 2em, left & right 4em */<br>
&emsp;&emsp;&emsp;&emsp;DIV { margin: 1em 2em 3em 4em; }/* top margin 1em, right 2em, bottom 3em, left 4em */<br>

	Padding
#Describes the amount of space between the top border and
the content of the selector.<br>
 &emsp;&emsp;Padding-Top<br>
	&emsp;&emsp;&emsp;&emsp;P { padding-top: 20%; }<br>

#Describes the amount of space between the right border and
the content of the selector.<br>
	&emsp;&emsp;Padding-Right<br>
&emsp;&emsp;&emsp;&emsp;P { padding-right: 20 px; }<br>

#Describes the amount of space between the bottom border
and the content of the selector.<br>
	&emsp;&emsp;Padding-Bottom<br>
&emsp;&emsp;&emsp;&emsp;P { padding-bottom: 5 em; }<br>

#Describes the amount of space between the left border and
the content of the selector.<br>
	&emsp;&emsp;Padding-Left<br>
&emsp;&emsp;&emsp;&emsp;P { padding-left: 15 pt; }<br>

#Shorthand for the padding-top, padding-right, padding-bottom,
and padding-left properties.<br>
	&emsp;&emsp;Padding<br>
&emsp;&emsp;&emsp;&emsp;BLOCKQUOTE { padding: 2em 4em 5em 4em; }<br>
	
	
	
	Borders
#Used to specify the width of an element's top border.<br>
	&emsp;&emsp;Border-Top-Width<br>
&emsp;&emsp;&emsp;&emsp;P { border-top: 20%; }<br>
	

#Used to specify the width of an ele#ent's right border.<br>
	&emsp;&emsp;Border-Right-Width<br>
&emsp;&emsp;&emsp;&emsp;P { border-right: 20%; }<br>

#Used to specify the width of an element's bottom border.<br>
	&emsp;&emsp;Border-Bottom-Width<br>
&emsp;&emsp;&emsp;&emsp;P { border-bottom: 20%; }<br>
	
#Used to specify the width of an element's left border.<br>
	&emsp;&emsp;Border-Bottom-Width<br>
&emsp;&emsp;&emsp;&emsp;P { border-left: 20%; }<br>

#Used to set the width of an element's border (either all
borders, or specifying top border, right border, bottom border,
left border).<br>
	&emsp;&emsp;Border-Width<br>
&emsp;&emsp;&emsp;&emsp;P { border-width: 20%; }<br>
&emsp;&emsp;&emsp;&emsp;P { border-width: 10px 5px 10px 5px; }<br>

#Used to set the color of an element's border.<br>
	&emsp;&emsp;Border-Color<br>
&emsp;&emsp;&emsp;&emsp;P { border-color: #00000; }<br>

#Sets style of a border - none, dotted, dashed, solid, double.<br>
		&emsp;&emsp;Border-Style<br>
&emsp;&emsp;&emsp;&emsp;P { border-style: dotted; }<br>

#Sets the width, style, and color of an element's top border.<br>
	&emsp;&emsp;Border-Top<br>
&emsp;&emsp;&emsp;&emsp;P { border-top: 10px, red, double;} <br>

#Sets the width, style, and color of an element's right border.<br>
	&emsp;&emsp;Border-Right<br>
&emsp;&emsp;&emsp;&emsp;P { border-right: 10px, red, double; }<br>

#Sets the width, style, and color of an element's bottom border.<br>
	&emsp;&emsp;Border-Bottom<br>
&emsp;&emsp;&emsp;&emsp;P { border-bottom: 10px, red, double; }<br>

#Sets the width, style, and color of an element's left border.<br>
	&emsp;&emsp;Border-Left<br>
&emsp;&emsp;&emsp;&emsp;P { border-left: 10px, red, double; }<br>

#Sets the width, style, and color of an element's border.<br>
	&emsp;&emsp;Border<br>
&emsp;&emsp;&emsp;&emsp;P { border: 10px, red, double; }<br>

#Each block-level or replaced element can be given a width,
specified as a length, a percentage, or as auto.<br>
	&emsp;&emsp;Width<br>
&emsp;&emsp;&emsp;&emsp;P { width: 15px; }<br>
&emsp;&emsp;&emsp;&emsp;H1 { width: 35%; }<br>
&emsp;&emsp;&emsp;&emsp;.foo { width: auto; }<br>

#Each block-level or replaced element can be given a height,
specified as a length or as auto.<br>
	&emsp;&emsp;Height<br>
&emsp;&emsp;&emsp;&emsp;P { height: 15px; }<br>
&emsp;&emsp;&emsp;&emsp;H1 { height: 35%; }<br>
&emsp;&emsp;&emsp;&emsp;.foo { height: auto; }<br>

#Allows text to wrap around an element (left, right, none).<br>
	&emsp;&emsp;Float<br>
&emsp;&emsp;&emsp;&emsp;P { float: left; }<br>
&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;H1 { float: right; }<br>
&emsp;&emsp;&emsp;&emsp;.foo { float: none; }<br>

