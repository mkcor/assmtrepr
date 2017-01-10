# Contributing

Fork this repository. Clone your fork. Your remote is named `origin` by
default (you can check this by running `$ git remote -v`). Add this remote:

    $ git remote add upstream git@github.com:mkcor/assmtrepr.git

It is standard to have an `origin` (you) and an `upstream` remote (gatekeeper).

Make sure your local `master` branch is in sync with the `upstream master`.
Create a feature branch.

## References

* R packaging http://r-pkgs.had.co.nz/
* GitHub flow https://guides.github.com/introduction/flow/
* Temporary library https://gist.github.com/jennybc/4ffc1607d07ed3b025dc

## Contributing an analysis

We (re)produce assessment reports in the form of
[vignettes](http://r-pkgs.had.co.nz/vignettes.html). Create a new vignette:

    > devtools::use_vignette("my_analysis")

As you hack, you may want to [check](http://r-pkgs.had.co.nz/check.html) the
work-in-progress package:

    > devtools::check()

Indeed, you want to make sure that your changes are free of common problems.

Once you are happy with your contribution, you want to build the package:

    > devtools::build()

This generates a tarball (`.tar.gz` file).

Next, you want to install this new version of the package in a temporary
library (somewhere *different* from the default R library trees). To check what
these default libraries are, run

    > .libPaths()
