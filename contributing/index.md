---
layout: page
title: "Contributing"
description: ""
---
{% include JB/setup %}

### 1. Git the code
In order to contribute you will need to [fork the repo](https://github.com/vivint-guilds/app-guild/fork)

Then clone the repo to your machine.

###### remember to change USERNAME to your GitHub username.

```bash
$ git clone git@github.com:USERNAME/app-guild.git
$ cd app-guild
```

### 2. Run Jekyll Locally
In order to preview your blog locally you'll need to install the Jekyll ruby gem. Note gem dependencies will also be installed. You don't have to run a local version but it helps if you want to preview your content before publishing.

```bash
$ gem install jekyll
```

If you run into a problem please consult the original [Jekyll installation documentation](http://jekyllrb.com/docs/installation/). You can also [create a support issue](https://github.com/vivint-guilds/app-guild/issues/new) using GitHub Issues.

Once the gem is installed you can navigate to your app-guild directory. Once in the directory you'll run jekyll with server support:

```bash
$ cd app-guild
$ jekyll serve
```

Your blog is now available at: [http://localhost:4000/](http://localhost:4000/).

### 3. Create a Post
Create posts easily via rake task:

```bash
$ rake post title="Hello World"
```

The rake task automatically creates a file with properly formatted filename and YAML Front Matter. Make sure to specify your own title. By default, the date is the current date.

The rake task will never overwrite existing posts unless you tell it to.

### 4. Create a Page
Create pages easily via rake task:

```bash
$ rake page name="about.md"
```

Create a nested page:

```bash
$ rake page name="pages/about.md"
```

Create a page with a "pretty" path:

```bash
$ rake page name="pages/about"
# this will create the file: ./pages/about/index.html
```

The rake task automatically creates a page file with properly formatted filename and YAML Front Matter as well as includes the Jekyll Bootstrap "setup" file.

### 5. Publish
After you've added posts or made changes to your theme or other files, simply commit them to your git repo and push the commits up to GitHub.

```bash
$ git add .
$ git commit -m "Add new content"
$ git push origin master
```

After you have pushed your changes then you will go to http://github.com/USERNAME/app-guild and [create a pull request](https://help.github.com/articles/creating-a-pull-request/).

### 6. Customize
Jekyll-Bootstrap can be used as-is as a basic blogging platform. However there are plenty of ways to dig into deeper customization. The following outlines deeper Jekyll-Bootstrap customization techniques:

#### Themes

Jekyll-Bootstrap supports modular theming. Themes can co-exist and be enabled/disabled on demand. Editing, configuring, and creating themes is docummented in the [Theming](http://jekyllbootstrap.com/usage/jekyll-theming.html) section.

#### Blog Configuration

Jekyll and Jekyll-Bootstrap has a simple but powerful [Jekyll Configuration System](http://jekyllbootstrap.com/usage/blog-configuration.html). You can:

* Specify a custom permalink format for blog posts.
* Specify a commenting engine like disqus, intensedebate, livefyre, or custom.
* Specify an analytics engine like google, getclicky, or custom.

#### Programming Interface

The API pages document main data-structures and code available for use in Jekyll and Jekyll-Bootstrap. Consult these pages for how and where to use the data and code provided.

#### Jekyll Introduction

<span class="label label-primary">Highly Recommend</span>

I highly recommend reading the [Jekyll Introduction](http://jekyllbootstrap.com/lessons/jekyll-introduction.html) if you plan to customize your blog. The introduction is meant for core understanding of how and why Jekyll works the way it does. This will provide you with the proper context, knowledge-base, and fundamentals necessary to understand and be efficient in working with Jekyll and Jekyll-Bootstrap.
