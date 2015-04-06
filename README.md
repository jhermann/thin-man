# Thin Man

*Thin Man* backs up all metadata in your source tree of `git` repos.

![logo](https://raw.githubusercontent.com/jhermann/thin-man/master/docs/_static/img/logo.png)


## Overview

By recording the tree layout, `git` remotes and ‘refs’ of the typical
`~/src` directory containing your cloned `git` repos,
*Thin Man* can restore that structure later on,
and also sync it to other machines.

This can be also part of a backup strategy by only including that small
amount of metadata in a backup set, instead of duplicating all the data
that is available in remote locations anyway.

This of course assumes that your repositories are usually clean and don't
contain days of uncommitted work, and can be easily restored into
working shape by bootstrap scripts and the like.
But that's a given, right?
