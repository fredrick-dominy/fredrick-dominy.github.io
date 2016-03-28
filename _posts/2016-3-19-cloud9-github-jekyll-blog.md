---
author: Fredrick Dominy
title: Cloud9 & Github to Create a Jekyll Blog
layout: post
comments: true
tags:
- github
- cloud9
- blog
---

Fairly easy to do with a minor authentication hiccup...

I referenced several articles and found these links to be very helpful:

* [Running Jekyll on Cloud9 - By Jean-François L'Heureux](http://jflh.ca/2016-01-18-running-jekyll-on-cloud9/)
* [Barry Clark's - Build A Blog With Jekyll And GitHub Pages](https://www.smashingmagazine.com/2014/08/build-blog-jekyll-github-pages/)
* [Static Websites with Jekyll - By Ryan Irelan](https://www.google.com/url?q=https%3A%2F%2Fapp.pluralsight.com%2Flibrary%2Fcourses%2Fstatic-websites-with-jekyll%2Fdescription&sa=D&sntz=1&usg=AFQjCNHf76ZNa8T97LfX32fNtbKKWysPpw)
* [Github Guides](https://guides.github.com/features/mastering-markdown/)
* [Jekyll Tips](http://jekyll.tips/)

Opening a project on [C9.io](https://c9.io/) is very easy and free. You can have as many projects as you like as long as they are not private.

I chose a custom project with no attached github repo, as I created it a little later in the process. Once the environment booted I ran:

```
gem install github-pages
```

Then, I forked Barry Clark's [jekyll-now repository](https://github.com/barryclark/jekyll-now) and changed the title to `fredrick-dominy.github.io` - which is necessary for github's automatic hosting.

I cloned the repo into my cloud9 environment and began configuring the site to my needs.

Jean-Fancois found that in order to view the blog with jekyll serve you need to assign flags for the host, IP, and config. The Run command looks like this:

``` bash
jekyll serve --host $IP --port $PORT --config _config.yml,_local_config.yml
```

... where _local_config.yml is a file you create with the following text.


``` yaml
url: "https://fredweb-blog-freximus.c9users.io"
baseurl: ""
```

Once you have the server up and running you can see begin to modify the content.

## Issues

I attempted to create an SSH clone to bypass the authentication of pushing to github, however I hit some roadblocks.  I may investigate later when it annoys me more.
