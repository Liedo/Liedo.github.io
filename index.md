---
layout: default
title: forecasting evaluation
tagline: technical documentation for JDemetra$+$ using GitHub Pages
description: Minimal tutorial on making a simple website with GitHub Pages
---

# Prototype web page using  $$ \LaTeX $$  to document the software *J*Demetra*+*

[Github Pages](https://pages.github.com) provide a simple way to make a
website using
[Markdown](https://daringfireball.net/projects/markdown/) and
[git](https://git-scm.com). 

We will also use [MathJax](https://www.mathjax.org/) 
to interpret correctly the Latex code included in the pages. Simply change the "_layouts/default.html" file 
by adding the following lines before the header: 

- Specify delimiters for inline mathematics: 
``` 
<script type="text/x-mathjax-config">MathJax.Hub.Config({tex2jax: {inlineMath: [['$','$'], ['\\(','\\)']]}});</script>
```

- Configuration of automatic equation numbering:
``` 
MathJax.Hub.Config({
  TeX: { equationNumbers: { autoNumber: "AMS" } }
});
``` 


- Load Mathjax.js: 
```
<script src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML" type="text/javascript" ></script>    
```

Jekyll's default markdown parser, kramdown, requires you to use ```$$ ... $$``` for both inline and display style,
so you could  insert mathematical expressions such as  
``` $$ \phi $$
``` 
, and it will be interpreted as $ \phi $. However, I am not sure how we could use other possibilities offered by $$ \LaTeX $$, 
e.g. the use of equation arrays, and make sure MathJax ([see Tex and Latex support](http://docs.mathjax.org/en/latest/tex.html)) interprets them correctly.


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

If anything here is confusing (or _wrong_!), or if I've missed
important details, please
[submit an issue](https://github.com/kbroman/simple_site/issues), or (even
better) fork [the GitHub repository for this website](https://github.com/kbroman/simple_site),
make modifications, and submit a pull request.

# Forecasting Evaluation in *J*Demetra*+*:
## [Notation](pages/notation.md)
## [Diebold-Mariano Test](pages/dmtest.md)
## [Encompassing Test](pages/encompassing.md)
## [Bias and Efficiency](pages/bias.md)



---

The source for this minimal tutorial is [on github](https://github.com/kbroman/simple_site).

Also see my [tutorials](http://kbroman.org/pages/tutorials) on
[git/github](http://kbroman.org/github_tutorial),
[GNU make](http://kbroman.org/minimal_make),
[knitr](http://kbroman.org/knitr_knutshell),
[R packages](http://kbroman.org/pkg_primer),
[data organization](http://kbroman.org/dataorg),
and [reproducible research](http://kbroman.org/steps2rr).
