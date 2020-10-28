---
output: hugodown::md_document
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "2015 07 23 r rmarkdown"
subtitle: ""
summary: ""
authors: []
tags: []
categories: []
date: 2020-10-28
lastmod: 2020-10-28
featured: false
draft: false

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: ""
  focal_point: ""
  preview_only: false

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects: []
rmd_hash: c425bfd180def20a

---

R Markdown
==========

This is an R Markdown document. Markdown is a simple formatting syntax for authoring HTML, PDF, and MS Word documents. For more details on using R Markdown see <http://rmarkdown.rstudio.com>.

You can embed an R code chunk like this:

<div class="highlight">

<pre class='chroma'><code class='language-r' data-lang='r'><span class='nf'><a href='https://rdrr.io/r/base/summary.html'>summary</a></span><span class='o'>(</span><span class='nv'>cars</span><span class='o'>)</span>

<span class='c'>#&gt;      speed           dist       </span>
<span class='c'>#&gt;  Min.   : 4.0   Min.   :  2.00  </span>
<span class='c'>#&gt;  1st Qu.:12.0   1st Qu.: 26.00  </span>
<span class='c'>#&gt;  Median :15.0   Median : 36.00  </span>
<span class='c'>#&gt;  Mean   :15.4   Mean   : 42.98  </span>
<span class='c'>#&gt;  3rd Qu.:19.0   3rd Qu.: 56.00  </span>
<span class='c'>#&gt;  Max.   :25.0   Max.   :120.00</span>

<span class='nv'>fit</span> <span class='o'>&lt;-</span> <span class='nf'><a href='https://rdrr.io/r/stats/lm.html'>lm</a></span><span class='o'>(</span><span class='nv'>dist</span> <span class='o'>~</span> <span class='nv'>speed</span>, data <span class='o'>=</span> <span class='nv'>cars</span><span class='o'>)</span>
<span class='nv'>fit</span>

<span class='c'>#&gt; </span>
<span class='c'>#&gt; Call:</span>
<span class='c'>#&gt; lm(formula = dist ~ speed, data = cars)</span>
<span class='c'>#&gt; </span>
<span class='c'>#&gt; Coefficients:</span>
<span class='c'>#&gt; (Intercept)        speed  </span>
<span class='c'>#&gt;     -17.579        3.932</span>
</code></pre>

</div>

Including Plots
===============

You can also embed plots. See Figure @ref(fig:pie) for example:

<div class="highlight">

<pre class='chroma'><code class='language-r' data-lang='r'><span class='nf'><a href='https://rdrr.io/r/graphics/par.html'>par</a></span><span class='o'>(</span>mar <span class='o'>=</span> <span class='nf'><a href='https://rdrr.io/r/base/c.html'>c</a></span><span class='o'>(</span><span class='m'>0</span>, <span class='m'>1</span>, <span class='m'>0</span>, <span class='m'>1</span><span class='o'>)</span><span class='o'>)</span>
<span class='nf'><a href='https://rdrr.io/r/graphics/pie.html'>pie</a></span><span class='o'>(</span>
  <span class='nf'><a href='https://rdrr.io/r/base/c.html'>c</a></span><span class='o'>(</span><span class='m'>280</span>, <span class='m'>60</span>, <span class='m'>20</span><span class='o'>)</span>,
  <span class='nf'><a href='https://rdrr.io/r/base/c.html'>c</a></span><span class='o'>(</span><span class='s'>'Sky'</span>, <span class='s'>'Sunny side of pyramid'</span>, <span class='s'>'Shady side of pyramid'</span><span class='o'>)</span>,
  col <span class='o'>=</span> <span class='nf'><a href='https://rdrr.io/r/base/c.html'>c</a></span><span class='o'>(</span><span class='s'>'#0292D8'</span>, <span class='s'>'#F7EA39'</span>, <span class='s'>'#C4B632'</span><span class='o'>)</span>,
  init.angle <span class='o'>=</span> <span class='o'>-</span><span class='m'>50</span>, border <span class='o'>=</span> <span class='kc'>NA</span>
<span class='o'>)</span>

</code></pre>

<div class="figure" style="text-align: center">

<img src="figs/pie-1.png" alt="A fancy pie chart." width="700px" />
<p class="caption">
A fancy pie chart.
</p>

</div>

</div>

