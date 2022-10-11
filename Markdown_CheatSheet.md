# MARKDOWN CHEATSHEET

# Headings

## Heading 1 
    ```
    # Heading 1 
    OR
    ============= (below H1 text)
    ```
Example:
# Heading text example
<br><br>

## Heading 2 ##
    ```
    ## Heading 2
    OR
    Markup: --------------- (below H2 text)
    ```
Example:
## Heading text example
<br><br>

## Heading 3
    ```
    ### Heading 3
    ```
Example:
### Heading text example
<br><br>

## Heading 4
    ```
    #### Heading 4
    ```
Example:
#### Heading text example
<br><br>


# Text Formating

## _Emphasized text_
    ```
    _Emphasized text_ or *Emphasized text*
    ```
Example:
_Heading text example_
or
*Heading text example*


## ~~Strikethrough text~~
    ```
    ~~Strikethrough text~~
    ```
Example:
~~Heading text example~~


## __Strong text__

    __Strong text__ or **Strong text**

Example:
**Heading text example**

## ___Strong emphasized text___

    ___Strong emphasized text___ or ***Strong emphasized text***

Example:
***Heading text example***

# Links

## Named Links

    [Named Link](http://www.google.fr/ "Named link title") and http://www.google.fr/ or <http://example.com/>

Example:
[Named Link](http://www.google.fr/ "Named link title") and http://www.google.fr/ or <http://example.com/>

## Section Links
    
    [heading-1](#heading-1 "Goto heading-1")

Example:
[heading-1](#heading-1 "Goto heading-1")


# Tables

## Simple Table

```
First Header  | Second Header
------------- | -------------
Content Cell  | Content Cell
Content Cell  | Content Cell
```

First Header  | Second Header
------------- | -------------
Content Cell  | Content Cell
Content Cell  | Content Cell


## Pipe devided Table
Adding a pipe `|` in a cell :

```
First Header  | Second Header
------------- | -------------
Content Cell  | Content Cell
Content Cell  |  \| 
```

First Header  | Second Header
------------- | -------------
Content Cell  | Content Cell
Content Cell  | \|

## Alignment in Table
Left, right and center aligned table

```
Left aligned Header | Right aligned Header | Center aligned Header
| :--- | ---: | :---:
Content Cell  | Content Cell | Content Cell
Content Cell  | Content Cell | Content Cell
```

Left aligned Header | Right aligned Header | Center aligned Header
| :--- | ---: | :---:
Content Cell  | Content Cell | Content Cell
Content Cell  | Content Cell | Content Cell

# Code

## single inverted Commas

    `code()`
`code()`

## Triple Inverted Commas

```javascript
code
```

```javascript
    var specificLanguage_code = 
    {
        "data": {
            "lookedUpPlatform": 1,
            "query": "Kasabian+Test+Transmission",
            "lookedUpItem": {
                "name": "Test Transmission",
                "artist": "Kasabian",
                "album": "Kasabian",
                "picture": null,
                "link": "http://open.spotify.com/track/5jhJur5n4fasblLSCOcrTp"
            }
        }
    }
```

# Lists Un-nested and Nested

## Unordered List
```
* Bullet list
    * Nested bullet
        * Sub-nested bullet etc
    * Bullet list item 2
OR
- Bullet list
    - Nested bullet
        - Sub-nested bullet etc
    - Bullet list item 2
``` 

Output:
* Bullet list
    * Nested bullet
        * Sub-nested bullet etc
* Bullet list item 2
<br>
- Bullet list
    - Nested bullet
        - Sub-nested bullet etc
    - Bullet list item 2 


## Ordered List

```
1. A numbered list
    1. A nested numbered list
    2. Which is numbered
2. Which is numbered
```

1. A numbered list
    1. A nested numbered list
    2. Which is numbered
2. Which is numbered

# Checkbox

```
 - [ ] An uncompleted task
 - [x] A completed task
```

Output:
- [ ] An uncompleted task
- [x] A completed task

## Subtasks - Nesting
```
- [ ] An uncompleted task
    - [ ] A subtask
```
Output:
- [ ] An uncompleted task
    - [ ] A subtask

# Quotations and Referancing

## Blockquote
```
> Blockquote
```
> Blockquote
<br><br>

## Nested Blockquote
```
>> Nested blockquote
    > Blockquote
    >> Nested Blockquote
```

## Horizontal Ray
```
_Horizontal line :_
```
_Horizontal line :_

```
- - - -
```

- - - -

# Images

_Image with alt :_

    ![picture alt](http://via.placeholder.com/200x150 "Title is optional")

Example:
![picture alt](http://via.placeholder.com/200x150 "Title is optional")


## Location Pointer
Link to a specific part of the page:
   
    [text goes here](#section_name)
         section_title<a name="section_name"></a>   

[Go To TOP](#TOP) 


# Hotkey:

`<kbd>` is keyboard input tag that can be used as:

```
<kbd>⌘F</kbd>
```
<kbd>⇧⌘F</kbd>

Hotkey list:

| Key | Symbol |
| --- | --- |
| Option | ⌥ |
| Control | ⌃ |
| Command | ⌘ |
| Shift | ⇧ |
| Caps Lock | ⇪ |
| Tab | ⇥ |
| Esc | ⎋ |
| Power | ⌽ |
| Return | ↩ |
| Delete | ⌫ |
| Up | ↑ |
| Down | ↓ |
| Left | ← |
| Right | → |

# Bonus:
## Emoji:

    Code appears between colons :EMOJICODE:

:exclamation: Use emoji icons to enhance text. :+1:  Look up emoji codes at [emoji-cheat-sheet.com](http://emoji-cheat-sheet.com/)

# HTML Code
The code stored in markdown can also be converted from an HTML file. for referance please view HTML Cheatsheet.
