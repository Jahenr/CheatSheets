## LATEX 2εCheat Sheet

## Document classes

book Default is two-sided.
report No\partdivisions.
article No\partor\chapterdivisions.
letter Letter (?).
slides Large sans-serif font.
Used at the very beginning of a document:
\documentclass{class}. Use\begin{document}to start
contents and\end{document}to end the document.

### Commondocumentclassoptions

10pt/11pt/12pt Font size.
letterpaper/a4paperPaper size.
twocolumn Use two columns.
twoside Set margins for two-sided.
landscape Landscape orientation. Must usedvips
-t landscape.
draft Double-space lines.
Usage:\documentclass[opt,opt]{class}.

### Packages

fullpageUse 1 inch margins.
anysize Set margins:\marginsize{l}{r}{t}{b}.
multicolUsencolumns:\begin{multicols}{n}.
latexsymUse LATEX symbol font.
graphicxShow image:\includegraphics[width=x]{file}.
url Insert URL:\url{http://.. .}.
Use before\begin{document}. Usage:\usepackage{package}

### Title

\author{text} Author of document.
\title{text} Title of document.
\date{text} Date.
These commands go before\begin{document}. The
declaration\maketitlegoes at the top of the document.

### Miscellaneous

\pagestyle{empty}Empty header, footer and no page num-
bers.
\tableofcontents Add a table of contents here.

## Document structure

\part{title}
\chapter{title}
\section{title}
\subsection{title}

```
\subsubsection{title}
\paragraph{title}
\subparagraph{title}
```
Use\setcounter{secnumdepth}{x}suppresses heading
numbers of depth> x, wherechapterhas depth 0. Use a*, as
in\section*{title}, to not number a particular item—these
items will also not appear in the table of contents.

### Text environments

\begin{comment} Comment (not printed). Requiresverbatim
package.
\begin{quote} Indented quotation block.
\begin{quotation}Likequotewith indented paragraphs.
\begin{verse} Quotation block for verse.

### Lists

```
\begin{enumerate} Numbered list.
\begin{itemize} Bulleted list.
\begin{description}Description list.
\itemtext Add an item.
\item[x]text Usexinstead of normal bullet or number.
Required for descriptions.
```
### References

```
\label{marker} Set a marker for cross-reference, often of the
form\label{sec:item}.
\ref{marker} Give section/body number of marker.
\pageref{marker}Give page number of marker.
\footnote{text} Print footnote at bottom of page.
```
### Floating bodies

```
\begin{table}[place] Add numbered table.
\begin{figure}[place] Add numbered figure.
\begin{equation}[place]Add numbered equation.
\caption{text} Caption for the body.
Theplaceis a list valid placements for the body.t=top,
h=here,b=bottom,p=separate page,!=place even if ugly.
Captions and label markers should be within the environment.
```
## Text properties

### Font face

```
Command Declaration Effect
\textrm{text} {\rmfamilytext} Roman family
\textsf{text} {\sffamilytext} Sans serif family
\texttt{text} {\ttfamilytext} Typewriter family
\textmd{text} {\mdseriestext} Medium series
\textbf{text} {\bfseriestext} Bold series
\textup{text} {\upshapetext} Upright shape
\textit{text} {\itshapetext} Italic shape
\textsl{text} {\slshapetext} Slanted shape
\textsc{text} {\scshapetext} Small Caps shape
\emph{text} {\emtext} Emphasized
\textnormal{text}{\normalfonttext}Document font
\underline{text} Underline
The command (tttt) form handles spacing better than the
declaration (tttt) form.
```
### Font size

```
\tiny tiny
\scriptsize scriptsize
\footnotesizefootnotesize
```
#### \small small

### \normalsize normalsize

## \large large

## \LargeLarge

## \LARGELARGE

## \huge huge

# \Huge Huge

```
These are declarations and should be used in the form{\small
```
.. .}, or without braces to affect the entire document.

