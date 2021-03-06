Reflections for the powers R package
================
Lisa Wei
2017-11-28

Package can be accessed via this link: [powers](https://github.com/suminwei2772/powers).

I had quite a difficult time developing and building the `powers` R package. Below are some issues I came across and approaches I used to try to solve them.

1.  I couldn't install the package properly at first. I think one problem was that my `powers` repo was set to `private` in Settings. I tried several things, including:

    -   Putting in the `auth_token` which I saw online allowed the user to access a private repo, but that didn't work

    -   Since I opened a Github repo first, cloned it in RStudio locally, and then set up a new R package project under this repo, I created a branch folder which contained by R package. This meant that I couldn't just use `github_install("username/repo")` since I had to specify the branch name as well. But I tried `github_install("username/repo", branch="powers")` but was not successful in installation.

    -   Made my `powers` repo public, and that seemed to have solved the issue.

2.  I kept on forgetting all the functions and commands that need to be executed to properly generate the documentations for each function (using `roxygen2::roxygenize()`), build the vignettes in the right folder locations (first `knit` and THEN do `devtools::build_vignettes()`), execute tests using `devtools::test()`. It was a lot to keep track of.

3.  I didn't quite understand what is meant by `include at least three unit tests for every function that is exported.` I was only able to write one for success and one test for failure in the `test_square.R` file for each function.

4.  Finally, I had trouble finding a way to visualize the `vignette` file in a user-readable way. I tried the following in the `my_vignette.Rmd` file:

<!-- -->

    output:
      github_document:
        toc: true
      rmarkdown::html_vignette:
    vignette: >
      %\VignetteIndexEntry{Using the `powers` package}
      %\VignetteEngine{knitr::rmarkdown}
      %\VignetteEncoding{UTF-8}

But I was never able to generate the Markdown file. So in the end, I decided to link the html file to my README.md and used the `https://htmlpreview.github.io/?https://github.com/suminwei2772/powers/blob/master/inst/doc/my_vignette.html` command which allows html preview on Github.
