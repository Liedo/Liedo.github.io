---
layout: default
title: forecasting evaluation
tagline: Technical documentation for JDemetra$+$ using GitHub Pages
description: Minimal tutorial on making a simple website with GitHub Pages
---

<div class="jumbotron">
<h1> Time Series Concepts for JDemetra+</h1>
<p> Prototype website using Latex to document the software JDemetra+</p>
</div>

<p class="float-right d-md-none">
<button type="button" class="btn btn-primary btn-sm" data-toggle="offcanvas">Toggle nav</button>
</p>

   
[Github Pages](https://pages.github.com) provide a simple way to make a
website using
[Markdown](https://daringfireball.net/projects/markdown/) and
[git](https://git-scm.com). 

We will also use [MathJax](https://www.mathjax.org/) 
to interpret correctly the Latex code included in the pages. Simply change the ```_layouts/default.html``` file 
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
, and it will be interpreted as $ \phi $. Syntax:
- [Kramdown quick reference](https://kramdown.gettalong.org/quickref.html) and [Kramdown syntax for mathematics](https://kramdown.gettalong.org/syntax.html#math-blocks)
- [MathJax Tex and Latex support](http://docs.mathjax.org/en/latest/tex.html) and [ongoing issues](https://github.com/mathjax/MathJax-docs/issues)

---

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
[submit an issue](https://github.com/Liedo/Liedo.github.io/issues), or (even
better) fork [the GitHub repository for this website](https://github.com/Liedo/Liedo.github.io),
make modifications, and submit a pull request.

<button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarsExampleDefault" aria-controls="navbarsExampleDefault" aria-expanded="false" aria-label="Toggle navigation">
   <span class="navbar-toggler-icon"></span>
</button>
	  
<div class="col-6 col-md-3 sidebar-offcanvas" id="sidebar">
  <div class="list-group">
    <a href="https://liedo.github.io/pages/dmtest.html" class="list-group-item active">Diebold-Mariano Test</a>
    <a href="https://liedo.github.io/pages/encompassing.html" class="list-group-item">Encompassing Test</a>
    <a href="https://liedo.github.io/pages/bias.html" class="list-group-item">Bias and Inefficiency</a>
   </div>
  </div><!--/span-->
---

The source for this material is [on github](https://github.com/Liedo/Liedo.github.io)
