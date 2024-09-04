# UMM CSci Senior seminar templates

LaTeX templates for University of Minnesota, Morris, Computer Science senior seminar proceedings and presentations.

There are three main components here:
* ```Annotated_bibliography``` has ```annotated_bibliography.tex``` and ```annotated_bibliography.bib```, which provide an example of using LaTeX and BibTeX to generate an annotated bibliography.
* ```Sample_paper``` has ```sample_paper.tex``` along with a figure and a BibTeX file provide an example of using LaTeX and BibTeX to generate a basic paper.
* ```Sample_talk``` has ```Sample_talk.tex``` along with a number of photographs and PDF figures provide an example of using LaTeX and the Beamer package to generate a set of slides.

Both the annotated bibliography and the sample paper use the
[ACM `acmart` Format](https://www.sigplan.org/Resources/Author/). 
We've also simplified the examples somewhat, removing features such as multiple authors that we're not likely to use.

## Using LaTeX

There are several different ways to use LaTeX in this course,
including:

- Online tools
- Using the tools installed in the CSci Lab
- Installing LaTeX on your own computer

### Online tools

Probably the most common approach these days is to use [Overleaf](https://www.overleaf.com/), which provides a cloud-based system that's kind of like Google Docs but for LaTeX.
 
These are freemium, and some of the pay features would be pretty
useful, so that's an issue to consider. Two particular features
you'd have to pay for if they matter to you are:

- The ability to share with more than one other person
- The ability to sync your work up with `git`/GitHub

The sharing limitation usually isn't a big deal because the
student just shares with their advisor. If you wanted to share
with other people (the course instructor, friends, family, etc.), though, then you'd need to pay.

Being able to connect your project to `git` would give you
all the nifty tools that `git` provides. Since there's
really just one author on the project, and no particularly
pressing need for things like branches, this is typically not
an issue.

### CSci lab

We have LaTeX and the TeXMaker GUI installed in the lab, so you should be able to clone a copy of your repo and work in the lab without any problems.

### Your own computer

If you want to install LaTeX on your own computer(s), there are a variety of tools you can use. Be prepared, though, for a quite substantial download; the full LaTeX install is very large (currently 2.5GB – there are lots of tools, libraries, fonts, etc.) and can take a while even on the University network. (It's not clear that the the server on the other end is very fast).

You could do the whole thing on the command line with editors like emacs or vim, but there are a number of more WYSIWYG LaTeX GUIs worth considering:

 - [TexMaker](http://www.xm1math.net/texmaker/) (what we have in the lab)
 - [TexStudio](http://www.texstudio.org/) (similar to TexMaker)
 - [LyX](http://www.lyx.org/)
 - [TexShop](http://pages.uoregon.edu/koch/texshop/) (Mac specific)

#### Troubleshooting

When running on Windows, I had an error 

```
! pdfTeX error (font expansion): auto expansion is only possible with scalable 
fonts.
```

Running the file `updmap` in `C:\Program Files\MiKTeX\miktex\bin\x64` fixed the issue. The file location, of course, depends on where MikTex got installed. 

## Some notes on running LaTeX directly

> The notes below only apply if you're running something
> like `pdflatex` and `bibtex` on the command line on a
> lab computer or your own computer. If you're using an online
> tool like Overleaf or an "IDE" like TexMaker they'll take
> care of these things for you.

**Run LaTeX _and_ BibTeX.** To fully build a LaTeX document you have to run LaTeX (sometimes twice – long story), then run BibTex, and then run LaTeX _again_. This is tedious and annoying, and a holdover from the early days of TeX/LaTeX when computers had very little memory. _Some_ GUI tools like TexStudio try to be "smart" and automatically (re)run things when necessary, but that doesn't always work, and sometimes you still have to re-run things there to get a complete build.

**Make sure you use PdfLatex instead of "plain" LaTeX.** The story here is long and complex, but "plain" LaTeX assumes that (a) all your figures are in PostScript and (b) you want your output in DVI format (instead of PDF). Neither of these assumptions have been likely true in most of your lifetime, and PdfLatex makes more "modern" assumptions that your figures are PDFs and that you want our output to be PDF. So when we say "run LaTeX", we really mean "run PdfLaTeX" in most settings.
