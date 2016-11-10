---
layout: post
title:  "About Jekyll"
categories: jekyll update
---

This is the base Jekyll theme. You can find out more info about customizing your Jekyll theme, as well as basic Jekyll usage documentation at [jekyllrb.com](http://jekyllrb.com/)

You can find the source code for Jekyll at
{% include icon-github.html username="jekyll" %} /
[jekyll](https://github.com/jekyll/jekyll)

## about *minima* theme
You can find the source code for the Jekyll new theme at:
{% include icon-github.html username="jekyll" %} /
[minima](https://github.com/jekyll/minima)

## more themes ?
  - [jekyllthemes.org](http://jekyllthemes.org)

## about markup : *kramdown*

Most pages are written using [kramdown syntax](http://kramdown.gettalong.org/).

## about Jekyll + Github pages

  - [Official GHPages help](https://pages.github.com/)

## github-pages gem

> A simple Ruby Gem to bootstrap dependencies for setting up and maintaining a
> local Jekyll environment in sync with GitHub Pages.

In my `Gemfile` I found advice to use
[github-pages](https://rubygems.org/gems/github-pages) gem whose source code is at
[GH:pages-gem](https://github.com/github/pages-gem)

But there is also a notice in <http://jekyllrb.com/docs/github-pages/>
suggesting to include this instead:

```rb
ruby source 'https://rubygems.org'
require 'json'
require 'open-uri'
versions = JSON.parse(open('https://pages.github.com/versions.json').read)
gem 'github-pages', versions['github-pages']
```

in order to be able to update gems accordingly with github pages.
See <https://pages.github.com/versions/> .

*github-pages* depends on *jekyll* itself and many other plugins,
this is why you can remove the *jekyll* line from Gemfile.
