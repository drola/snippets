Document editing in Linux terminal
==================================

PDF merge, stitch PDF's together
--------------------------------
Run:

    gs -dBATCH -dNOPAUSE -q -sDEVICE=pdfwrite -sOutputFile=output.pdf in1.pdf in2.pdf in3.pdf

Requires:

    sudo apt-get install ghostscript


Source: [http://askubuntu.com/a/257170](http://askubuntu.com/a/257170)