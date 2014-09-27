---
layout: post
title: ! 'New psanxiao.com'
date: 2014-09-27
categories:
- General
tags: []
status: publish
type: post
published: true
meta:
  _edit_last: '6'
  _wpcom_is_markdown: '1'
author:
  login: psanxiao
  email: psanxiao@gmail.com
  display_name: psanxiao
  first_name: ''
  last_name: ''
---
After many years using [Wordpress](https://wordpress.org/) as CMS for this blog, it is time to change. Wordpress is a very good solution for creating your own blog or personal page. It is very easy to use and very personalized by means of the incredible amount of themes and plugins. 

But, I wanted to try a simpler solution that could be possible to maintain in a easier way. Another reason to change was that I wanted to write and add new posts from [Sublime Text](http://www.sublimetext.com/), the text editor that I use, using [Markdown](http://en.wikipedia.org/wiki/Markdown). 

The solution that I finally chose is [JekyllBootstrap](http://jekyllbootstrap.com/). The main power of using this solution it is that all you need are text files, no database are need. Both, pages and posts are simple text files wrote in Markdown or html, if you prefer. Even the blog configuration is made by a text file also. All web is now in a git repository, in [github](http://github.com) actually, so it is very easy to manage changes. Also github pages support Jekyll, therefore no additional hosting is needed to make public the web.

Of course, there are a couple of limitations. For example, there are few themes or plugins available, or it has no a comments system integrated. For this last issue there is alternative. You can use any comments services like [Disqus](https://disqus.com/), for example. All you need to do in this case it is just configuring the comments provider into the JekyllBootstrap configuration file.

In order to migrate the old blog in Wordpress I found a couple of alternatives. The one I chose was exporting Worpress entries to a XML file and using a migration script as it explained in this [link](http://jbeckwith.com/2013/07/17/wordpress-to-jekyll/).

Finally, I configured my domain, psanxiao.com, to point to the gh-page of the github repository following the oficial [github instructions](https://help.github.com/articles/setting-up-a-custom-domain-with-github-pages). There are still some adjustments, but this new infrastructure is already running.