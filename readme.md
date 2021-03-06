A gRadual intRoduction to data visualization
================
Chester Ismay and Ted Laderas

Welcome! This is a workshop for the Cascadia R conference that is meant to be a gentle introduction to data visualization using the `ggplot2` and the `plotly` packages. 

You'll learn the basics of the grammar of graphics and learn how to visualize and understand relationships between different kinds of variables in your dataset.

## Prerequisites

Please make sure to have this completed prior to the workshop beginning. Reading over all the materials here will help you get an understanding of what is to be expected and a better grounding to dive into the material as the workshop gets started. To participate in this workshop, you'll need to do the following on your own laptops:

1. Have the latest version of R AND RStudio installed ([Directions are here](http://moderndive.netlify.com/2-getting-started.html#what-are-r-and-rstudio))
2. Be familiar with the [basics of the RStudio Interface](https://ismayc.github.io/rbasics-book/3-rstudiobasics.html#rstudio-layout)
3. We further recommend you read through the first two chapters of the free [ModernDive](http://moderndive.netlify.com) textbook to get up-to-speed/refreshed on R programming. It isn't essential that you do everything there, but we will expect you have gone through this material prior to the workshop starting. If you have questions about this prerequisite material, please reach out!
4. Have the following R packages installed: `dplyr`, `readr`, `plotly`, `gapminder`, `remotes`, `fivethirtyeight`, and `ggplot2`. 

    This can be accomplished by copying the following code into the *Console* in RStudio and pressing Enter. Note that you'll see quite a few lines of code run while the packages are installing. Don't be alarmed. After all of these packages are installed you should see them listed in the Packages tab in the bottom right section of RStudio.
    
    We needed to install the developmental version of the `ggplot2` package in order for it to work nicely with the `plotly` package in Part 3 of this workshop and this is the reason for installing the [`remotes`](https://github.com/r-lib/remotes) package as well.

    ```
    install.packages(c("dplyr", "readr", "plotly", "gapminder", "remotes", "fivethirtyeight"))
    remotes::install_github("tidyverse/ggplot2")
    ```
    
    - The [`tidyverse`](http://tidyverse.tidyverse.org/) contains a variety of different packages that will be useful in your analysis including the [`ggplot2`](https://ggplot2.tidyverse.org/) package that will be the focus of this workshop. We'll also use the [`dplyr`](https://ggplot2.tidyverse.org/) package for data wrangling and the [`readr`](https://readr.tidyverse.org/) package for reading in data.
    - The [`plotly`](https://plotly-book.cpsievert.me/) package will be used for interactive graphics. 
    - The [`gapminder`](https://github.com/jennybc/gapminder/blob/master/README.md) package contains a data set made famous by Hans Rosling exploring data on the world's countries.
    - The [`fivethirtyeight`](http://fivethirtyeight-r.netlify.com/) package contains many datasets used by data journalists at FiveThirtyEight.com.

## IMPORTANT FINAL STEP

- Download the conference materials as a [ZIP file](https://github.com/tidyverse-intro/gradual_visualization/archive/master.zip) and extract the files there as a folder on your computer. Note the importance of actually extracting all the files to a folder. Double click on the **gradual_visualization.Rproj** file in that folder to open up an RStudio project containing the files needed for the workshop.  

You'll be following along in the **Part1-ggplot2_intro.Rmd**, **Part2-working_with_factors.Rmd**, and **Part3-interactive_plots.Rmd** files, running the R code in the "chunks" there, and writing your own code to practice. You can also follow along with the webpage for the workshop at <https://cascadiarconf-viz.netlify.com>.
    
Remember, in this workshop we will adhere to the [code of conduct for this conference](https://cascadiarconf.com/coc/). Be respectful of your fellow students, workshop leaders, and workshop TAs and let's learn together.

## Outline of this Workshop

Please bring a pencil, at least one color of pen, and some paper to write on.

1. Visualizing continuous data (scatterplots)
    - Learning about `aes`thetics and `mapping` of variables
    - Some basic `geom`etries
1. Visualizing categorical data
    - More about `geom`s
    - Learning to create small multiple plots using `facet`ing
1. Visualizing categorical versus continuous data (boxplots and violin plots)
1. Making your plots interactive using the `ggplotly()` function in the `plotly` package

