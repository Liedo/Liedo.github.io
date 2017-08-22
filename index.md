---
layout: default
title: forecasting evaluation
tagline: technical documentation for JDemetra$+$ using GitHub Pages
description: Minimal tutorial on making a simple website with GitHub Pages
---

# Using $$ \LaTeX $$ and Github pages to document the software JDemetra+

[Github Pages](https://pages.github.com) provide a simple way to make a
website using
[Markdown](https://daringfireball.net/projects/markdown/) and
[git](https://git-scm.com). 

We will also use [MathJax](https://www.mathjax.org/) 
to interpret correctly the Latex code included in the pages (just change the _layouts/default.html file 
by adding right before the header the following lines: 

``` 
<script type="text/x-mathjax-config">MathJax.Hub.Config({tex2jax: {inlineMath: [['$','$'], ['\\(','\\)']]}});</script>
```

```
<script src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML" type="text/javascript" ></script>  
)  
```

Does $$ \LaTeX $$ work here?  $$ \phi $$. It is working well, but it seems that you can only insert 
mathematical expressions, like 
``` $$ \phi $$
``` 
Equation arrays and other possibilities offered by $$ \LaTeX $$ will not be correctly interpreted by MathJax.


With [GitHub Pages](https://pages.github.com), you just write things in
[Markdown](https://daringfireball.net/projects/markdown/),
[GitHub](https://github.com) hosts the site for you, and you just push
material to your GitHub repository with `git add`, `git commit`, and
`git push`.


The sites use [Jekyll](https://jekyllrb.com/), a
[ruby](https://www.ruby-lang.org/en/) [gem](https://rubygems.org/), to
convert Markdown files to html, and this part is done
automatically when you push the materials to the `gh-pages` branch
of a GitHub repository.

# Forecasting Evaluation in JDemetra+:

- [Notation](pages/notation.md)
- [Making an independent website](pages/independent_site.html)
- [Making a personal site](pages/user_site.html)
- [Making a site for a project](pages/project_site.html)
- [Making a jekyll-free site](pages/nojekyll.html)
- [Testing your site locally](pages/local_test.html)
- [Resources](pages/resources.html)

If anything here is confusing (or _wrong_!), or if I've missed
important details, please
[submit an issue](https://github.com/kbroman/simple_site/issues), or (even
better) fork [the GitHub repository for this website](https://github.com/kbroman/simple_site),
make modifications, and submit a pull request.

---

The source for this minimal tutorial is [on github](https://github.com/kbroman/simple_site).

Also see my [tutorials](http://kbroman.org/pages/tutorials) on
[git/github](http://kbroman.org/github_tutorial),
[GNU make](http://kbroman.org/minimal_make),
[knitr](http://kbroman.org/knitr_knutshell),
[R packages](http://kbroman.org/pkg_primer),
[data organization](http://kbroman.org/dataorg),
and [reproducible research](http://kbroman.org/steps2rr).
