## Notes:

The instructions refer to old rmarkdown and knitr versions.
Rather than using the knit2html function I used the function render from the rmarkdown package.

The figure are in the directory PA1_template_files rather than in figure/ as asked by the instructors.
I didn't change the output directory setting as suggested by the creator of knitr Yihui Xie.
See this Github issue for more info: https://github.com/rstudio/rmarkdown/issues/587

As a consequence the md file will contain the right relative path for the figures,
but these will be placed in "PA1_template_files/figure-html/" rather than in "figure"
as requested by the instructors.

I could have copied manually the files, but I feel this would be wrong because you add
to the data analysis pipeline a step that could possibly generate error and confusion
if I update the figures in the document but forget to copy them again in the "figure/" folder.
