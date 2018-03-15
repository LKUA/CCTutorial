# Pretend tutorial
## LK

### Make a tutorial

#### <a href="#section1"> 1. Import data in R</a>

#### <a href="#section2"> 2. Create a plot</a>

#### <a href="#section3"> 3. Save the plot</a>

### You can get all of the resources for this tutorial from <a href="https://github.com/ourcodingclub/CC-EAB-tut-ideas" target="_blank">this GitHub repository</a>. Clone and download the repo as a zip file, then unzip it.

<a name="section1"></a>

## 1. Import data in R

Open `RStudio`, create a new script by clicking on `File/ New File/ R Script` set the working directory and load the packages we'll need.
  
```r
# Set the working directory
setwd("C:/Users/lucik/Google Drive/Post Doc/ARC/CC-Ghent-master")


# Load packages
library(ggplot2)
library(dplyr)
```

<a name="section2"></a>

## 2. Create a plot

THis makes a nice plot
```r
# Add your code and comments here

load("traits.RData")
load("traits_sum.RData")

# Comparing within-individual correlations
# Trait-trait correlation plot
(correlation <- corrplot(cor(traits[,2:5], use = "pairwise.complete.obs")))

# Save the plot in your working directory
png(filename = "trait_correlation.png", width = 600, height = 600)
(correlation <- corrplot(cor(traits[,2:5], use = "pairwise.complete.obs")))
dev.off()

```

<a name="section3"></a>

## 3. The third section

Here you can add some more text if you wish.

```r
# Add more code and comments
```



<center> <img src="{{ site.baseurl }}/trait_correlation.png" alt="Img" style="width: 800px;"/> </center>

This is the end of the tutorial. Here is a summary of what we learned:

##### - something
##### - something else
##### - and a third thing

We can also provide some useful links:

For more on `ggplot2`, read the official <a href="https://www.rstudio.com/wp-content/uploads/2015/03/ggplot2-cheatsheet.pdf" target="_blank">ggplot2 cheatsheet</a>.
