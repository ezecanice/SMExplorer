
<!-- README.md is generated from README.Rmd. Please edit that file -->
SMExplorer
==========

[![Travis-CI Build Status](https://travis-ci.org/BroVic/SMExplorer.svg?branch=master)](https://travis-ci.org/BroVic/SMExplorer)

An R package for the exploratory analysis of social media metrics

SMExplorer is currently in beta-mode
------------------------------------

You are invited to contribute to this project by helping us test the app, identifying issues and suggesting possible changes and new features. To participate please follow the following instructions:

### Install R

R is a programming language as well as an environment that is tailored for data analysis. Visit <https://cloud.r-project.org> to get the current version that suits your system. Skip this step if you already have it. This application depends on R version 3.3.3 and above. To check the version you have installed run

``` r
R.version.string
```

### Install R Studio (optional)

R Studio is an integrated development environment (IDE) that makes learning and working with R a lot easier. You DO NOT need it to run the application, but it will help. It is available for download at the [company's website](https://www.rstudio.com/products/rstudio/download/).

### Install SMExplorer

You can get SMExplorer pre-built or you can fork/clone this repository and build the package yourself

#### To get a pre-built copy

1.  Install the devtools package: Devtools is a package that makes it easy to build stuff in the R environment. Also, it will make it easy for the user to download this package from GitHub as specified in the next section. To get devtools run this line in the R console

``` r
install.packages("devtools")
```

1.  Install and load the package from the repository by running this line inside the R console:

``` r
library(devtools)
install_github("NESREA/SMExplorer")
```

#### To build your own copy

1.  Fork this repository and get a local copy for your system using `git clone`. Be sure of the folder in which you are going to store the repository.
2.  (For Windows) open the command prompt and navigate to the parent folder of the repository using the `cd` command.
3.  Run this command to build SMExplorer via the command line

        R CMD build SMExplorer

4.  Check the folder's contents using `dir`. If all went well, you should see a compressed file with name `SMExplorer_x.x.x.9xxx.tar.gz`. This is the output of a successful build.
5.  Install SMExplorer into the R library, from where it's functionalities can be deployed.

        R CMD INSTALL SMExplorer_x.x.x.9xxx.tar.gz

### Test the App

#### Run the Application

The app has only one externally accessible function, `explore()`. Now that you have installed it, you will have to load it into your open R session as follows:

``` r
library(SMExplorer)

# Run the application
explore()
```

#### Register a New OAuth Session

On first use, you will find an error message telling you that you have not registered any security credentials. Click on the link that says *"Register new session"* and you will be asked in the R console wether you want to use direct authentication. Enter "1" for YES and return to the app's user interface.

#### Make an entry

You are likely to see a second error message saying *"Bad HTTP"*.

![](error-badrequest.PNG)
This is because no search term has been supplied for analysis. For now, the app has not been enabled to provide search values on start, but that feature is coming soon. To begin your analysis, enter a term you are looking for on Twitter and click on the **Go!** button.

**NB:** There are a few other common error messages that occur like *"timeout"* and *"set\_up\_twitter\_oauth"* did blah-blah-blah... these are usually due to poor network service and when you see them just try to run the app again by clicking on **"Go"**.

Please report issues **[here](https://github.com/NESREA/SMExplorer/issues)** as we work on making the application very robust.

I can also be reached by [email](mailto:victor.ordu@nesrea.gov.ng).
