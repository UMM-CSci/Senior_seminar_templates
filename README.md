# UMM CSci Senior seminar templates

LaTeX templates for University of Minnesota, Morris, Computer Science senior seminar proceedings and presentations.

There are three main components here:
* ```Annotated_bibliography``` has ```annotated_bibliography.tex``` and ```annotated_bibliography.bib```, which provide an example of using LaTeX and BibTeX to generate an annotated bibliography.
* ```Sample_paper``` has ```sample_paper.tex``` along with a figure and a BibTeX file provide an example of using LaTeX and BibTeX to generate a basic paper.
* ```Sample_talk``` has ```Sample_talk.tex``` along with a number of photographs and PDF figures provide an example of using LaTeX and the Beamer package to generate a set of slides.

Both the annotated bibliography and the sample paper use ```sig-alternate.cls```, which is our modified version of the [ACM sig-alternate document class](http://www.acm.org/sigs/publications/proceedings-templates). The primary changes we've made to the ACM document class and examples are:
* Replaced the copyright notice with a Creative Commons license.
* Removed the ACM document fees.
* Removed the terms and categories, which seem to really just be confusing relic of a pre-search-engine era.
* Simplified the examples somewhat, removing features such as multiple authors that we're not likely to use.
* "Forced" the paper size to US Letter (8.5 by 11 inches). This is useful because tools like TexMaker default to A4, and this overrides that.

Since the annotated bibliography example and the sample paper both use ```sig-alternate.cls```, we have a link to it in the annotated bibliography folder instead of a second copy. This will hopefully make it easier to ensure that we don't end up with two different versions out there with slightly different behaviors.

## Using LaTeX

We have LaTeX and the TeXMaker GUI installed in the lab, so you should be able to clone a copy of your repo and work in the lab without any problems.

If you want to install LaTeX on your own computer(s), there are a variety of tools you can use. Be prepared, though, for a quite substantial download; the full LaTeX install is very large (currently 2.5GB – there are lots of tools, libraries, fonts, etc.) and can take a while even on the University network (I don't think the server on the other end is very fast).

You could do the whole thing on the command line with editors like emacs or vim, but there are a number of more WYSIWYG LaTeX GUIs worth considering:

 - [TexMaker](http://www.xm1math.net/texmaker/) (what we have in the lab)
 - [TexStudio](http://www.texstudio.org/) (similar to TexMaker)
 - [LyX](http://www.lyx.org/)
 - [TexShop](http://pages.uoregon.edu/koch/texshop/) (Mac specific)

There are also some on-line, cloud-based solutions for folks that prefer that route:

 - [ShareLaTeX](https://www.sharelatex.com/)
 - [Overleaf](https://www.overleaf.com/)
 
These are freemium, and some of the pay features would be pretty useful, so that's an issue to consider. They also don't necessary interact beautifully with `git`, so it you and your advisor want to use `git`/Github, then that's a concern.

## Some notes on LaTeX

**Run LaTeX _and_ BibTeX.** To fully build a LaTeX document you have to run LaTeX (sometimes twice – long story), then run BibTex, and then run LaTeX _again_. This is tedious and annoying, and a holdover from the early days of TeX/LaTeX when computers had very little memory. _Some_ GUI tools like TexStudio try to be "smart" and automatically (re)run things when necessary, but that doesn't always work, and sometimes you still have to re-run things there to get a complete build.

**Make sure you use PdfLatex instead of "plain" LaTeX.** The story here is long and complex, but "plain" LaTeX assumes that (a) all your figures are in PostScript and (b) you want your output in DVI format (instead of PDF). Neither of these assumptions have been likely true in over a decade, and PdfLatex makes more "modern" assumptions that your figures are PDFs and that you want our output to be PDF. So when we say "run LaTeX", we really mean "run PdfLaTeX" in most settings.
