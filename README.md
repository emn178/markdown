README.md
=========
This is a README.md example shows how to write a README.md.

## Headers
Markdown supports two styles of headers, Setext and atx.
### Setext
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
### atx
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
Optionally, you may “close” atx-style headers. This is purely cosmetic — you can use this if you think it looks better. The closing hashes don’t even need to match the number of hashes used to open the header. (The number of opening hashes determines the header level.) :
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
