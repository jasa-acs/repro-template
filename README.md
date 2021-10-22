JASA Sharing Reproducible Materials over Github
================

This GitHub repository contains a template structure for author(s) who
submit to JASA AC&S and Theory & Methods to include materials to
reproduce any analyses, visualizations, and tables.

## Why is template repository this useful?

The purpose of this template repository is to provide a mechanism for
author(s) to share their materials on Github. This enables the following
advantages for author(s):

1.  Data analyses (including code, narrative text, output, plots, etc)
    can be version controlled (or branched) allowing original author(s)
    to continue to develop the analyses or other data analysts to build
    off the analyses. Also iterations and changes to the analysis are
    then available via the check in history.
2.  The materials to reproduce the analyses could be directly copied to
    the JASA repository with `git clone` functionality.
3.  Others?

## How does the process work?

### Step 1

Author(s) create a public GitHub repository by

1.  Forking this template repository
2.  Using `git clone` and removing the `.git` file

### Step 2

Author(s) directly edit the files in the template repository by adding
the relevant files to the folders and/or `manuscript.Rmd`.

### Step 3

Author(s) use `git commit` to track changes over time and use `git push`
to push changes to a repository on the author(s) personal GitHub
account.

### Step 4

Author(s) submit a link to their GitHub repository as part of the [JASA
Reproducibility review
process](https://jasa-acs.github.io/repro-guide/).

### Step 5

JASA Associate Editors of Reproducible will review the materials in the
personal GitHub repository of the authors and submit a reproducibility
review as part of the standard JASA review process. Authors have the
opportunity to respond to the review by making changes and pushing their
changes to their personal GitHub repository.

**Should reviewers/editors be allow to provide pull requests?**

### Step 6

Once the manuscript is accepted, the materials in the author(s) personal
GitHub repository will be copied to the [JASA
repository](https://github.com/jasa-acs).

## Description of template structure using R

Two preferred file structures for submissions are shown below. The goals
in prescribing this structure are to make it easier for the
reproducibility reviewer to confirm the materials are sufficient for
reproducing the results as well as facilitating automated generation of
the outputs via Docker, Singularity, or Github Actions.

## Reproduciblity materials only

The first is for the case where reproducibility materials are being
provided and are separate from the manuscript.

    ## 
    ## project directory
    ##   |-- .here
    ##   |  o-- object of type(s):file
    ##   |-- README.md
    ##   |  o-- object of type(s):file
    ##   |-- renv/
    ##   |  o-- object of type(s):dir
    ##   |-- preprocessing/
    ##   |  o-- object of type(s):dir
    ##   |-- analysis/
    ##   |  o-- object of type(s):dir
    ##   |-- data/
    ##   |  o-- object of type(s):dir
    ##   o-- output/
    ##      o-- object of type(s):dir

## Reproducible document

The second is for manuscripts written as R Markdown documents.

    ## 
    ## project directory
    ##   |-- manuscript.rmd
    ##   |  o-- object of type(s):file
    ##   |-- renv/
    ##   |  o-- object of type(s):dir
    ##   |-- preprocessing/
    ##   |  o-- object of type(s):dir
    ##   o-- data/
    ##      o-- object of type(s):dir
