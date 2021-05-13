
# Version control through Git, GitHub & GitKraken for researchers

<!-- badges: start -->
[![Netlify Status](https://api.netlify.com/api/v1/badges/846e3c15-8af4-4bba-8fce-02ea13f42e53/deploy-status)](https://app.netlify.com/sites/rse-workshop-material-template/deploys)
[![Project Status: Active – The project has reached a stable, usable state and is being actively developed.](https://www.repostatus.org/badges/latest/active.svg)](https://www.repostatus.org/#active)
<!-- badges: end -->

Source of the website of a short course.

It is powered by [Hugo](https://gohugo.io/) and the following themes:

* [Hugo theme learn](https://github.com/matcornic/hugo-theme-learn)
* [Hugo theme reveal-hugo](https://github.com/dzello/reveal-hugo)

Slides for each section are listed in the menu and opened in a new tab (thanks to a [custom menu layout](/blob/master/layouts/partials/menu.html), compared to the original Hugo learn theme).

Some Markdown content is generated with [R Markdown](https://rmarkdown.rstudio.com/), using [hugodown](https://github.com/r-lib/hugodown/).

The website is deployed by [Netlify](https://www.netlify.com/).

### Why these tools?

Why use Hugo for both the website and slidedecks, and not, say Hugo+hugodown for pages and xaringan for slides?
This way the source of slides is html produced by Hugo from Markdown content.
It allows me to use:

* downlit syntax highlighting for slides created from R Markdown with hugodown output format;
* Chroma syntax highlighting for other languages;
* emojis! `:grin:` works in slides;
* Shortcodes in slides, should I choose to.

Also, because slides are in the content, they are indexed by the Hugo learn theme so searchable!


## Credits

The workshop materials website template is based on the [hugo-theme-learn](https://github.com/matcornic/hugo-theme-learn), [reveal-hugo](https://github.com/dzello/reveal-hugo) Hugo themes and further work and configuration by Maëlle Salmon for her course site on [**Scientific blogging with R Markdown**](https://github.com/maelle/rmd-blogging-course).


## Creating Content

All contect lives in the `content/` folder

To create a new chapter, ideally create a new folder within `content/` use

```
hugo new --kind chapter <chapter-folder>/_index.md
```

You can add further sections to the chapter with

```
hugo new <chapter-folder>/<section-title>.md
```

It is best to start the file name for new section with a zero padded number, indicating the order of the sections (for visual ordering of the files in your text editor). To set the ordering of each section in the navigation menu, use the `weight` argument in the YAML header of each file. Weights in the chapter YAML header specify the order of the chapters in the navigation panel while weights in normal sections refer to the internal ordering of sections within each chapter.

For more details, refer to the [hugo learn theme](https://learn.netlify.app/en/) documentation site.
