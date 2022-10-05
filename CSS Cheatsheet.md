
# CSS CHEATSHEET

Font Properties

    Font-Family
    Changes the font family of certain words, sentences,
    paragraphs, etc.
    P { font-family: "New Century Schoolbook", Times, serif; }
                                  
Font-Style

    Changes text: normal, oblique, and italics.
    H1 { font-style: oblique; }
    P { font-style: normal; }
        
Font-Variant

    Used to display font in normal or small-caps.
    SPAN { font-variant: small-caps; }

Font-Weight

    Used to specify the weight of the font.
    H1 { font-weight: 800; } or P { font-weight: normal; }

Font-Size

    Used to modify the size of the displayed font.
    H1 { font-size: large; } or P { font-size: 12pt; }
    LI { font-size: 90%; }
    STRONG { font-size: larger; }
 
Font

   Used to combine all properties of fonts.

    P { font: italic bold 12pt/14pt Times, serif; }


**Color and Background Properties**
    
Color

    Changes the color of text.
    H1 { color: blue; } or H2 { color: #000080; }

Background-Color

    Sets the background color of an element.
    BODY { background-color: white; }
    H1 { background-color: #000080; }

Background-Image

    Sets the background image of an element.
    BODY { background-image: url(/images/foo.gif); }
    P { background-image: url(http://www.htmlhelp.com/bg.png); }

Background-Repeat

    Determines how a specified background image is repeated.

    The repeat-x value will repeat the image horizontally while the
    repeat-y value will repeat the image vertically.
    BODY { background: white url(candybar.gif);
    background-repeat: repeat-x; }

Background-Attachment

 Determines if a specified background image will scroll with the
 content or be fixed with regard to the canvas.

    BODY { background: white url(candybar.gif);
    background-attachment: fixed; }
    Background
    Used to combine all properties of background.
    BODY { background: white url(http://www.htmlhelp.com/foo.gif); }
    BLOCKQUOTE { background: #7fffd4; }
    P { background: url(../backgrounds/pawn.png) #f0f8ff fixed; }
    TABLE { background: red url(leaves.jpg) no-repeat bottom right; }


**Text Properties**

Word-Spacing

Defines an additional amount of space between words.

    P EM { word-spacing: 0.4em; }
    P.note { word-spacing: -0.2em; }

Letter-Spacing

Defines an additional amount of space between characters.

    H1 { letter-spacing: 0.1em; }
    P.note { letter-spacing: -0.1em; }

Text-Decoration

  Allows text to be decorated through one of five properties:
  underline, overline, line-through, blink, none.
    
    A:link, A:visited, A:active { text-decoration: none; }
    Vertical-Align

  Used to alter the vertical positioning of an inline element,
  relative to its parent element or to the element's line.

    IMG.middle { vertical-align: middle; }
    IMG { vertical-align: 50%; }
    .exponent { vertical-align: super; }

Text-Transform

 Allows for capitalizing the first letter of each word (capitalize),
 capitalizing all letters of a word (uppercase), using all small
 letters in each word(lowercase), and the inital value(none).

    H1 { text-transform: uppercase; }
    H2 { text-transform: capitalize; }

Text-Align

Used to justify text left, center, right, and justify.

    H1 { text-align: center; }
    P.newspaper { text-align: justify; }

Text-Indent

 Used to specify the amount of indentation prior to the first line
 of text.

    P { text-indent: 5em; }

Line-Height

 Used to control the spacing between baselines of text.

    P { line-height: 200%; }

**Classification Properties**

List-Style-Type

Specifies the type of list-item marker,
 and is used if list-styleimage is none or if image loading is turned off
.
    
    LI.square { list-style-type: square; }
    UL.plain { list-style-type: none; }
    OL { list-style-type: upper-alpha; } /* A B C D E etc. */
    OL OL { list-style-type: decimal; } /* 1 2 3 4 5 etc. */
    OL OL OL { list-style-type: lower-roman; } /* i ii iii iv v etc. */

List-Style-Image

  Specifies the image that will be used as list-item marker when
  image loading is turned on, replacing the marker specified in
  the list-style-type property.

    UL.check { list-style-image: url(/LI-markers/checkmark.gif); }
    UL LI.x { list-style-image: url(x.png); }

List-Style-Position

 Determines where the marker is placed in regard to the list
 item. If the value inside is used, the lines will wrap under the
marker instead of being indented. outside is default.

    UL { list-style-position: inside; } 





**Box Properties** 


  Margin-Top

   Sets the top margin of an element by specifying a length or a
   percentage.

    BODY { margin-top: 5pt; }

  Margin-Right

  Sets the right margin of an element by specifying a length or a
  percentage.

    P.narrow { margin-right: 50%; }

Margin-Bottom

 sets the bottom margin of an element by specifying a length or
 a percentage.

    DT { margin-bottom: 3em; }

Margin-Left

 sets the left margin of an element by specifying a length or a
 percentage.

    ADDRESS { margin-left: 50%; }

Margin

Sets the margins of an element by specifying top, bottom, left
and right margins -- all either specifying length or percentage.

    BODY { margin: 5em; } /* all margins 5em */
    P { margin: 2em 4em; } /* top & bottom 2em, left & right 4em */
    DIV { margin: 1em 2em 3em 4em; }
    /* top margin 1em, right 2em, bottom 3em, left 4em */

Padding-Top
Describes the amount of space between the top border and
the content of the selector.

    P { padding-top: 20%; }

Padding-Right

Describes the amount of space between the right border and
the content of the selector.

    P { padding-right: 20 px; }

Padding-Bottom

Describes the amount of space between the bottom border
and the content of the selector.

    P { padding-bottom: 5 em; }

Padding-Left

Describes the amount of space between the left border and
the content of the selector.

    P { padding-left: 15 pt; }

Padding

Shorthand for the padding-top, padding-right, padding-bottom,
and padding-left properties.

    BLOCKQUOTE { padding: 2em 4em 5em 4em; }

Border-Top-Width

  Used to specify the width of an element's top border.

    P { border-top: 20%; }

Border-Right-Width

  Used to specify the width of an element's right border.

    P { border-right: 20%; }

Border-Bottom-Width

Used to specify the width of an element's bottom border.

    P { border-bottom: 20%; }





Border-Left-Width

Used to specify the width of an element's left border.

    P { border-left: 20%; }

Border-Width

Used to set the width of an element's border (either all
borders, or specifying top border, right border, bottom border,
left border).

    P { border-width: 20%; }
    P { border-width: 10px 5px 10px 5px; }

Border-Color

Used to set the color of an element's border.

    P { border-color: #00000; }

Border-Style

Sets style of a border - none, dotted, dashed, solid, double.

    P { border-style: dotted; }

Border-Top

Sets the width, style, and color of an element's top border.

    P { border-top: 10px, red, double; }

Border-Right

Sets the width, style, and color of an element's right border.

    P { border-right: 10px, red, double; }

Border-Bottom

Sets the width, style, and color of an element's bottom border.

    P { border-bottom: 10px, red, double; }
    Border-Left

Sets the width, style, and color of an element's left border.

    P { border-left: 10px, red, double; }

Border

Sets the width, style, and color of an element's border.

    P { border: 10px, red, double; }

Width

Each block-level or replaced element can be given a width,
specified as a length, a percentage, or as auto.

    P { width: 15px; }
    H1 { width: 35%; }
    .foo { width: auto; }

Height

Each block-level or replaced element can be given a height,
specified as a length or as auto.

    P { height: 15px; }
    H1 { height: 35%; }
    .foo { height: auto; }

Float

Allows text to wrap around an element (left, right, none).

    P { float: left; }
    H1 { float: right; }
    .foo { float: none; }

Clear

 Specifies whether an element allows floating elements to its

   sides (left, right, none).
   
    P { clear: left; }
    H1 { clear: right; }
    .foo { clear: none; }
