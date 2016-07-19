LatexScript
===========

This set of perl script is devised to handle manipulating
latex source files. Primary intend to use is when submitting
a latex document to Arxiv, a scientific journal or any other
place where some cleaning is necessary but tedious.

Overview
--------

Latex is very fine when writing documents. Typically one works
in a directory and files accumulate, but not all are send to
the editor. Instead, a large portion may be attempts, or discarded
files that are of no interest to the editor.

Thus only the files that occur in the text need to be send.
Also, some additional formatting may be necessary. The goal
of the perl scripts in LatexScript is to help the author work
out all this.

Disclaimer: this author is not responsible for any bug that
happen when using the program. You are best to save your stuff.
I cannot be held responsible for bugs and trouble that accompany
using the program. Additionally, not all latex code can be
used as input since there is just too much variety.

However, if a bug happen, I will have a look and try to help
if possible. Send me an e-mail at mathieu.dutour@gmail.com

For the impatient
-----------------

The best way to use the program is to copy the manuscript files
in another directory on which the operations are done.

Those program are doing various operations on the latex source
of the papers. Those operations are conservative in the sense
that the source are modified but the paper still compiles and the
obtained .ps or .pdf file is identical to the original.

List of available scripts
-------------------------

Following programs are available in LatexScript
  * **RemovePercentLine**: Remove commentaries indicated by %
  * **DirectoryUnfold**: Put all files in a directory and ensures
that the result still compiles. Necessary for arxiv and
Elsevier submissions.
  * **LatexFileMerging**: Remove \input by merging the tex source in the program.
  * **FigureFileRenumbering**: Some editors prefer that your figure filenames
are organized in a certain way. This program will allow you to comply.
  * **ReorderEpsfig**: Sometimes the use of the operation
\epsfig{height=3mm, file=MyImage.eps} is illegal (for example in elsevier)
and should be replaced by
\epsfig{file=MyImage.eps, height=3mm}
  * **CheckCitation**: This program detect citation which are not used in the text It also give detects some other possible inconsistencies.
  * **CheckReference**: This program detect equation reference that are not used and other inconsistencies
  * **MakeArxivArch**: This programs make an archive directly submittable to the arxiv
repository system.
  * **SimpleCopy**: This program copies the file of a paper to another directory and copies as well all the dependencies that may exist
  * **SimpleCopyForEdit**: This program differs from the preceding in that it copies as well the makefile if existing and also the .fig file or .png files if existing.


References
----------

The latex editing system is well documented See for example https://latex-project.org/intro.html

