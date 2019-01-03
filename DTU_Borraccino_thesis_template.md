# BORRACCINO's PdfLaTeX thesis template (DTU Wind Energy) #

This is a thesis template adapted from "Laursen's XeLaTeX thesis template" [Laursen thesis](https://bitbucket.org/_laursen/laursens-xelatex-thesis-template).

The template has been modified to: 

1. work with PdfLaTeX instead of XeLaTeX 
2. employ DTU Wind Energy's official logos, colors, etc.

Examples of what can be done in a thesis also provided (e.g. including a pdf file of a journal article).


### TeX Studio ###

The template was prepared in TeX Studio. It employs so-called magic comments. The following build command line may be helpful to perform manual typesetting:
txs:///pdflatex | txs:///biber | txs:///pdflatex | txs:///view-pdf.

where:

* txs:///pdflatex is: pdflatex.exe --enable-write18 -synctex=1 -interaction=nonstopmode %.tex
* txs:///biber is: biber.exe %
* txs:///view-pdf is: the default embedded pdf viewer.

### Options & Modifications ###
* Similarly to Laursen's example, static information can be set in ``preamble/static.tex``. 
* The file ``preamble/general.tex`` was mostly modified for the font sizes of titles, headings, etc. 
* The file ``preamble/font.tex`` allows the font to work either with XeLaTeX or PdfLaTeX. The [TeX Gyre Adventor](http://www.ctan.org/tex-archive/fonts/tex-gyre) font series is used, and normally part of MiKTeX latest versions.

### Other included packages ###
A number of extra packages are added in: ``preamble/Antoine_packages.tex`` (for maths, tables, etc).  This file is where you should add any other package you would like to use.

### Prefront & Front matters ###
* The file ``prefrontmatter/titlepage.tex`` creates the title page.
* The file ``prefrontmatter/colophon.tex`` allows to change details on the Department/Section.
* The folder ``frontmatter`` contains ``.tex`` files for the Summary, Preface, etc.

### Main Matter  ###
Contains the list of chapters. One ``.tex`` file per chapter.

### Bibliography ###

Prepared using [BibTeX](http://www.bibtex.org/). Place your bibliography file in the ``bibliography/`` folder, and change the line: ``\addbibresource{bibliography/Thesis.bib}``.

### NOTA BENE ###
The template does not substitute to the DTU Wind Energy's guidelines. The template is not officially approved by DTU Wind Energy. 
It can be freely used and adapted by the user for writing a PhD/MSc/BSc thesis. The user has the responsibility to ensure  compliance with DTU guidelines (or any other institute's).

### Post Scriptum ###
The template was prepared during my PhD thesis at DTU Wind Energy. I hope it will be helpful to those in the same situation as I was.