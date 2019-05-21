# Template for Reveal presentations

This project is intended to be used as a base/template when creating new
presentations.

The presentations are based on reveal.js. Reveal.js and some third party plugins
are added as git submodules to make it easy to keep them up to date. To get
everything you need you can clone with the --recurse-submodules option

```
git clone --recurse-submodules -j4 https://github.com/MartinWallgren/reveal-template.git
```

or if you already cloned the repo you can get the submodules as below.

```
git submodule init
git submodule update
```

# Markdown for all the things

The presentation resides in index.html which will load everything you need and
then generate slides from the markdown in slides.md. This means that the entire
presentation can be written in markdown. It is possible to add slides directly
to index.html too if you need something special that can't be done in markdown.

# Launch the presentation

Some of the plugins does not work properly if the presentation is not hosted by
a HTTP server. There is a script in the root called present.sh that will host
the presentation for you and make it available on http://localhost:8000.

present.sh is basically just a glorified alias for the simple HTTP server that
is part of the standard python library.

# Examples

There are examples on how to create some of the common elements in markdown in
example.md. If you want to see how they look execute present.sh and go to
http://localhost:8000/example.html


# PDF Export

The pdf export plugin is installed
(https://github.com/McShelby/reveal-pdfexport), this means that pressing `E`
will change the slides to a pdf friendly format. Then simply print to file to
get a pdf.
