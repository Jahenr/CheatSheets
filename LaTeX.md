{\rtf1\ansi\ansicpg1252\cocoartf2761
\cocoatextscaling0\cocoaplatform0{\fonttbl\f0\fswiss\fcharset0 Helvetica;}
{\colortbl;\red255\green255\blue255;}
{\*\expandedcolortbl;;}
\paperw11900\paperh16840\margl1440\margr1440\vieww11520\viewh8400\viewkind0
\pard\tx720\tx1440\tx2160\tx2880\tx3600\tx4320\tx5040\tx5760\tx6480\tx7200\tx7920\tx8640\pardirnatural\partightenfactor0

\f0\fs24 \cf0 ## LATEX 2\uc0\u949 Cheat Sheet\
\
## Document classes\
\
book Default is two-sided.\
report No\\partdivisions.\
article No\\partor\\chapterdivisions.\
letter Letter (?).\
slides Large sans-serif font.\
Used at the very beginning of a document:\
\\documentclass\{class\}. Use\\begin\{document\}to start\
contents and\\end\{document\}to end the document.\
\
### Commondocumentclassoptions\
\
10pt/11pt/12pt Font size.\
letterpaper/a4paperPaper size.\
twocolumn Use two columns.\
twoside Set margins for two-sided.\
landscape Landscape orientation. Must usedvips\
-t landscape.\
draft Double-space lines.\
Usage:\\documentclass[opt,opt]\{class\}.\
\
### Packages\
\
fullpageUse 1 inch margins.\
anysize Set margins:\\marginsize\{l\}\{r\}\{t\}\{b\}.\
multicolUsencolumns:\\begin\{multicols\}\{n\}.\
latexsymUse LATEX symbol font.\
graphicxShow image:\\includegraphics[width=x]\{file\}.\
url Insert URL:\\url\{http://.. .\}.\
Use before\\begin\{document\}. Usage:\\usepackage\{package\}\
\
### Title\
\
\\author\{text\} Author of document.\
\\title\{text\} Title of document.\
\\date\{text\} Date.\
These commands go before\\begin\{document\}. The\
declaration\\maketitlegoes at the top of the document.\
\
### Miscellaneous\
\
\\pagestyle\{empty\}Empty header, footer and no page num-\
bers.\
\\tableofcontents Add a table of contents here.\
\
## Document structure\
\
\\part\{title\}\
\\chapter\{title\}\
\\section\{title\}\
\\subsection\{title\}\
\
```\
\\subsubsection\{title\}\
\\paragraph\{title\}\
\\subparagraph\{title\}\
```\
Use\\setcounter\{secnumdepth\}\{x\}suppresses heading\
numbers of depth> x, wherechapterhas depth 0. Use a*, as\
in\\section*\{title\}, to not number a particular item\'97these\
items will also not appear in the table of contents.\
\
### Text environments\
\
\\begin\{comment\} Comment (not printed). Requiresverbatim\
package.\
\\begin\{quote\} Indented quotation block.\
\\begin\{quotation\}Likequotewith indented paragraphs.\
\\begin\{verse\} Quotation block for verse.\
\
### Lists\
\
```\
\\begin\{enumerate\} Numbered list.\
\\begin\{itemize\} Bulleted list.\
\\begin\{description\}Description list.\
\\itemtext Add an item.\
\\item[x]text Usexinstead of normal bullet or number.\
Required for descriptions.\
```\
### References\
\
```\
\\label\{marker\} Set a marker for cross-reference, often of the\
form\\label\{sec:item\}.\
\\ref\{marker\} Give section/body number of marker.\
\\pageref\{marker\}Give page number of marker.\
\\footnote\{text\} Print footnote at bottom of page.\
```\
### Floating bodies\
\
```\
\\begin\{table\}[place] Add numbered table.\
\\begin\{figure\}[place] Add numbered figure.\
\\begin\{equation\}[place]Add numbered equation.\
\\caption\{text\} Caption for the body.\
Theplaceis a list valid placements for the body.t=top,\
h=here,b=bottom,p=separate page,!=place even if ugly.\
Captions and label markers should be within the environment.\
```\
## Text properties\
\
### Font face\
\
```\
Command Declaration Effect\
\\textrm\{text\} \{\\rmfamilytext\} Roman family\
\\textsf\{text\} \{\\sffamilytext\} Sans serif family\
\\texttt\{text\} \{\\ttfamilytext\} Typewriter family\
\\textmd\{text\} \{\\mdseriestext\} Medium series\
\\textbf\{text\} \{\\bfseriestext\} Bold series\
\\textup\{text\} \{\\upshapetext\} Upright shape\
\\textit\{text\} \{\\itshapetext\} Italic shape\
\\textsl\{text\} \{\\slshapetext\} Slanted shape\
\\textsc\{text\} \{\\scshapetext\} Small Caps shape\
\\emph\{text\} \{\\emtext\} Emphasized\
\\textnormal\{text\}\{\\normalfonttext\}Document font\
\\underline\{text\} Underline\
The command (tttt) form handles spacing better than the\
declaration (tttt) form.\
```\
### Font size\
\
```\
\\tiny tiny\
\\scriptsize scriptsize\
\\footnotesizefootnotesize\
```\
#### \\small small\
\
### \\normalsize normalsize\
\
## \\large large\
\
## \\LargeLarge\
\
## \\LARGELARGE\
\
## \\huge huge\
\
# \\Huge Huge\
\
```\
These are declarations and should be used in the form\{\\small\
```\
.. .\}, or without braces to affect the entire document.\
\
### Verbatim text\
\
```\
\\begin\{verbatim\} Verbatim environment.\
\\begin\{verbatim*\}Spaces are shown as.\
\\verb!text! Text between the delimiting characters (in\
this case \'91!\'92) is verbatim.\
```\
### Justification\
\
```\
Environment Declaration\
\\begin\{center\} \\centering\
\\begin\{flushleft\} \\raggedright\
\\begin\{flushright\} \\raggedleft\
```\
### Miscellaneous\
\
```\
\\linespread\{x\}changes the line spacing by the multiplierx.\
```\
## Text-mode symbols\
\
### Symbols\
\
```\
& \\& \\_... \\ldots \'95 \\textbullet\
$ \\$ \'88 \\^\{\} | \\textbar \\ \\textbackslash\
% \\%\uc0\u32 \u771  \\~\{\} # \\# \'a7 \\S\
```\
### Accents\
\
```\
`o \\\'91o\uc0\u32 \u769 o\\\'92o \'88o \\^o\u32 \u771 o \\~o\u32 \u772 o\\=o\
\uc0\u775 o \\.o\u32 \u776 o\\"o\u32 \u807 o \\c o \u711 o \\v o\u32 \u779 o\\H o\
\uc0\u807 c \\c c o. \\d o o\
\uc0\u772 \
```\
```\
\\b o oo\\t oo \'9c\\oe\
\'8c\\OE \'e6\\ae \'c6\\AE\uc0\u32 \u778 a \\aa\u32 \u778 A\\AA\
\'f8 \\o \'d8\\O l \\l L \\L \uc0\u305  \\i\
\uc0\u63166  \\j \'a1 ~\'91 \'bf ?\'91\
```\
### Delimiters\
\
```\
\'91\'91 \'93\'91\'91 \{\\\{ [[ (( <\\textless\
\'92\'92 \'94\'92\'92 \}\\\} ]] )) >\\textgreater\
```\
### Dashes\
\
```\
Name Source Example Usage\
hyphen - X-ray In words.\
en-dash -- 1\'965 Between numbers.\
em-dash --- Yes\'97or no? Punctuation.\
```\
### Line and page breaks\
\
```\
\\\\ Begin new line without new paragraph.\
\\\\* Prohibit pagebreak after linebreak.\
\\kill Don\'92t print current line.\
\\pagebreakStart new page.\
\\noindent Do not indent current line.\
```\
### Miscellaneous\
\
```\
\\today March 28, 2017.\
$\\sim$ Prints\uc0\u8764 instead of\\~\{\}, which makes\u32 \u771 .\
~ Space, disallow linebreak (W.J.~Clinton).\
\\@. Indicate that the.ends a sentence when following\
an uppercase letter.\
\\hspace\{l\} Horizontal space of lengthl(Ex:l=20pt).\
\\vspace\{l\} Vertical space of lengthl.\
\\rule\{w\}\{h\}Line of widthwand heighth.\
```\
## Tabular environments\
\
### tabbingenvironment\
\
```\
\\=Set tab stop. \\> Go to tab stop.\
Tab stops can be set on \'93invisible\'94 lines with\\killat the end\
of the line. Normally\\\\is used to separate lines.\
```\
\
### tabularenvironment\
\
\\begin\{array\}[pos]\{cols\}\
\\begin\{tabular\}[pos]\{cols\}\
\\begin\{tabular*\}\{width\}[pos]\{cols\}\
\
#### tabularcolumn specification\
\
l Left-justified column.\
c Centered column.\
r Right-justified column.\
p\{width\} Same as\\parbox[t]\{width\}.\
@\{decl\} Insertdeclinstead of inter-column space.\
| Inserts a vertical line between columns.\
\
#### tabularelements\
\
\\hline Horizontal line between rows.\
\\cline\{x-y\}Horizontal line across columnsxthroughy.\
\\multicolumn\{n\}\{cols\}\{text\}\
A cell that spansncolumns, withcolscolumn\
specification.\
\
## Math mode\
\
For inline math, use\\(...\\)or$...$. For displayed math,\
use\\[...\\]or\\begin\{equation\}.\
\
Superscriptx ^\{x\} Subscriptx _\{x\}\
x\
y \\frac\{x\}\{y\}\
\
### \uc0\u8721 n\
\
```\
k=1 \\sum_\{k=1\}^n\
```\
### n\uc0\u8730 x \\sqrt[n]\{x\} \u8719 n\
\
```\
k=1 \\prod_\{k=1\}^n\
```\
### Math-mode symbols\
\
\uc0\u8804 \\leq \u8805 \\geq 6 =\\neq \u8776  \\approx\
\'d7\\times \'f7\\div \'b1\\pm \'b7 \\cdot\
\uc0\u9702  ^\{\\circ\} \u9702  \\circ \u8242  \\prime \'b7\'b7\'b7\\cdots\
\
\uc0\u8734 \\infty \'ac\\neg \u8743 \\wedge \u8744  \\vee\
\uc0\u8835 \\supset \u8704 \\forall \u8712 \\in \u8594 \\rightarrow\
\uc0\u8834 \\subset \u8707 \\exists \u8712 / \\notin \u8658 \\Rightarrow\
\uc0\u8746  \\cup \u8745 \\cap | \\mid \u8660 \\Leftrightarrow\
a\uc0\u32 \u775  \\dot a \'88a \\hat a\u32 \u772 a \\bar a\u32 \u771 a \\tilde a\
\uc0\u945  \\alpha \u946 \\beta \u947  \\gamma \u948  \\delta\
 \\epsilon \uc0\u950  \\zeta \u951  \\eta \u949  \\varepsilon\
\uc0\u952  \\theta \u953  \\iota \u954  \\kappa \u952  \\vartheta\
\uc0\u955  \\lambda \u956 \\mu \u957  \\nu \u958  \\xi\
\uc0\u960  \\pi \u961  \\rho \u963  \\sigma \u964  \\tau\
\uc0\u965  \\upsilon \u966 \\phi \u967  \\chi \u968  \\psi\
\uc0\u969  \\omega \u915 \\Gamma \u8710 \\Delta \u920  \\Theta\
\uc0\u923  \\Lambda \u926 \\Xi \u928 \\Pi \u931  \\Sigma\
\uc0\u933 \\Upsilon \u934 \\Phi \u936 \\Psi \u8486  \\Omega\
\
## Bibliography and citations\
\
When using BibTEX, you need to runlatex,bibtex, and\
latextwice more to resolve dependencies.\
\
### Citation types\
\
```\
\\cite\{key\} Full author list and year. (Watson and Crick\
1953)\
\\citeA\{key\} Full author list. (Watson and Crick)\
\\citeN\{key\} Full author list and year. Watson and Crick\
(1953)\
\\shortcite\{key\} Abbreviated author list and year.?\
\\shortciteA\{key\}Abbreviated author list.?\
\\shortciteN\{key\}Abbreviated author list and year.?\
\\citeyear\{key\} Cite year only. (1953)\
All the above have anNPvariant without parentheses; Ex.\
\\citeNP.\
```\
### BibTEXentry types\
\
```\
@article Journal or magazine article.\
@book Book with publisher.\
@booklet Book without publisher.\
@conference Article in conference proceedings.\
@inbook A part of a book and/or range of pages.\
@incollection A part of book with its own title.\
@misc If nothing else fits.\
@phdthesis PhD. thesis.\
@proceedings Proceedings of a conference.\
@techreport Tech report, usually numbered in series.\
@unpublished Unpublished.\
```\
### BibTEXfields\
\
```\
address Address of publisher. Not necessary for major\
publishers.\
author Names of authors, of format ....\
booktitle Title of book when part of it is cited.\
chapter Chapter or section number.\
edition Edition of a book.\
editor Names of editors.\
institution Sponsoring institution of tech. report.\
journal Journal name.\
key Used for cross ref. when no author.\
month Month published. Use 3-letter abbreviation.\
note Any additional information.\
number Number of journal or magazine.\
organizationOrganization that sponsors a conference.\
pages Page range (2,6,9--12).\
publisher Publisher\'92s name.\
school Name of school (for thesis).\
series Name of series of books.\
title Title of work.\
type Type of tech. report, ex. \'93Research Note\'94.\
volume Volume of a journal or book.\
year Year of publication.\
Not all fields need to be filled. See example below.\
```\
### CommonBibTEXstyle files\
\
```\
abbrv Standard abstract alphawith abstract\
alpha Standard apa APA\
plain Standard unsrt Unsorted\
```\
```\
The LATEX document should have the following two lines just\
before\\end\{document\}, wherebibfile.bibis the name of the\
BibTEX file.\
```\
```\
\\bibliographystyle\{plain\}\
\\bibliography\{bibfile\}\
```\
### BibTEXexample\
\
```\
The BibTEX database goes in a file calledfile.bib, which is\
processed withbibtex file.\
```\
```\
@String\{N = \{Na\\-ture\}\}\
@Article\{WC:1953,\
author = \{James Watson and Francis Crick\},\
title = \{A structure for Deoxyribose Nucleic Acid\},\
journal = N,\
volume = \{171\},\
pages = \{737\},\
year = 1953\
\}\
```\
## Sample LATEX document\
\
```\
\\documentclass[11pt]\{article\}\
\\usepackage\{fullpage\}\
\\title\{Template\}\
\\author\{Name\}\
\\begin\{document\}\
\\maketitle\
```\
```\
\\section\{section\}\
\\subsection*\{subsection without number\}\
text \\textbf\{bold text\} text. Some math: $2+2=5$\
\\subsection\{subsection\}\
text \\emph\{emphasized text\} text. \\cite\{WC:1953\}\
discovered the structure of DNA.\
```\
```\
A table:\
\\begin\{table\}[!th]\
\\begin\{tabular\}\{|l|c|r|\}\
\\hline\
first & row & data \\\\\
second & row & data \\\\\
\\hline\
\\end\{tabular\}\
\\caption\{This is the caption\}\
\\label\{ex:table\}\
\\end\{table\}\
```\
```\
The table is numbered \\ref\{ex:table\}.\
\\end\{document\}\
```\
```\
Copyright\'a9c2014 Winston Chang\
http://wch.github.io/latexsheet/\
```\
\
}