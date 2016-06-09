Vagrant Talk
============

Talk on Vagrant, originally given at [ManLUG](http://www.manlug.org/) in November 2013. If you'd like me to give this talk at a user group or conference, please drop me an email at: paul@xk7.net

Slides and notes
----------------

Slides and notes are available as Markdown source files. You can use [pandoc](http://johnmacfarlane.net/pandoc/) to convert them into various formats (PDF slides are the most reliable).

Generate slides:

    pandoc -t beamer slides.md -o slides.pdf

Generate notes:

    pandoc notes.md -o notes.pdf
    
For other formats, substitute the relevant type or file extension as outlined in the pandoc documentation.

Links
-----

 * [Creating a Debian Wheezy Base Box for Vagrant](https://mikegriffin.ie/blog/20130418-creating-a-debian-wheezy-base-box-for-vagrant/)
 * [Vagrant: Up and Running](http://shop.oreilly.com/product/0636920026358.do) - Mitchell Hashimoto (O'Reilly)
 * [FLOSS UK Newsletter](http://www.flossuk.org/Newsletter) - September 2013 issue contains a review by Paul Waring of _Vagrant: Up and Running_
