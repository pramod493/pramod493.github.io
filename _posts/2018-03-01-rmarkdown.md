---
layout: default
title: "Automatically generate HTML report from RMarkdown"
date: 2018-03-01
---

RMarkdown (Rmd) is commonly accessed via RStudio interface. It supports export to HTML, markdown, PDF and MS-Word.

A sample Rmd file consists of yams header, content and code block enclosed in {r}

 --- 
title: "sample report" 
author: "doc-author" 
date: "March 01, 2018"
 output:
   html_document
 ---  

The content goes here. It can include markdown, images, and Latex equations. 

```{r} 
 ## R code goes here
 ``` 

R provides a variety of options to process and visualize data. We can leverage this to create (static) reports.

> This post has been copied from the blog.
