---
layout: post
title:  "Starting a blog"
date:   2024-02-01 
---

## tl;dr?
We have recently put a [GitHub Enterprise Server] [github enterprise server] into operation. For administrative purposes, we have some workflows around the [GitHub Enterprise Server] [github enterprise server]. To gain more knowledge, I had to dive a little deeper into [GitHub] [github] / [GitHub Enterprise Server] [github enterprise server]. During my learning experience, I stumbled upon the possibility to run blogs / website on [GitHub] [github].
Below is a very simple description of how such a blog can be implemented using the [Ruby] [ruby] web framework [Jekyll] [jekyll].

## Create appropriate repository
In your [GitHub] [github] account create a repository named `<github_username>.github.io`. If you push some [Jekyll] [jekyll] code into this repo, [GitHub] [github] will render the site and it is available via the link `http://<github_username}.github.io`, e.g. `http://florianmaier101178.github.io`.

## Installation of jekyll on ubuntu linux
{% highlight bash %}
$ sudo apt install -y ruby-dev
$ sudo gem install jekyll
{% endhighlight %}

## Setup of blog
{% highlight bash %}
$ jekyll new florianmaier101178.github.io
$ cd florianmaier101178.github.io
$ git init .
$ git remote add origin git@github.com:florianmaier101178/florianmaier101178.github.io.git
$ git push origin master
{% endhighlight %}

## Run the blog locally
{% highlight bash %}
$ jekyll serve
$ open http://localhost:4000
{% endhighlight %}

## Minima theme
The blog is based on the [minima theme] [minima]. 
I did some customizations of the footer and the main page. These adaptions are applied in the subdirectories `_includes` and `_layouts` of the repository. Both directories are copied from the [minima code] [minima].

[minima]: https://github.com/jekyll/minima/releases/tag/v2.5.1
[github enterprise server]: https://docs.github.com/en/enterprise-server@3.11
[github]: https://github.com/
[jekyll]: https://jekyllrb.com/
[ruby]: https://www.ruby-lang.org/en/
