# HelloWorld
Learning Git


# Markdown
A markdown example shows how to write a markdown file. This document integrates core syntax and extensions (GMF).

* [Block Elements](#block-elements)
  * [Paragraphs and Line Breaks](#paragraphs-and-line-breaks)
  * [Headers](#headers)
  * [Blockquotes](#blockquotes)
  * [Lists](#lists)
  * [Code Blocks](#code-blocks)
  * [Horizontal Rules](#horizontal-rules)
  * [Table](#table)
* [Span Elements](#span-elements)
  * [Links](#links)
  * [Emphasis](#emphasis)
  * [Code](#code)
  * [Images](#images)
  * [Strikethrough](#strikethrough)
* [Miscellaneous](#miscellaneous)
  * [Automatic Links](#automatic-links)
  * [Backslash Escapes](#backslash-escapes)
* [Inline HTML](#inline-html)

## Block Elements
### Paragraphs and Line Breaks
#### Paragraphs
HTML Tag: `<p>`

One or more blank lines. (A blank line is a line containing nothing but **spaces** or **tabs** is considered blank.)

Code:

    This will be 
    inline.
    
    This is second paragraph.
Preview:
***
This will be 
inline.

This is second paragraph.
***
#### Line Breaks
HTML Tag: `<br />`

End a line with **two or more spaces**.

Code:

    This will be not  
    inline.
Preview:
***
This will be not  
inline.
***

### Headers
Markdown supports two styles of headers, Setext and atx.
#### Setext
HTML Tags: `<h1>`, `<h2>`

“Underlined” using **equal signs (=)** as `<h1>` and **dashes (-)** as `<h2>` in any number.

Code:

    This is an H1
    =============
    This is an H2
    -------------
Preview:
***
This is an H1
=============

This is an H2
-------------
***
#### atx
HTML Tags: `<h1>`, `<h2>`, `<h3>`, `<h4>`, `<h5>`, `<h6>`

Uses 1-6 **hash characters (#)** at the start of the line, corresponding to `<h1>` - `<h6>`.

Code:

    # This is an H1
    ## This is an H2
    ###### This is an H6
Preview:
***
# This is an H1
## This is an H2
###### This is an H6
***
Optionally, you may “close” atx-style headers. The closing hashes **don’t need to match** the number of hashes used to open the header.

Code:

    # This is an H1 #
    ## This is an H2 ##
    ### This is an H3 ######
Preview:
***
# This is an H1 #
## This is an H2 ##
### This is an H3 ######
***

### Blockquotes
HTML Tag: `<blockquote>`

Markdown uses email-style **>** characters for blockquoting. It looks best if you hard wrap the text and put a > before every line.

Code:

    > This is a blockquote with two paragraphs. Lorem ipsum dolor sit amet,
    > consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus.
    > Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus.
    > 
    > Donec sit amet nisl. Aliquam semper ipsum sit amet velit. Suspendisse
    > id sem consectetuer libero luctus adipiscing.
Preview:
***
> This is a blockquote with two paragraphs. Lorem ipsum dolor sit amet,
> consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus.
> Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus.
> 
> Donec sit amet nisl. Aliquam semper ipsum sit amet velit. Suspendisse
> id sem consectetuer libero luctus adipiscing.

***
Markdown allows you to be lazy and only put the > before the first line of a hard-wrapped paragraph.

Code:

    > This is a blockquote with two paragraphs. Lorem ipsum dolor sit amet,
    consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus.
    Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus.
    
    > Donec sit amet nisl. Aliquam semper ipsum sit amet velit. Suspendisse
    id sem consectetuer libero luctus adipiscing.
Preview:
***
> This is a blockquote with two paragraphs. Lorem ipsum dolor sit amet,
consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus.
Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus.

> Donec sit amet nisl. Aliquam semper ipsum sit amet velit. Suspendisse
id sem consectetuer libero luctus adipiscing.

***
Blockquotes can be nested (i.e. a blockquote-in-a-blockquote) by adding additional levels of >.

Code:

    > This is the first level of quoting.
    >
    > > This is nested blockquote.
    >
    > Back to the first level.
Preview:
***
> This is the first level of quoting.
>
> > This is nested blockquote.
>
> Back to the first level.

***
Blockquotes can contain other Markdown elements, including headers, lists, and code blocks.

Code:

    > ## This is a header.
    > 
    > 1.   This is the first list item.
    > 2.   This is the second list item.
    > 
    > Here's some example code:
    > 
    >     return shell_exec("echo $input | $markdown_script");
Preview:
***
> ## This is a header.
> 
> 1.   This is the first list item.
> 2.   This is the second list item.
> 
> Here's some example code:
> 
>     return shell_exec("echo $input | $markdown_script");

***

### Lists
Markdown supports ordered (numbered) and unordered (bulleted) lists.
#### Unordered
HTML Tag: `<ul>`

Unordered lists use **asterisks (*)**, **pluses (+)**, and **hyphens (-)**.

Code:

    *   Red
    *   Green
    *   Blue
Preview:
***
*   Red
*   Green
*   Blue

***
is equivalent to:

Code:

    +   Red
    +   Green
    +   Blue
and:

Code:

    -   Red
    -   Green
    -   Blue
#### Ordered
HTML Tag: `<ol>`

Ordered lists use numbers followed by periods:

Code:

    1.  Bird
    2.  McHale
    3.  Parish
Preview:
***
1.  Bird
2.  McHale
3.  Parish

***
It’s possible to trigger an ordered list by accident, by writing something like this:

Code:

    1986. What a great season.
Preview:
***
1986. What a great season.

***
You can **backslash-escape (\\)** the period:

Code:

    1986\. What a great season.
Preview:
***
1986\. What a great season.

***
#### Indented

##### Blockquote
To put a blockquote within a list item, the blockquote’s > delimiters need to be indented:

Code:

    *   A list item with a blockquote:

        > This is a blockquote
        > inside a list item.
Preview:
***
*   A list item with a blockquote:

    > This is a blockquote
    > inside a list item.

***
##### Code Block
To put a code block within a list item, the code block needs to be indented twice — **8 spaces** or **two tabs**:

Code:

    *   A list item with a code block:

            <code goes here>
Preview:
***
*   A list item with a code block:

        <code goes here>

***
##### Nested List
Code:

    * A
      * A1
      * A2
    * B
    * C
Preview:
***
* A
  * A1
  * A2
* B
* C

***
### Code Blocks
HTML Tag: `<pre>`

Indent every line of the block by at least **4 spaces** or **1 tab**.

Code:

    This is a normal paragraph:

        This is a code block.
Preview:
***
This is a normal paragraph:

    This is a code block.
***
A code block continues until it reaches a line that is not indented (or the end of the article).

Within a code block, ***ampersands (&)*** and angle **brackets (< and >)** are automatically converted into HTML entities.

Code:

        <div class="footer">
            &copy; 2004 Foo Corporation
        </div>
Preview:
***
    <div class="footer">
        &copy; 2004 Foo Corporation
    </div>
***
Following sections Fenced Code Blocks and Syntax Highlighting are extensions, you can use the other way to write the code block.
#### Fenced Code Blocks
Just wrap your code in ```` ``` ```` (as shown below) and you won't need to indent it by four spaces.

Code:

    Here's an example:

    ```
    function test() {
      console.log("notice the blank line before this function?");
    }
    ```
Preview:
***
Here's an example:

```
function test() {
  console.log("notice the blank line before this function?");
}
```
***
#### Syntax Highlighting
In your fenced block, add an optional language identifier and we'll run it through syntax highlighting ([Support Languages](https://github.com/github/linguist/blob/master/lib/linguist/languages.yml)).

Code:

    ```ruby
    require 'redcarpet'
    markdown = Redcarpet.new("Hello World!")
    puts markdown.to_html
    ```
Preview:
***
```ruby
require 'redcarpet'
markdown = Redcarpet.new("Hello World!")
puts markdown.to_html
```
***
### Horizontal Rules
HTML Tag: `<hr />`
Places **three or more hyphens (-), asterisks (*), or underscores (_)** on a line by themselves. You may use spaces between the hyphens or asterisks.

Code:

    * * *
    ***
    *****
    - - -
    ---------------------------------------
    ___
Preview:
***
* * *
***
*****
- - -
---------------------------------------
___
***
### Table
HTML Tag: `<table>`

It's an extension.

Separates column by **pipe (|)** and header by **dashes (-)**, and uses **colon (:)** for alignment.

The outer **pipes (|)** and alignment are optional. There are **3 delimiters** each cell at least for separating header.

Code:
```
| Left | Center | Right |
|:-----|:------:|------:|
|aaa   |bbb     |ccc    |
|ddd   |eee     |fff    |

 A | B 
---|---
123|456


A |B 
--|--
12|45
```
Preview:
***
| Left | Center | Right |
|:-----|:------:|------:|
|aaa   |bbb     |ccc    |
|ddd   |eee     |fff    |

 A | B 
---|---
123|456

A |B 
--|--
12|45
***
## Span Elements
### Links
HTML Tag: `<a>`

Markdown supports two style of links: inline and reference.

#### Inline
Inline link format like this: `[Link Text](URL "Title")`

Title is optional.

Code:

    This is [an example](http://example.com/ "Title") inline link.
    
    [This link](http://example.net/) has no title attribute.
Preview:
***
This is [an example](http://example.com/ "Title") inline link.

[This link](http://example.net/) has no title attribute.
***
If you’re referring to a local resource on the same server, you can use relative paths:

Code:

    See my [About](/about/) page for details. 
Preview:
***
See my [About](/about/) page for details. 
***
#### Reference
You could predefine link references. Format like this: `[id]: URL "Title"`

Title is also optional. And the you refer the link, format like this: `[Link Text][id]`

Code:

    [id]: http://example.com/  "Optional Title Here"
    This is [an example][id] reference-style link.
Preview:
***
[id]: http://example.com/  "Optional Title Here"
This is [an example][id] reference-style link.
***
That is:

* Square brackets containing the link identifier (**not case sensitive**, optionally indented from the left margin using up to three spaces);
* followed by a colon;
* followed by one or more spaces (or tabs);
* followed by the URL for the link;
* The link URL may, optionally, be surrounded by angle brackets.
* optionally followed by a title attribute for the link, enclosed in double or single quotes, or enclosed in parentheses.

The following three link definitions are equivalent:

Code:

    [foo]: http://example.com/  "Optional Title Here"
    [foo]: http://example.com/  'Optional Title Here'
    [foo]: http://example.com/  (Optional Title Here)
    [foo]: <http://example.com/>  "Optional Title Here"
Uses an empty set of square brackets, the link text itself is used as the name.

Code:

    [Google]: http://google.com/
    [Google][]
Preview:
***
[Google]: http://google.com/
[Google][]
***
### Emphasis
HTML Tags: `<em>`, `<strong>`

Markdown treats **asterisks (*)** and **underscores (_)** as indicators of emphasis. **One delimiter** will be  `<em>`; **double delimiters* will be `<strong>`.

Code:

    *single asterisks*

    _single underscores_

    **double asterisks**

    __double underscores__
Preview:
***
*single asterisks*

_single underscores_

**double asterisks**

__double underscores__
***
But if you surround an * or _ with spaces, it’ll be treated as a literal asterisk or underscore.

You can backslash escape it:

Code:

    \*this text is surrounded by literal asterisks\*
Preview:
***
\*this text is surrounded by literal asterisks\*
***
### Code
HTML Tag: `<code>`

Wraps it with **backtick quotes (`)**.

Code:

    Use the `printf()` function.
Preview:
***
Use the `printf()` function.
***
To include a literal backtick character within a code span, you can use **multiple backticks** as the opening and closing delimiters:

Code:

    ``There is a literal backtick (`) here.``
Preview:
***
``There is a literal backtick (`) here.``
***
The backtick delimiters surrounding a code span may include spaces — one after the opening, one before the closing. This allows you to place literal backtick characters at the beginning or end of a code span:

Code:

    A single backtick in a code span: `` ` ``

    A backtick-delimited string in a code span: `` `foo` ``
Preview:
***
A single backtick in a code span: `` ` ``

A backtick-delimited string in a code span: `` `foo` ``
***
### Images
HTML Tag: `<img />`

Markdown uses an image syntax that is intended to resemble the syntax for links, allowing for two styles: inline and reference.
#### Inline

Inline image syntax looks like this: `![Alt text](URL "Title")`

Title is optional.

Code:

    ![Alt text](/path/to/img.jpg)

    ![Alt text](/path/to/img.jpg "Optional title")
Preview:
***
![Alt text](/path/to/img.jpg)

![Alt text](/path/to/img.jpg "Optional title")
***
That is:

* An exclamation mark: !;
* followed by a set of square brackets, containing the alt attribute text for the image;
* followed by a set of parentheses, containing the URL or path to the image, and an optional title attribute enclosed in double or single quotes.

#### Reference
Reference-style image syntax looks like this: `![Alt text][id]`

Code:

    [img id]: url/to/image  "Optional title attribute"
    ![Alt text][img id]
Preview:
***
[img id]: url/to/image  "Optional title attribute"
![Alt text][img id]
***
### Strikethrough
HTML Tag: `<del>`

It's an extension.

GFM adds syntax to strikethrough text.

Code:
```
~~Mistaken text.~~
```
Preview:
***
~~Mistaken text.~~
***
## Miscellaneous
### Automatic Links
Markdown supports a shortcut style for creating “automatic” links for URLs and email addresses: simply surround the URL or email address with angle brackets. 

Code:

    <http://example.com/>
    
    <address@example.com>
Preview:
***
<http://example.com/>

<address@example.com>
***
GFM will autolink standard URLs.

Code:
```
https://github.com/emn178/markdown
```
Preview:
***
https://github.com/emn178/markdown
***

### Backslash Escapes
Markdown allows you to use backslash escapes to generate literal characters which would otherwise have special meaning in Markdown’s formatting syntax.

Code:

    \*literal asterisks\*
Preview:
***
\*literal asterisks\*
***
Markdown provides backslash escapes for the following characters:

Code:

    \   backslash
    `   backtick
    *   asterisk
    _   underscore
    {}  curly braces
    []  square brackets
    ()  parentheses
    #   hash mark
    +   plus sign
    -   minus sign (hyphen)
    .   dot
    !   exclamation mark

## Inline HTML
For any markup that is not covered by Markdown’s syntax, you simply use HTML itself. There’s no need to preface it or delimit it to indicate that you’re switching from Markdown to HTML; you just use the tags.

Code:

    This is a regular paragraph.

    <table>
        <tr>
            <td>Foo</td>
        </tr>
    </table>

    This is another regular paragraph.
Preview:
***
This is a regular paragraph.

<table>
    <tr>
        <td>Foo</td>
    </tr>
</table>

This is another regular paragraph.
***
Note that Markdown formatting syntax is **not processed within block-level HTML tags**. 

Unlike block-level HTML tags, Markdown syntax is **processed within span-level tags**.

Code:

    <span>**Work**</span>
    
    <div>
        **No Work**
    </div>
Preview:
***
<span>**Work**</span>

<div>
  **No Work**
</div>
***












### My Other Resource Lists

### My Other Resource Lists

### My Other Resource Lists

### My Other Resource Lists

### My Other Resource Lists

* *[Web Development Study Resources](https://github.com/dargaCode/WebDevStudyResources/blob/master/README.md)*
* *[Logic and Coding Games](https://github.com/dargaCode/LogicAndCodingGames)*

# Portfolio Examples

I wanted to absorb a lot of different portfolio sites before I started working on my own. 

Most of these were dug up on reddit. Some have things I really like and want to emulate, some have things I want to avoid, and a lot have some of both. 

I also found a thread with [lots of great portfolio advice](https://www.reddit.com/r/webdev/comments/1nzzsn/cant_make_a_portfolio/). 

# Contributing

Feel free to add more (in alphabetical order), or remove yours if you'd rather not have it here. 

Please follow the existing format.

# Highlights

Here are some that I like, whether it be their overall design, the colors, or just a small UX touch. 

1. [abbyhubbard.design](http://abbyhubbard.design)
1. **[briandelaney.com](http://briandelaney.com)** - Single-page design with great UX
1. [bree-eros.github.io](http://bree-eros.github.io)
1. **[cameronaskin.info](http://cameronaskin.info)** - Polished single-page design
1. [codepen.io/ketnelson](http://codepen.io/ketnelson/full/LNjLVW) - Nice colors & blurred backgrounds
1. [codepen.io/oneate7](http://codepen.io/oneate7/full/qdGprg) - Icons for each project
1. [coryhughart.com](http://coryhughart.com) - Nice style and art
1. **[courtneysgamecoderocks.com](http://courtneysgamecoderocks.com/)** - Great polish and energy
1. [desandro.com](http://desandro.com/)
1. **[felixsun.me](http://felixsun.me)** - Nice cover animation
1. **[guglieri.com](http://guglieri.com)** - Very polished single-page design
1. [hanno.co](http://hanno.co)
1. [ivesvh.com](http://ivesvh.com) - Lots of animation
1. [joma-web-schmie.de](http://joma-web-schmie.de)
1. [joshkissel.com](http://joshkissel.com)
1. [justingillespie.com](http://justingillespie.com)
1. [kevinpamaran.com](http://kevinpamaran.com/) - Nice cover
1. [manparvesh.github.io](http://manparvesh.github.io/)
1. [marcuseisele.com](http://marcuseisele.com)
1. [michaelpumo.com](http://michaelpumo.com/) - Nice cover
1. [nanja.space](http://nanja.space) - Playful animations
1. [ruigomes.me](http://ruigomes.me)
1. [sambedingfield.com](http://sambedingfield.com) - Nice art
1. [shaykyasin.github.io](http://shaykyasin.github.io) - Nice cover page & colors
1. **[strml.net](http://strml.net)** - Animated page "codes itself"

# The Whole List

1. [aaronholmes.net](http://aaronholmes.net)
1. [abbyhubbard.design](http://abbyhubbard.design)
1. [acko.net](http://acko.net)
1. [adrianratajczak.work](http://adrianratajczak.work)
1. [adrianrivers.github.io](https://adrianrivers.github.io)
1. [alonso.codes](http://alonso.codes)
1. [amateurgeek.com](http://amateurgeek.com)
1. [andyhau.com](http://andyhau.com)
1. [applid.com](http://applid.com)
1. [aprilzero.com](http://aprilzero.com)
1. [aquaticgorilla.com](http://aquaticgorilla.com)
1. [arianv.com](http://arianv.com)
1. [austindev.me](http://austindev.me)
1. [barneycarroll.com](http://barneycarroll.com)
1. [benadam.me](http://benadam.me)
1. [billypurvis.co.uk](http://billypurvis.co.uk)
1. [blog.andyjiang.com](http://blog.andyjiang.com/)
1. [brandondail.me](http://brandondail.me)
1. [brandonjyuhas.me](http://brandonjyuhas.me)
1. [bree-eros.github.io](http://bree-eros.github.io)
1. [briandelaney.com](http://briandelaney.com)
1. [byronsadik.com](http://byronsadik.com)
1. [cabbi.bo](http://cabbi.bo/)
1. [callmenick.com](http://callmenick.com)
1. [cameronaskin.info](http://cameronaskin.info)
1. [chrispederick.com](http://chrispederick.com)
1. [chrzanowski.github.io](http://chrzanowski.github.io)
1. [codepen.io/axelf/full/jqgMJa](http://codepen.io/axelf/full/jqgMJa)
1. [codepen.io/coreywhite](http://codepen.io/coreywhite/full/vNovYY)
1. [codepen.io/Dwayneabutcher](http://codepen.io/Dwayneabutcher/full/mPMrQJ)
1. [codepen.io/eddyerburgh](http://codepen.io/eddyerburgh/full/oxwXjx)
1. [codepen.io/Gatz12](http://codepen.io/Gatz12/full/aNyaXQ)
1. [codepen.io/gazzer82](http://codepen.io/gazzer82/full/gpVQQd)
1. [codepen.io/golle404](http://codepen.io/golle404/full/vNoxzg)
1. [codepen.io/gry0](http://codepen.io/gry0/full/zqxZve)
1. [codepen.io/hash004](http://codepen.io/hash004/full/dMydYZ)
1. [codepen.io/JackBid](http://codepen.io/JackBid/full/rVgXep)
1. [codepen.io/jessawright](http://codepen.io/jessawright/full/JXXEpE)
1. [codepen.io/jpetersen00](http://codepen.io/jpetersen00/full/PzowWg)
1. [codepen.io/ketnelson](http://codepen.io/ketnelson/full/LNjLVW)
1. [codepen.io/LubaMay](http://codepen.io/LubaMay/full/YqZRWd)
1. [codepen.io/luomint](http://codepen.io/luomint/full/Kdgqjp)
1. [codepen.io/lveent](http://codepen.io/lveent/full/gaZyaq)
1. [codepen.io/merraysy](http://codepen.io/merraysy/full/KzpwJG)
1. [codepen.io/npatrick96](http://codepen.io/npatrick96/full/pyagBJ)
1. [codepen.io/oneate7](http://codepen.io/oneate7/full/qdGprg)
1. [codepen.io/rflvrl](http://codepen.io/rflvrl/full/dMygzd)
1. [codepen.io/ScoHa](http://codepen.io/ScoHa/full/OXJEPV)
1. [codepen.io/sjmercier](http://codepen.io/sjmercier/full/WwpENZ)
1. [codepen.io/thepeted](http://codepen.io/thepeted/full/LpPWWQ)
1. [codepen.io/varunm22](http://codepen.io/varunm22/full/jbomxr)
1. [codepen.io/zachn1700](http://codepen.io/zachn1700/full/yOpPYE)
1. [colbydude.com](http://colbydude.com)
1. [coryhughart.com](http://coryhughart.com)
1. [corynorris.me](http://corynorris.me)
1. [courtneysgamecoderocks.com](http://courtneysgamecoderocks.com/)
1. [crmpicco.co.uk](http://crmpicco.co.uk)
1. [daman2408.github.io/my-portfolio](http://daman2408.github.io/my-portfolio)
1. [damianschwyrz.de](http://damianschwyrz.de)
1. [dangoodspeed.com](http://dangoodspeed.com/)
1. [danielstrong.io](http://danielstrong.io)
1. [dentefederico.altervista.org](http://dentefederico.altervista.org)
1. [derekknox.com](http://derekknox.com)
1. [desandro.com](http://desandro.com/)
1. [dividedzero.com](http://dividedzero.com)
1. [donaldcameron77.info](http://donaldcameron77.info)
1. [drewbarontini.com](http://drewbarontini.com/)
1. [drewrawitz.com](http://drewrawitz.com)
1. [eina.ca](http://eina.ca)
1. [ekstrakt.mk](http://ekstrakt.mk)
1. [elliotforbes.co.uk](http://elliotforbes.co.uk)
1. [en.nicolasbouliane.com](http://en.nicolasbouliane.com)
1. [evanyou.me](http://evanyou.me/)
1. [felixsun.me](http://felixsun.me)
1. [fourtonfish.com](http://fourtonfish.com)
1. [furycodes.com](http://furycodes.com)
1. [giorgiodelgado.ca](http://giorgiodelgado.ca)
1. [glebbahmutov.com](https://glebbahmutov.com/)
1. [gregdizzia.com](http://gregdizzia.com)
1. [guglieri.com](http://guglieri.com)
1. [hanno.co](http://hanno.co)
1. [helgesverre.com](http://helgesverre.com)
1. [hrek.me](http://hrek.me)
1. [ignaciorivas.me](http://ignaciorivas.me)
1. [igvita.com](http://igvita.com)
1. [ivesvh.com](http://ivesvh.com)
1. [j-w-v.com](http://www.j-w-v.com/)
1. [jakereynolds.co](http://jakereynolds.co)
1. [jasonhee.com](http://jasonhee.com)
1. [jasonlydon.com](http://jasonlydon.com)
1. [javier.xyz](http://javier.xyz/)
1. [jennifer-nguyen.ca](http://jennifer-nguyen.ca)
1. [jgefroh.com](http://jgefroh.com/)
1. [jimmybweb.com](http://jimmybweb.com)
1. [jimmyjia.me](http://jimmyjia.me)
1. [joa-ebert.com](http://joa-ebert.com)
1. [joelglovier.com](http://joelglovier.com)
1. [joelgriffith.net](http://joelgriffith.net)
1. [joepichardo.com](http://joepichardo.com)
1. [joma-web-schmie.de](http://joma-web-schmie.de)
1. [josegarrido.me](http://josegarrido.me)
1. [joshkissel.com](http://joshkissel.com)
1. [justingillespie.com](http://justingillespie.com)
1. [justinwhite.co](http://justinwhite.co)
1. [kbrgl.github.io](http://kbrgl.github.io)
1. [keats.me](http://keats.me)
1. [keithclark.co.uk](http://keithclark.co.uk)
1. [kemdu.lt](http://kemdu.lt)
1. [kevinpamaran.com](http://kevinpamaran.com/)
1. [kylebelanger.com](http://kylebelanger.com)
1. [liviucmg.com](http://liviucmg.com)
1. [lukemichaels.herokuapp.com](http://lukemichaels.herokuapp.com)
1. [luketwomey.com](http://luketwomey.com)
1. [maciejczyzewski.me](http://maciejczyzewski.me)
1. [mackenziechild.me](https://mackenziechild.me/)
1. [manparvesh.github.io](http://manparvesh.github.io/)
1. [marcuseisele.com](http://marcuseisele.com)
1. [markjaquith.com](http://markjaquith.com/)
1. [matthewcorway.com](http://matthewcorway.com)
1. [matthewross.me](http://matthewross.me)
1. [mauriceprosper.com](http://mauriceprosper.com)
1. [maxlaumeister.com](http://maxlaumeister.com)
1. [me.jdf2.org](http://me.jdf2.org)
1. [mediaworks.cz](http://mediaworks.cz)
1. [michaelcharl.es/aubrey](http://michaelcharl.es/aubrey)
1. [michaelfogleman.com](https://www.michaelfogleman.com/)
1. [michaelpumo.com](http://michaelpumo.com/)
1. [mollyjameson.com](http://mollyjameson.com)
1. [nanja.space](http://nanja.space)
1. [nateberkopec.com](http://nateberkopec.com)
1. [nicholashorn.com](http://nicholashorn.com)
1. [nickfletchr.com](http://nickfletchr.com)
1. [nickstewart.me](http://nickstewart.me)
1. [nobigthings.com](http://nobigthings.com)
1. [oliver.codes](http://oliver.codes)
1. [onether.com](http://onether.com)
1. [paulkmiller.com](http://paulkmiller.com)
1. [probably.ninja](http://probably.ninja/)
1. [richardhessler.com](http://richardhessler.com)
1. [ruigomes.me](http://ruigomes.me)
1. [ryan.mcgeary.org](http://ryan.mcgeary.org/)
1. [ryantaylordev.ca](http://ryantaylordev.ca)
1. [ryanvando.bitballoon.com](http://ryanvando.bitballoon.com)
1. [ryanyurkan.in](http://ryanyurkan.in)
1. [saijogeorge.com](http://saijogeorge.com)
1. [sambedingfield.com](http://sambedingfield.com)
1. [seanloyless.info](http://seanloyless.info)
1. [seanmccaffery.net](http://seanmccaffery.net)
1. [shaykyasin.github.io](http://shaykyasin.github.io)
1. [skylerhartle.com](http://skylerhartle.com)
1. [sohweb.co.uk](http://sohweb.co.uk)
1. [strml.net](http://strml.net)
1. [substack.net](http://substack.net)
1. [suhyunpak.com](http://www.suhyunpak.com)
1. [syropia.net](http://syropia.net)
1. [t-cote.ca](http://t-cote.ca)
1. [tarangagarwalla.com](http://tarangagarwalla.com/)
1. [tanmayshankar.weebly.com](http://tanmayshankar.weebly.com/)
1. [theelisabeth.com](http://theelisabeth.com)
1. [thiagobelem.net](http://thiagobelem.net)
1. [thojad.github.io/ClintonVilla](http://thojad.github.io/ClintonVilla)
1. [timmyomahony.com](http://timmyomahony.com)
1. [travisneilson.com](http://travisneilson.com)
1. [willcmcc.com](http://willcmcc.com)
1. [xstoryteller.com](http://xstoryteller.com)
1. [zachhoefler.com](http://zachhoefler.com)
1. [zachsaucier.com](http://zachsaucier.com)
1. [zerazera.github.io](http://zerazera.github.io)
1. [zertukis.com](http://zertukis.com)

