---
author: Ben Tyler Elliott
date: 2022-07-25 11:58:47 +07:00
image: "/assets/img/posts/"
layout: post
published: true
repo: "https://github.com/obverter/"
tags: []
title: Title
---

Hook

<!-- more -->

Content

## Section

### Subsection

<!-- This code:

```latex
$$
  D = \left(\begin{matrix}
  1 & -1 & & & & \\
  &    & \cdots &   & \\
  &    &        & 1 & -1
 \end{matrix}
 \right)
$$
```
yields this:

$$
D = \left(\begin{matrix}
  1 & -1 & & & & \\
  &    & \cdots &   & \\
  &    &        & 1 & -1
\end{matrix}
\right)
$$ -->

A matrix in text must be set smaller: $$ \bigl(\begin{smallmatrix}a & b \\ c & d\end{smallmatrix} \bigr) $$ to not increase leading in a portion of text. The way this inline matrix is written is: ```$$ \bigl(\begin{smallmatrix}a & b \\ c & d\end{smallmatrix} \bigr) $$```

### No blank lines between Markdown list items

### Sidenote Example

+ Split Bregman iteration {% sidenote 1 'Goldstein, T. and Osher, S. (2009). The split Bregman method for l1-regularized problems. SIAM J. Img. Sci., 2:323-343.' %}
+ Dykstra's alternating projection algorithm {% sidenote 2 'Dykstra, R. L. (1983). An algorithm for restricted least squares regression. J. Amer. Statist. Assoc., 78(384):837-842.' %}
+ Proximal point algorithm applied to the dual
+ Numerous applications in statistics and machine learning: lasso, gen. lasso, graphical lasso, (overlapping) group lasso, ...
+ Embraces distributed computing for big data {% sidenote 3 'Boyd, S., Parikh, N., Chu, E., Peleato, B., and Eckstein, J. (2011). Distributed optimization and statistical learning via the alternating direction method of multipliers. Found. Trends Mach. learn., 3(1):1-122.' %}

### Liquid tag parsing strangeness

Example of the proper way to write an url inside a *Liquid* full-width image tag.

This code: ```{{ '{% fullwidth "assets/img/rhino.png" "Tuftes pet rhino (via <a href=\"//www.edwardtufte.com/tufte/\">Edward Tufte</a>)" ' }} %}```

produces the following image with a title. Notice that I have had to escape the double quotes in the HTML with a backslash. Also, the example above leaves out the single quote in 'Tufte's" because of the topsy-turvy way that you have to escape the escapes in code sections that are used for illustrative purposes in this text. Bottom line is that there are occasionally some odd interactions between the Markdown parser, custom *Liquid* tags and HTML.
{% fullwidth "assets/img/rhino.png" "Tufte's pet rhino (via <a href=\"//www.edwardtufte.com/tufte/\">Edward Tufte</a>)" %}

```Liquid
[It is] notable that the Feynman lectures (3 volumes) write about all of physics in 1800 pages, using only 2 levels of hierarchical headings: chapters and A-level heads in the text. It also uses the methodology of *sentences* which then cumulate sequentially into *paragraphs*, rather than the grunts of bullet points. Undergraduate Caltech physics is very complicated material, but it didn’t require an elaborate hierarchy to organize.
<cite>[http://www.edwardtufte.com/bboard/q-and-a-fetch-msg?msg_id=0000hB](http://www.edwardtufte.com/bboard/q-and-a-fetch-msg?msg_id=0000hB)</cite>
```
