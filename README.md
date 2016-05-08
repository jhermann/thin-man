# Thin Man

*Thin Man* backs up all metadata in your source tree of `git` repos.

![logo](https://raw.githubusercontent.com/jhermann/thin-man/master/docs/_static/img/logo.png)

 [![Travis CI](https://api.travis-ci.org/jhermann/thin-man.svg)](https://travis-ci.org/jhermann/thin-man)
 [![Coveralls](https://img.shields.io/coveralls/jhermann/thin-man.svg)](https://coveralls.io/r/jhermann/thin-man)
 [![GitHub Issues](https://img.shields.io/github/issues/jhermann/thin-man.svg)](https://github.com/jhermann/thin-man/issues)
 [![License](https://img.shields.io/pypi/l/thin-man.svg)](https://github.com/jhermann/thin-man/blob/master/LICENSE)
 [![Development Status](https://pypip.in/status/thin-man/badge.svg)](https://pypi.python.org/pypi/thin-man/)
 [![Latest Version](https://img.shields.io/pypi/v/thin-man.svg)](https://pypi.python.org/pypi/thin-man/)
 [![Download format](https://pypip.in/format/thin-man/badge.svg)](https://pypi.python.org/pypi/thin-man/)
 [![Downloads](https://img.shields.io/pypi/dw/thin-man.svg)](https://pypi.python.org/pypi/thin-man/)


## Overview

By recording the tree layout, `git` remotes and ‘refs’ of the typical
`~/src` directory containing your cloned `git` repos,
*Thin Man* can restore that structure later on,
and also sync it to other machines.

This can be also part of a backup strategy by only including that small
amount of metadata in a backup set, instead of duplicating all the data
that is available in remote locations anyway.

That of course assumes that your repositories are usually clean and don't
contain days of uncommitted work, and can be easily restored into
working shape by bootstrap scripts and the like.
But that's a given, right?


## Installation

*Thin Man* can be installed via ``pip install thin-man`` as usual,
see [releases](https://github.com/jhermann/thin-man/releases) for an overview of available versions.
To get a bleeding-edge version from source, use these commands:

```sh
repo="jhermann/thin-man"
pip install -r <(curl -skS "https://raw.githubusercontent.com/$repo/master/requirements.txt")
pip install -UI -e "git+https://github.com/$repo.git#egg=${repo#*/}"
```

See [Contributing](#contributing) on how to create a full development environment.

To add bash completion, read the [Click docs](http://click.pocoo.org/4/bashcomplete/#activation) about it,
or just follow these instructions:

```sh
cmdname=thin-man
mkdir -p ~/.bash_completion.d
( export _$(tr a-z- A-Z_ <<<"$cmdname")_COMPLETE=source ; \
  $cmdname >~/.bash_completion.d/$cmdname.sh )
grep /.bash_completion.d/$cmdname.sh ~/.bash_completion >/dev/null \
    || echo >>~/.bash_completion ". ~/.bash_completion.d/$cmdname.sh"
. "/etc/bash_completion"
```


## Usage

…


## Contributing

To create a working directory for this project, call these commands:

```sh
git clone "https://github.com/jhermann/thin-man.git"
cd "thin-man"
. .env --yes --develop
invoke build --docs test check
```

See [CONTRIBUTING](https://github.com/jhermann/thin-man/blob/master/CONTRIBUTING.md) for more.

[![Throughput Graph](https://graphs.waffle.io/jhermann/thin-man/throughput.svg)](https://waffle.io/jhermann/thin-man/metrics)


## References

**Similar Projects**

* [tony/vcspull](https://github.com/tony/vcspull)
* [earwig/git-repo-updater](https://github.com/earwig/git-repo-updater)

**Tools**

* [Cookiecutter](http://cookiecutter.readthedocs.io/en/latest/)
* [PyInvoke](http://www.pyinvoke.org/)
* [pytest](http://pytest.org/latest/contents.html)
* [tox](https://tox.readthedocs.io/en/latest/)
* [Pylint](http://docs.pylint.org/)
* [twine](https://github.com/pypa/twine#twine)
* [bpython](http://docs.bpython-interpreter.org/)
* [yolk3k](https://github.com/myint/yolk#yolk)

**Packages**

* [Rituals](https://jhermann.github.io/rituals)
* [Click](http://click.pocoo.org/)


## Acknowledgements

…
