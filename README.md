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
* Changed the paper size to 8.5 by 11 from the default A4. 

Since the annotated bibliography example and the sample paper both use ```sig-alternate.cls```, we have a link to it in the annotated bibliography folder instead of a second copy. This will hopefully make it easier to ensure that we don't end up with two different versions out there with slightly different behaviors.
