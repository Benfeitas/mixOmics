
[![R build
status](https://github.com/mixOmicsteam/mixOmics/workflows/R-CMD-check/badge.svg)](https://github.com/mixOmicsteam/mixOmics/actions)
[![](https://img.shields.io/badge/bioc%20release-6.12.2-green.svg)](https://www.bioconductor.org/packages/mixOmics)
[![Build
Status](https://travis-ci.org/mixOmicsTeam/mixOmics.svg?branch=master)](https://travis-ci.org/mixOmicsTeam/mixOmics)
[![](https://codecov.io/gh/mixOmicsTeam/mixOmics/branch/master/graph/badge.svg)](https://codecov.io/gh/mixOmicsTeam/mixOmics)
[![download](http://www.bioconductor.org/shields/downloads/release/mixOmics.svg)](https://bioconductor.org/packages/stats/bioc/mixOmics)
[![](https://img.shields.io/github/last-commit/mixOmicsTeam/mixOmics.svg)](https://github.com/mixOmicsTeam/mixOmics/commits/master)
[![license](https://img.shields.io/badge/license-GPL%20\(%3E=%202\)-lightgrey.svg)](https://choosealicense.com/)
[![dependencies](http://bioconductor.org/shields/dependencies/release/mixOmics.svg)](http://bioconductor.org/packages/release/bioc/html/mixOmics.html#since)

![](http://mixomics.org/wp-content/uploads/2019/07/MixOmics-Logo-1.png)

This repository contains the `R` package [now hosted on
Bioconductor](http://bioconductor.org/packages/release/bioc/html/mixOmics.html)
and our current `GitHub` version.

## Installation

**(Mac OS Users Only:)** Ensure you have installed
[XQuartz](https://www.xquartz.org/) first.

#### Latest Bioconductor Release

Make sure you have the latest R version and the latest `BiocManager`
package installed following [these
instructions](https://www.bioconductor.org/install/) (if you use legacy
R versions (\<=3.5.0) refer to the instructions at the end of the
mentioned page), you can then install `mixOmics` using the following
code:

``` r
## install BiocManager if not installed
if (!requireNamespace("BiocManager", quietly = TRUE))
    install.packages("BiocManager")
## install mixOmics
BiocManager::install('mixOmics')
```

#### `GitHub` Versions
We have two versions on GitHub. First, make sure you have the latest version of Bioconductor, then install the library [devtools](https://github.com/r-lib/devtools):
``` r
# Check your BioC version
if (BiocManager::version() >= package_version('3.11')) 
{
  BiocManager::install("mixOmicsTeam/mixOmics")
} else
{
  message('Please update to the latest Bioconductor (https://www.bioconductor.org/install/) ',
          'to install the stable GitHub version')
}

# Install devtools from CRAN
install.packages("devtools")

# Or the development version from GitHub:
# install.packages("devtools")
devtools::install_github("r-lib/devtools")
```

##### Stable version
This is our last stable version of `mixOmics` from
`GitHub` (as bug-free as it can be):
``` r
library('devtools')
BiocManager::install("mixOmicsTeam/mixOmics")
```

##### Development version
Our [development
version](https://github.com/mixOmicsTeam/mixOmics/blob/devel/DESCRIPTION#L4)
includes our latest bugs fixes and new features yet to be widely tested (see below **'What's new'**):

``` r
library('devtools')
BiocManager::install("mixOmicsTeam/mixOmics@devel")
```


Check after installation that the following code does not throw any
error (especially Mac users - refer to [installation
instructions](#installation)) and that the welcome message confirms you
have installed [the latest
version](https://github.com/mixOmicsTeam/mixOmics/blob/master/DESCRIPTION#L4):

``` r
library(mixOmics) 
#> Loaded mixOmics ?.?.?
```


## Contribution

We welcome community contributions concordant with [our code of
conduct](https://github.com/mixOmicsTeam/mixOmics/blob/master/CODE_OF_CONDUCT.md).
We strongly recommend adhering to [Bioconductor’s coding
guide](https://bioconductor.org/developers/how-to/coding-style/) for
software consistency if you wish to contribute to our R codes.

### Bug reports and pull requests

To report a bug (or offer a solution for a bug\!):
<https://github.com/mixOmicsTeam/mixOmics/issues>. We fully welcome and
appreciate well-formatted and detailed pull requests. Preferrably with
tests on our datasets.

### Discussion forum

We wish to make our discussions transparent so please direct your
questions to our discussion forum
<https://mixomics-users.discourse.group>. This forum is aimed to host
discussions on choices of multivariate analyses, bug report as well as
comments and suggestions to improve the package. We hope to create an
active community of users, data analysts, developers and R programmers
alike\! Thank you\!

## About the `mixOmics` team

`mixOmics` is collaborative project between Australia (Melbourne),
France (Toulouse), and Canada (Vancouver). The core team includes
Kim-Anh Lê Cao - <https://lecao-lab.science.unimelb.edu.au> (University
of Melbourne), Florian Rohart - <http://florian.rohart.free.fr>
(Toulouse) and Sébastien Déjean -
<https://perso.math.univ-toulouse.fr/dejean/>. We also have key
contributors, past (Benoît Gautier, François Bartolo) and present (Al
Abadi, University of Melbourne) and several collaborators including
Amrit Singh (University of British Columbia), Olivier Chapleur (IRSTEA,
Paris), Antoine Bodein (Universite de Laval) - **it could be you too, if
you wish to be involved\!**.

The project started at the *Institut de Mathématiques de Toulouse* in
France, and has been fully implemented in Australia, at the *University
of Queensland*, Brisbane (2009 – 2016) and at the *University of
Melbourne*, Australia (from 2017). We focus on the development of
computational and statistical methods for biological data integration
and their implementation in `mixOmics`.

## Why this toolkit?

`mixOmics` offers a wide range of novel multivariate methods for the
exploration and integration of biological datasets with a particular
focus on variable selection. Single ‘omics analysis does not provide
enough information to give a deep understanding of a biological system,
but we can obtain a more holistic view of a system by combining multiple
‘omics analyses. Our `mixOmics` R package proposes a whole range of
multivariate methods that we developed and validated on many biological
studies to gain more insight into ‘omics biological studies.

## Want to know more?

www.mixOmics.org (tutorials and resources)

Our latest bookdown vignette:
<https://mixomicsteam.github.io/Bookdown/>.

## Different types of methods

We have developed 17 novel multivariate methods (the package includes 19
methods in total). The names are full of acronyms, but are represented
in this diagram. *PLS* stands for *Projection to Latent Structures*
(also called Partial Least Squares, but not our prefered nomenclature),
*CCA* for *Canonical Correlation Analysis*.

That’s it\! Ready\! Set\! Go\!

Thank you for using `mixOmics`\!

![](http://mixomics.org/wp-content/uploads/2012/04/framework-mixOmics-June2016.jpg)

## What’s New

#### September 2020

  - New biplot now available for `pca` family. See the examples in [this
    issue](https://github.com/mixOmicsTeam/mixOmics/issues/90)

#### April 2020

  - weighted consensus plots for DIABLO objects now consider
    per-component weights

#### March 2020

  - `plotIndiv` now supports (weighted) consensus plots for block
    analyses. See the example in [this
    issue](https://github.com/mixOmicsTeam/mixOmics/issues/57)

  - `plotIndiv(..., ind.names=FALSE)` [warning
    issue](https://github.com/mixOmicsTeam/mixOmics/issues/59) now fixed

#### January 2020

  - `perf.block.splsda` now supports calculation of combined AUC
  - `block.splsda` bug which could drop some classes with
    `near.zero.variance=TRUE` now fixed

#### November 2019

  - Parallel computing improved for `tune` and `perf` functions, and
    even more on Unix-like systems

  - Fixed margin error problem with `plotLoadings`. See the example in
    [this issue](https://github.com/mixOmicsTeam/mixOmics/issues/45)

  - `cim` bug which overestimated correlations for single component now
    fixed

  - `perf.sgccda` now supports calculation of average combined AUC

#### September 2019

  - You can now customise `auroc` plots in version 6.8.3. See example
    [here](https://github.com/mixOmicsTeam/mixOmics/issues/35)
