# Overview

An example of using LaTeX and BibTeX to create a paper
using the format we want for the course.

There's a lot of useful examples of how to use LaTeX in
`sample_paper.tex`, and examples of BibTeX formatting in
`sample_paper.bib`.

Our recommendation is to copy `sample_paper.tex` to something
that makes more sense for your setting, like `lamberty.tex`
or `face_generation_using_GANs.tex`. You probably also want
to make a copy of `sample_paper.bib`, or at least rename it.

`sample_paper.tex` should build successfully "as is". If it
doesn't or you have any problems with it, definitely let us
know.

# Accessibility

## Resources

The main source for creating accessible articles is the guide [Accessible PDFs Using the ACM Article Template by Kevin Lin](https://kevinl.info/accessible-pdfs-using-the-acm-article-template/)

This includes links to tools for checking accessibility and template files. 

## Changes to sample paper

These are changes made to add tags for accessibility and to improve
other accessibility issues:

* The documentclass was changed to `acmart-tagged`
* The following was added right in front of the documentclass:
```
\DocumentMetadata{
  lang=en,
  pdfversion=2.0,
  pdfstandard=ua-2,
  testphase={phase-III,firstaid,math,title}
}
```
* The LaTeX compiler option was changed to LauLaTeX + MakeIndex + BibTex. This was an option in the TexWorks editor (by the green arrow). It is also possible to change to LuaLaTeX in Overleaf. 

Future work:
* Add descriptions to pictures. 




