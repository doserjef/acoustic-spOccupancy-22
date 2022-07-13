# Bayesian occupancy modeling with acoustic data in spOccupancy <a href='https://www.jeffdoser.com/files/spoccupancy-web/'><img src="https://github.com/doserjef/spOccupancy/blob/main/man/figures/logo.png" align="right" height="139" width="120"/></a>

### [Jeffrey W. Doser](https://www.jeffdoser.com/)

#### Department of Integrative Biology, Michigan State University

Presentation for Cornell Acoustic Methods Reading Group Series, July 19, 2022

## About

Occupancy modeling is a common approach to assess species distribution patterns across space and/or time, while explicitly accounting for false absences in detection-nondetection data. Passive acoustic monitoring (PAM) provides potentially massive amounts of data on the presence or absence of species over space and time, and thus PAM data can be leveraged in an occupancy modeling framework to provide important insights on distribution patterns of individual species and overall communities. 
 
This presentation is focused on fitting Bayesian occupancy models with acoustic data in the [spOccupancy R package](https://www.jeffdoser.com/files/spoccupancy-web/). I first give a brief introduction of occupancy modeling, provide an overview of spatial autocorrelation and why we may need to account for it in occupancy models, introduce the `spOccupancy` package, and provide two examples of how to fit a single-species and multi-species occupancy model to a data set on a tropical amphibian community from [Ribeiro et al. 2018](https://esajournals.onlinelibrary.wiley.com/doi/abs/10.1002/eap.1741). This repository contains the presentation slides, the example data set, and the R scripts for the two examples. 

## Installing spOccupancy

spOccupancy can be installed from CRAN using `install.packages("spOccupancy")`. 

## Installing additional R packages

In the examples, we will use four additional packages for summarizing our results: [coda](https://cran.r-project.org/web/packages/coda/index.html), [MCMCvis](https://github.com/caseyyoungflesh/MCMCvis), [ggplot2](https://ggplot2.tidyverse.org/index.html), and [sf](https://r-spatial.github.io/sf/). These packages can be installed from CRAN as follows: 

```{r}
install.packages(c("coda", "MCMCvis", "ggplot2", "sf"))
```

## Repository directory

### code

+ `single-species-example.R`: example code that fits a spatial and nonspatial occupancy model to a single amphibian species and provides basic summaries of the results.
+ `multi-species-example.R`: example code that fits a spatial and nonspatial multi-species occupancy model to a tropical amphibian community and provides basic summaries of the results.  

### data

Contains example data set on tropical amphibian occurrence in the Brazilian Atlantic Forest. These data come from [Riberio et al. 2018](https://esajournals.onlinelibrary.wiley.com/doi/abs/10.1002/eap.1741). The data set was obtained from the [Zipkin Lab Code Archive](https://github.com/zipkinlab/Ribeiro_etal_2018_EcoApps) and permsission to use the data set as an example was generously given by [José Wagner Ribeiro Jr](https://github.com/Xuletajr). The full data set used detection-nondetection data from human surveys as well as from autonomous acoustic recording units, and here we will only use the acoustic data. The R data object `ribeiroJrEtAl2018Data.rda` contains the acoustic data from the study formatted for use in `spOccupancy`. 

## Additional Resources

+ [Introductory spOccupancy manuscript](https://besjournals.onlinelibrary.wiley.com/doi/full/10.1111/2041-210X.13897)
+ [spOccupancy website](https://www.jeffdoser.com/files/spoccupancy-web/index.html)
+ Package updates are posted on [my twitter account](https://twitter.com/jeffdoser18)
