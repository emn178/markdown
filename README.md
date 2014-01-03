# Markdown
This is a markdown example shows how to write a markdown file.

* [Block Elements](#block-elements)
  * [Paragraphs and Line Breaks](#paragraphs-and-line-breaks)
  * [Headers](#headers)
  * [Blockquotes](#blockquotes)
  * [Lists](#lists)
  * [Code Blocks](#code-blocks)
  * [Horizontal Rules](#horizontal-rules)
* [Inline Elements](#inline-elements)
  * [Links](#links)
  * [Emphasis](#emphasis)
  * [Code](#code)
  * [Images](#images)
* [Miscellaneous](#miscellaneous)
  * [Automatic Links](#automatic-links)
  * [Backslash Escapes](#backslash-escapes)

## Block Elements
### Paragraphs and Line Breaks
#### Paragraphs
A paragraph is simply one or more consecutive lines of text, separated by one or more blank lines. (A blank line is any line that looks like a blank line — a line containing nothing but spaces or tabs is considered blank.) Normal paragraphs should not be indented with spaces or tabs.

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
When you do want to insert a `<br />` break tag using Markdown, you end a line with two or more spaces, then type return.

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
Setext-style headers are “underlined” using equal signs (for first-level headers) and dashes (for second-level headers). 
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
Any number of underlining =’s or -’s will work.
#### atx
Atx-style headers use 1-6 hash characters at the start of the line, corresponding to header levels 1-6. 

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
Optionally, you may “close” atx-style headers. This is purely cosmetic — you can use this if you think it looks better. The closing hashes don’t even need to match the number of hashes used to open the header. (The number of opening hashes determines the header level.)

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
Markdown uses email-style > characters for blockquoting. If you’re familiar with quoting passages of text in an email message, then you know how to create a blockquote in Markdown. It looks best if you hard wrap the text and put a > before every line.

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
Unordered lists use asterisks, pluses, and hyphens — interchangably — as list markers.

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
Preview:
***
+   Red
+   Green
+   Blue

***
and:

Code:

    -   Red
    -   Green
    -   Blue
Preview:
***
-   Red
-   Green
-   Blue

***
#### Ordered
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
It’s worth noting that it’s possible to trigger an ordered list by accident, by writing something like this:

Code:

    1986. What a great season.
Preview:
***
1986. What a great season.

***
In other words, a number-period-space sequence at the beginning of a line. To avoid this, you can backslash-escape the period:

Code:

    1986\. What a great season.
Preview:
***
1986\. What a great season.

***
#### Indented
You need to indent for using some functions.

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
To put a code block within a list item, the code block needs to be indented twice — 8 spaces or two tabs:

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
Pre-formatted code blocks are used for writing about programming or markup source code. Rather than forming normal paragraphs, the lines of a code block are interpreted literally. Markdown wraps a code block in both `<pre>` and `<code>` tags.

To produce a code block in Markdown, simply indent every line of the block by at least 4 spaces or 1 tab. For example, given this input:

Code:

    This is a normal paragraph:

        This is a code block.
Preview:
***
This is a normal paragraph:

    This is a code block.
***
A code block continues until it reaches a line that is not indented (or the end of the article).

Within a code block, ampersands (&) and angle brackets (< and >) are automatically converted into HTML entities. This makes it very easy to include example HTML source code using Markdown — just paste it and indent it, and Markdown will handle the hassle of encoding the ampersands and angle brackets. For example, this:

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
### Horizontal Rules
You can produce a horizontal rule tag (`<hr />`) by placing three or more hyphens, asterisks, or underscores on a line by themselves. If you wish, you may use spaces between the hyphens or asterisks. Each of the following lines will produce a horizontal rule:

Code:

    * * *
    ***
    *****
    - - -
    ---------------------------------------
Preview:
***
* * *
***
*****
- - -
---------------------------------------
***
## Inline Elements
### Links
Markdown supports two style of links: inline and reference.

In both styles, the link text is delimited by [square brackets].

To create an inline link, use a set of regular parentheses immediately after the link text’s closing square bracket. Inside the parentheses, put the URL where you want the link to point, along with an optional title for the link, surrounded in quotes. For example:

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
Reference-style links use a second set of square brackets, inside which you place a label of your choosing to identify the link:

Code:

    This is [an example][id] reference-style link.
Preview:
***
This is [an example][id] reference-style link.
***
Then, anywhere in the document, you define your link label like this, on a line by itself:

Code:

    [id]: http://example.com/  "Optional Title Here"
[id]: http://example.com/  "Optional Title Here"
That is:

* Square brackets containing the link identifier (optionally indented from the left margin using up to three spaces);
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
Link definitions are only used for creating links during Markdown processing, and are stripped from your document in the HTML output.

Link definition names may consist of letters, numbers, spaces, and punctuation — but they are not case sensitive.

The implicit link name shortcut allows you to omit the name of the link, in which case the link text itself is used as the name. Just use an empty set of square brackets — e.g., to link the word “Google” to the google.com web site, you could simply write:

Code:

    [Google]: http://google.com/
    [Google][]
Preview:
***
[Google]: http://google.com/
[Google][]
***
### Emphasis
Markdown treats asterisks (*) and underscores (_) as indicators of emphasis. Text wrapped with one * or _ will be wrapped with an HTML `<em>` tag; double *’s or _’s will be wrapped with an HTML `<strong>` tag. E.g., this input:

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

To produce a literal asterisk or underscore at a position where it would otherwise be used as an emphasis delimiter, you can backslash escape it:

Code:

    \*this text is surrounded by literal asterisks\*
Preview:
***
\*this text is surrounded by literal asterisks\*
***
### Code
To indicate a span of code, wrap it with backtick quotes (`). Unlike a pre-formatted code block, a code span indicates code within a normal paragraph. For example:

Code:

    Use the `printf()` function.
Preview:
***
Use the `printf()` function.
***
To include a literal backtick character within a code span, you can use multiple backticks as the opening and closing delimiters:

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
Admittedly, it’s fairly difficult to devise a “natural” syntax for placing images into a plain text document format.

Markdown uses an image syntax that is intended to resemble the syntax for links, allowing for two styles: inline and reference.

Inline image syntax looks like this:

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

Reference-style image syntax looks like this:

Code:

    ![Alt text][img id]
Preview:
***
![Alt text][img id]
***
Where “id” is the name of a defined image reference. Image references are defined using syntax identical to link references:

Code:

    [img id]: url/to/image  "Optional title attribute"
[img id]: url/to/image  "Optional title attribute"
## Miscellaneous
### Automatic Links
Markdown supports a shortcut style for creating “automatic” links for URLs and email addresses: simply surround the URL or email address with angle brackets. What this means is that if you want to show the actual text of a URL or email address, and also have it be a clickable link, you can do this:

Code:

    <http://example.com/>
    
    <address@example.com>
Preview:
***
<http://example.com/>

<address@example.com>
***
### Backslash Escapes
Markdown allows you to use backslash escapes to generate literal characters which would otherwise have special meaning in Markdown’s formatting syntax. For example, if you wanted to surround a word with literal asterisks (instead of an HTML <em> tag), you can use backslashes before the asterisks, like this:

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
