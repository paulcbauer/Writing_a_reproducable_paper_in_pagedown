# Writing a reproducable paper with R Markdown and Pagedown
This repository contains files and a template to write a reproducible paper in pagedown. `paper.pdf` contains the pdf-formatted version of our template which provides an introduction to the fairly new pagedown R-package as well as "tricks" and code to produce important elements of scientific papers (e.g., tables, figures, inlince code, etc.).
 
The file underlying this template is `paper.Rmd` which contains all the code and input to produce a good-looking working-paper "style" doucment (in html and in pdf).

All the files you will need to "replicate" `paper.pdf` are:

1. the input files:

* `paper.rmd` (the underlying R Markdown file).
* `references.bib` (the bibliography).
* `data.csv` (some raw data).
* `american-sociological-association.csl` (defines the style of your bibliography). 
  * You can download various citation styles [here](https://github.com/citation-style-language/styles)

2. the "styling" files:

Basically, these are files you will need to specify in the YAML of your `paper.rmd`, so that R and ultimately pagedown recognizes the certain style you want to achieve for your document. With using our templates, you will create a document that has the "look" of a working paper (we based our files on the [jss_paged pagedown format](https://github.com/rstudio/pagedown#journal-of-statistical-software-article-pagedownjss_paged)). 

* `wp_paged.html` (based on `jss_paged.html`)
* `wp.css`
* `wp-fonts.css`
* `wp-pages.css`

Take `paper.rmd` (the underlying R Markdown file of this pdf) and have a look at the YAML (line \#18 - \#22) to see how to specifiy these files.
Basically, what happens here is that within the [jss_paged function](https://rdrr.io/cran/pagedown/man/jss_paged.html) we additionally specify that we want to use custom CSS and custom HTML.

Once you run/compile the `paper.rmd` file in Rstudio it creates a output file called `paper_pagedown.html`.

By using pagedown's `chrome_print` function in the YAML (line \#25) your html based web page will be printed to `paper_pagedown.pdf` (the one you are reading right now).

Both outputs will be saved in your working directory.



We intend to update this file when we discover more convenient code (you can follow any updates within this repository).

Enjoy! 
 
