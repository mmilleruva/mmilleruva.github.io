---
layout: post
title:  "Sublime Power User Tips"
date:   2014-07-10 23:08:03
categories: Sublime Text 2
---

## Goto Anything

* `CMD-P` - Goto anything. Fuzzy search all the files in your project. Entering an @ character searches for symbols within the currently selected file (i.e. method names, classes, ...) or use `cmd-r`. So if I was in index.html and wanted to update the css style `.table-style` in main.css I could use the following commands `CMD-P`, then enter `main@table-sty` to go to that css style. I purposefully didn't complete everything to show that you only need to type what is necessary.

## Multiple Cursors
* `CMD-D` (multiple times) -highlights next occurences of a string and allows editing with multiple cursors

* `CNTRL-CMD-G` - Creates a cursor for every instance of the string

* `OPT` - Allows Column highlighting

* `CMD-SHIFT-L` - create a cursor for every line highlighted


## Search And Replace

* `cmd-i` - incremental search. You can use enter to select the value of your search

## Command Palette

* `cmd-shift-p` - opens the command palette

## Snippets

* `cmd-/` - comments out the current line you are on.
* pulling up the command palette, you can type snippet to show all of the snippets for the language you are in.
