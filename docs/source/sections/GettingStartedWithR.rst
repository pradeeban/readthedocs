************************
ISB-CGC Workshops at NCI
************************

This information is currently intended only for attendees who have
signed up for the
`workshops at NCI on May 24th and 25th <https://cbiit.nci.nih.gov/ncip/nci-cancer-genomics-cloud-pilots/nci-cancer-genomics-cloud-workshop>`_.
After the workshops, all materials will be made available as part of the
ISB-CGC documentation here on readthedocs.

**Please check back again before the day of the workshop!**

Step #1: Installing R and RStudio
###################################################

Basic Information
-----------------
R is a great way to with the cloud pilot data. We can perform Big Queries,
statistically model data, and easily visualize the results. R programming
is easier and more robust then ever before.


Installation
-----------------------------------

RStudio is a freely available development environment that makes working
in R more intuitive. Always install (and update to) the most recent versions.

First we need to download and install R. `Download and install R <https://cran.rstudio.com/>`.

Next we download and install RStudio. `RStudio <https://www.rstudio.com/products/rstudio/download/>`.

Questions?
----------

Let us know if you're having trouble! We're here to help.


Step #2: How to prepare for the workshop
########################################

There's a few R libraries we need to install for the workshop. To do that,
start up RStudio, and click over to the "Console" window containing the
interactive R prompt. The window should be in the lower left corner.

**Necessary:**

Install `devtools <https://cran.r-project.org/web/packages/devtools/index.html>`::

	install.packages("devtools")

Install `bigrquery <https://cran.r-project.org/web/packages/bigrquery/index.html>`.::

	install.packages("bigrquery")

Install `httr <https://cran.r-project.org/web/packages/httr/index.html>`.::

	install.packages("httr")

Install `ISBCGCExamples <https://github.com/isb-cgc/examples-R>`. ::

	library(devtools)
	install_github("isb-cgc/examples-R", build_vignettes=TRUE)

To view and run the ISB-CGC R vignettes.::

	  help(package="ISBCGCExamples")

**Strongly Recommended:**

Install `ggplot2 <https://cran.r-project.org/web/packages/ggplot2/index.html>`::

	install.packages("ggplot2")

There are vignettes for each TCGA data type, and more elaborate examples involving analyzing genomic data,
correlating gene expression and methylation, and correlating protein and mRNA levels.

The vignettes as R-markdown can be found in the examples-R/inst/doc directory, which can serve as examples of using builtin BigQuery functions like Pearson correlation,
or even how to implement more complex functions like Spearmans correlation. Queries can be simple character vectors, or standalone files.

Results are returned as data.frames using the bigrquery package to interact with the servers.
The SQL files used in the vignettes can be found at examples-R/inst/sql. These are parsed and dispatched with arguments using the DisplayAndDispatchQuery function,
found in the file of the same name in examples-R/R.

**Additional Resources:**

`ISB-CGC documentation <http://isb-cancer-genomics-cloud.readthedocs.io/en/latest/index.html>`