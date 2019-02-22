#1 - Long footnotes out of order
================================
Date: 2017-12-13 17:34

Footnote gets sometimes shunted to the next page because it won't fit,
while the (shorter) next one does and gets printed on the right page.

Like

    1, 3
    2, 4, 5

in my "test document" when one inch of space is added before the title
in the Paper cover.

#2 - Superscript not working in titles
======================================
Date: 2017-12-13 18:42

As per the title, superscript (like in \*) doesn't work properly when
embedded within a title (e.g., `.Heading 1 "Something \**"`), resulting
in an error like this:

    test.troff:28: can't transparently output node at top level

And leaving the size increased.

#FIXED 3 - Footnotes get too much bottom margin
===============================================
Date: 2017-12-16 15:20

When invoking `./test.sh` the footnotes on the second page have what
looks like a full 1v of excess space between themselves and the footer.

#4 - Dictionary macros footer not reached
=========================================
Date: 2017-12-16 15:21

Only happens on the first page (plus adding a heading to the end of the
current dictionary file just... breaks it, putting the heading on a new
page and creating **another** new page after that).