### Verbatim text

```
\begin{verbatim} Verbatim environment.
\begin{verbatim*}Spaces are shown as.
\verb!text! Text between the delimiting characters (in
this case ‘!’) is verbatim.
```
### Justification

```
Environment Declaration
\begin{center} \centering
\begin{flushleft} \raggedright
\begin{flushright} \raggedleft
```
### Miscellaneous

```
\linespread{x}changes the line spacing by the multiplierx.
```
## Text-mode symbols

### Symbols

```
& \& \_... \ldots • \textbullet
$ \$ ˆ \^{} | \textbar \ \textbackslash
% \% ̃ \~{} # \# § \S
```
### Accents

```
`o \‘o ́o\’o ˆo \^o ̃o \~o ̄o\=o
̇o \.o ̈o\"o ̧o \c o ˇo \v o ̋o\H o
̧c \c c o. \d o o
̄
```
```
\b o oo\t oo œ\oe
Œ\OE æ\ae Æ\AE ̊a \aa ̊A\AA
ø \o Ø\O l \l L \L ı \i
 \j ¡ ~‘ ¿ ?‘
```
### Delimiters

```
‘‘ “‘‘ {\{ [[ (( <\textless
’’ ”’’ }\} ]] )) >\textgreater
```
### Dashes

```
Name Source Example Usage
hyphen - X-ray In words.
en-dash -- 1–5 Between numbers.
em-dash --- Yes—or no? Punctuation.
```
### Line and page breaks

```
\\ Begin new line without new paragraph.
\\* Prohibit pagebreak after linebreak.
\kill Don’t print current line.
\pagebreakStart new page.
\noindent Do not indent current line.
```
### Miscellaneous

```
\today March 28, 2017.
$\sim$ Prints∼instead of\~{}, which makes ̃.
~ Space, disallow linebreak (W.J.~Clinton).
\@. Indicate that the.ends a sentence when following
an uppercase letter.
\hspace{l} Horizontal space of lengthl(Ex:l=20pt).
\vspace{l} Vertical space of lengthl.
\rule{w}{h}Line of widthwand heighth.
```
## Tabular environments

### tabbingenvironment

```
\=Set tab stop. \> Go to tab stop.
Tab stops can be set on “invisible” lines with\killat the end
of the line. Normally\\is used to separate lines.
```

### tabularenvironment

\begin{array}[pos]{cols}
\begin{tabular}[pos]{cols}
\begin{tabular*}{width}[pos]{cols}

#### tabularcolumn specification

l Left-justified column.
c Centered column.
r Right-justified column.
p{width} Same as\parbox[t]{width}.
@{decl} Insertdeclinstead of inter-column space.
| Inserts a vertical line between columns.

#### tabularelements

\hline Horizontal line between rows.
\cline{x-y}Horizontal line across columnsxthroughy.
\multicolumn{n}{cols}{text}
A cell that spansncolumns, withcolscolumn
specification.

## Math mode

For inline math, use\(...\)or$...$. For displayed math,
use\[...\]or\begin{equation}.

Superscriptx ^{x} Subscriptx _{x}
x
y \frac{x}{y}

### ∑n

```
k=1 \sum_{k=1}^n
```
### n√x \sqrt[n]{x} ∏n

```
k=1 \prod_{k=1}^n
```
### Math-mode symbols

≤\leq ≥\geq 6 =\neq ≈ \approx
×\times ÷\div ±\pm · \cdot
◦ ^{\circ} ◦ \circ ′ \prime ···\cdots

∞\infty ¬\neg ∧\wedge ∨ \vee
⊃\supset ∀\forall ∈\in →\rightarrow
⊂\subset ∃\exists ∈/ \notin ⇒\Rightarrow
∪ \cup ∩\cap | \mid ⇔\Leftrightarrow
a ̇ \dot a ˆa \hat a ̄a \bar a ̃a \tilde a
α \alpha β\beta γ \gamma δ \delta
 \epsilon ζ \zeta η \eta ε \varepsilon
θ \theta ι \iota κ \kappa θ \vartheta
λ \lambda μ\mu ν \nu ξ \xi
π \pi ρ \rho σ \sigma τ \tau
υ \upsilon φ\phi χ \chi ψ \psi
ω \omega Γ\Gamma ∆\Delta Θ \Theta
Λ \Lambda Ξ\Xi Π\Pi Σ \Sigma
Υ\Upsilon Φ\Phi Ψ\Psi Ω \Omega

## Bibliography and citations

When using BibTEX, you need to runlatex,bibtex, and
latextwice more to resolve dependencies.

### Citation types

```
\cite{key} Full author list and year. (Watson and Crick
1953)
\citeA{key} Full author list. (Watson and Crick)
\citeN{key} Full author list and year. Watson and Crick
(1953)
\shortcite{key} Abbreviated author list and year.?
\shortciteA{key}Abbreviated author list.?
\shortciteN{key}Abbreviated author list and year.?
\citeyear{key} Cite year only. (1953)
All the above have anNPvariant without parentheses; Ex.
\citeNP.
```
### BibTEXentry types

```
@article Journal or magazine article.
@book Book with publisher.
@booklet Book without publisher.
@conference Article in conference proceedings.
@inbook A part of a book and/or range of pages.
@incollection A part of book with its own title.
@misc If nothing else fits.
@phdthesis PhD. thesis.
@proceedings Proceedings of a conference.
@techreport Tech report, usually numbered in series.
@unpublished Unpublished.
```
### BibTEXfields

```
address Address of publisher. Not necessary for major
publishers.
author Names of authors, of format ....
booktitle Title of book when part of it is cited.
chapter Chapter or section number.
edition Edition of a book.
editor Names of editors.
institution Sponsoring institution of tech. report.
journal Journal name.
key Used for cross ref. when no author.
month Month published. Use 3-letter abbreviation.
note Any additional information.
number Number of journal or magazine.
organizationOrganization that sponsors a conference.
pages Page range (2,6,9--12).
publisher Publisher’s name.
school Name of school (for thesis).
series Name of series of books.
title Title of work.
type Type of tech. report, ex. “Research Note”.
volume Volume of a journal or book.
year Year of publication.
Not all fields need to be filled. See example below.
```
### CommonBibTEXstyle files

```
abbrv Standard abstract alphawith abstract
alpha Standard apa APA
plain Standard unsrt Unsorted
```
```
The LATEX document should have the following two lines just
before\end{document}, wherebibfile.bibis the name of the
BibTEX file.
```
```
\bibliographystyle{plain}
\bibliography{bibfile}
```
### BibTEXexample

```
The BibTEX database goes in a file calledfile.bib, which is
processed withbibtex file.
```
```
@String{N = {Na\-ture}}
@Article{WC:1953,
author = {James Watson and Francis Crick},
title = {A structure for Deoxyribose Nucleic Acid},
journal = N,
volume = {171},
pages = {737},
year = 1953
}
```
## Sample LATEX document

```
\documentclass[11pt]{article}
\usepackage{fullpage}
\title{Template}
\author{Name}
\begin{document}
\maketitle
```
```
\section{section}
\subsection*{subsection without number}
text \textbf{bold text} text. Some math: $2+2=5$
\subsection{subsection}
text \emph{emphasized text} text. \cite{WC:1953}
discovered the structure of DNA.
```
```
A table:
\begin{table}[!th]
\begin{tabular}{|l|c|r|}
\hline
first & row & data \\
second & row & data \\
\hline
\end{tabular}
\caption{This is the caption}
\label{ex:table}
\end{table}
```
```
The table is numbered \ref{ex:table}.
\end{document}
```
```
Copyright©c2014 Winston Chang
http://wch.github.io/latexsheet/
```

