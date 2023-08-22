An example of using LaTeX and the `beamer` package to create
a set of slides for a talk.

Most people use other slide tools like Google Slides
these days. These are typically much easier to learn, and
the WYSIWYG nature of them can be really appealing. They do
have a few weaknesses, though:

1. They don't have all the wonderful math formatting tools
    LaTeX gives you.
1. They don't do automatic citation management like
    LaTeX + BibTeX give you.
1. They don't force you to be consistent about things
    like fonts, font sizes, and things like title placement.

The first of these may not matter to you if your presentation 
doesn't have much or any math in it. If it does, though,
LaTeX will probably make that math look a _lot_ better than
some other presentation tool.

You typically don't provide a ton of citations in your
presentation, so the second probably isn't a huge deal.

The third is subtle, but important. Most slide tools have
themes that try to make sure that your slides look consistent
across your presentation. Most of them will, however, automatically
shrink your font sizes if you put put too much text on a slide.
This can lead to both inconsistent appearance across your slides,
and in the worst case can lead to text so small it can't be
read by old eyes at the back of the room.

If you do choose to use LaTeX for your presentation,
`Sample_talk.tex` provides a complete example of using
the `beamer` packet in LaTeX to build a slide deck actually
used for an ACM conference presentation several years ago.

`Sample_talk.tex` should build successfully "as is". If it
doesn't or you have any problems with it, definitely let us
know.
