---
title: How I built this website
author: Francis Leblanc
date: '2020-06-29'
slug: how-i-built-this-website
categories:
  - website
tags:
  - R Markdown
  - blogdown
  - Hugo
subtitle: ''
summary: ''
authors: []
lastmod: '2020-06-29T13:48:09-04:00'
featured: no
image:
  caption: ''
  focal_point: ''
  preview_only: no
projects: []
toc: true
---

## Why this post

As a first post, it seemed appropriate to document the process of building this website and regroup resources for future use and help some other users. I entertained the idea of a personal website since I started my graduate studies in bioinformatics to showcase my work, but also build a platform that will extend outside the frame of my thesis. Using RMarkdown as my main work document, the package [**blogdown**](https://bookdown.org/yihui/blogdown/) is the perfect fit (almost).

## Resources I used

<iframe width="560" height="315" src="http://www.youtube.com/embed/vVHZ76OwPow" frameborder="0" allowfullscreen></iframe>

<details>
  <summary>Videos</summary>

  
  #### This video (and others in this series) shows how to get your site running on [**netlify**](https://app.netlify.com/) for free!

<iframe width="560" height="315" src="http://www.youtube.com/embed/vVHZ76OwPow" frameborder="0" allowfullscreen></iframe>

  
  #### This video goes trough the customization options of the academic theme.

  <iframe width="560" height="315" src="http://www.youtube.com/embed/ox_Ue9yzf-0" frameborder="0" allowfullscreen></iframe>
  
  <br> 

</details>


<details>
	<summary>Web resources</summary>

* [**blogdown**](https://bookdown.org/yihui/blogdown/) R book details most steps to get you going.
	
* [**Academic**](https://sourcethemes.com/academic/docs/) details how to customize this Hugo theme within the parameters they have made easy to modify.

</details>

<br>

There are many themes available, from complex to simple on [**Hugo site**](https://themes.gohugo.io/). The current theme is [**Academic**](https://themes.gohugo.io/academic/), a complex theme. It conveniently has many templates and functions that allow referencing publications, projects or posts and sharing them. The downside of it's complexity is that customizing it is difficult. One feature I tryed (and failed) to change is allowing a TOC to be displayed with posts rendered from .Rmd or .RMarkdown files. 

I found a solution for .md files [**here**](https://github.com/gcushen/hugo-academic/issues/1520). So for now, I simply set `toc: true` if the file is .md and `toc: false` if it is a .Rmd since the `<root dir>/layouts/_default/single.htm` has to be the same for both files.

```html
{{- define "main" -}}
{{ if .Params.toc }}
<div class="container-fluid docs">
    <div class="row flex-xl-nowrap">
      <div class="d-none d-xl-block col-xl-2 docs-toc">
        <ul class="nav toc-top">
          <li><a href="#" id="back_to_top" class="docs-toc-title">{{ i18n "on_this_page" }}</a></li>
        </ul>
        {{ .TableOfContents }}
        {{ partial "docs_toc_foot" . }}
      </div>
      <main class="col-12 col-md-0 col-xl-10 py-md-3 pl-md-5 docs-content" role="main">
{{ end }}
        <article class="article">
            {{ partial "page_header" . }}
            <div class="article-container">
              <div class="article-style">
                {{ .Content }}
              </div>
              {{ partial "page_footer" . }}
            </div>
        </article>
  {{ if .Params.toc }}
      </main>
    </div>
  </div>
  {{ end }}
{{- end -}}
```

## The few issues I had (*that may save you time*)

1. Change the URL in `<root dir>/config.toml` for the site after netlify is running to have sharable posts working.
2. Create new posts, courses or add publications with the addin button of Rstudio.
3. If you have a lot of changes (new files) to commit, git may crash if when you try to stage them in Rstudio. I use the Tools>shell... `git add .` then you can commit either from Rstudio of from the shell and it should work. If git crashed, you may have to go delete the `.git/index.lock` by command line (if you are using windows the directory won't be visible) `cd <root dir>/.git/` then `rm index.lock`.
4. If you have accents in you path (even before your `root dir` where the website project is located), git won't work properly and you may end up with a blank git tab in Rstudio. 

