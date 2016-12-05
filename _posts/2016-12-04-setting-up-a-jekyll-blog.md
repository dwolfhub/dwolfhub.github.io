---
layout: post
title:  "Setting Up a Jekyll Blog on Github Pages"
date:   2016-12-04 16:49:08 -0600
categories: jekyll blog guide
comments: true
---

In this article, I'll walk you through creating a blog website quickly and easily
using the static site generator [Jekyll](https://jekyllrb.com). This article
assumes you have a general knowledge of markdown and using the command line.
Also that you are using a linux-based system with `git`, `ruby` and `gem`
installed. You can use the `which` command to make sure they are installed. If
the program is in your PATH, these commands will print out the location of the
program. If it prints out nothing, the program isn't installed.

{% highlight bash %}
which git
which ruby
which gem
{% endhighlight %}

The methods in this guide were used to create this site and I thought I would
share the wealth.


## Installing Jekyll

The recommended way to install Jekyll is with gem. Use the following command
to install Jekyll globally on your system.

{% highlight bash %}
sudo gem install jekyll
{% endhighlight %}

When I ran this on my Macbook I got an "Operation not permitted" error. I ended
up having to specify to gem where the binary files are located using the `-n`
flag.

{% highlight bash %}
sudo gem install jekyll
sudo gem install -n /usr/local/bin jekyll
{% endhighlight %}

Once you get it installed you should have the jekyll command available.

{% highlight bash %}
which jekyll
/usr/local/bin/jekyll
{% endhighlight %}


## Creating The Site

To create your new site, use the `jekyll new` command, specifying the folder for
your site.

{% highlight bash %}
jekyll new my-new-site
{% endhighlight %}

Move into the new folder jekyll has created and initialize a git repository.
{% highlight bash %}
cd my-new-site
git init
{% endhighlight %}

Configuring a jekyll site is done in the `_config.yml` file. Open up that file
and enter information about your new blog site.


## Setting Up The Repo

Log into your [Github](https://github.com) account and create a new repository.
**Important:** the name of the repository has to be in this format:
`your-github-username.github.io`. This is going to end up being the URL of your
site, but Github will also let you point a custom domain at it.

