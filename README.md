# g2chvc


Genes to Cognition: Hippocampus vs Cortex project

## Prerequistes

You will first need to install the data package
[g2chvcdata](http://github.com/sje30/g2chvcdata) and the
[sjemea](http://github.com/sje30/sjemea) packages.

# Installing this package

To install this package in R you need the devtools package; skip the
first line if you already have it installed:

	install.packages("devtools")
	devtools::install_github("sje30/g2chvc", quick=TRUE)

Setting `quick=TRUE` prevents the vignettes from being rebuilt (which
can take a long time right now.)

## Generating the figures

The scripts for generating figures are stored in `inst/makefigs/`
which you can directly run, e.g.:

	require(g2chvc)
	source(system.file("makefigs/hvc_rasters.R", package="g2chvc"))

In this case you will see PDFs made in your current working directory.

## Generating the SVM table.

	knitr::knit2pdf(system.file("makefigs", "hvc_class.Rnw", package="g2chvc"))

This will generate a vignette and leave a copy of the .tex file
and the generated vignette `hvc_class.pdf`.



