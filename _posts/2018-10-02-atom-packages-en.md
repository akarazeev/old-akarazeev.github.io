---
title: Packages for Atom Text Editor
date: 2018-10-02 18:00:00 +03:00
tags:
- Atom
- Text Editor
- Programming
- Packages
layout: single
---

Since I've been using [Atom](https://atom.io) for a pretty long time, I decided to write a few words about it.

One of the main points for me are: (1) it's open sourced, all sources can be found in [corresponding repository](https://github.com/atom/atom); (2) its functionality can be extended using `packages`.

So I decided to save the list of my installed packages: [atom-packages.txt]({{ site.url }}{{ site.baseurl }}/data/atom-packages.txt).

After installation of Atom itself, these packages from file "atom-packages.txt" can be installed with the following command: `apm install --packages-file atom-packages.txt`

And with this command I saved the list of installed packages to file "atom-packages.txt": `apm list --installed --bare > atom-packages.txt`.

Spell checking for Russian and English languages: `Cmd + ,` -> `Packages` -> Search for "spell-check" -> `Settings` -> Set the value “en-US, ru-RU” for `Locales` (that's how to set up any installed package).

Some of the packages assume that corresponding Python-libraries are already installed (e.g. `pycodestyle`). Most likely the execution of the following commands will be sufficient:
```
pip install --upgrade pycodestyle
pip install --upgrade pyflakes
pip install --upgrade mypy
```

A few words about [MyPy](http://mypy-lang.org/index.html): it's a static type checker for Python. I recommend to uncheck the following items in the settings of `linter-mypy` package to avoid multiple `warnings` in projects where typing is not necessary: `Disallow Untyped Defs`, `Disallow Any Expr` and `Warn Missing Imports`.

My Theme: both `UI Theme` and `Syntax Theme` are “One Light”.
