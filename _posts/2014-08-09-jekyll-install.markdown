---
layout: post
title:  "How we installed Jekyll"
date:   2014-08-09 01:01:27
categories: jekyll update
---

# How we set up Jekyll

## 1. Github setup

First we created a repo.

Next, we created a new branch of the repo called 'gh-pages'. Github automatically treats branches named 'gh-pages' as public Github pages (which runs on Jekyll). Free hosting and version control!

## 2. Clone the repo locally

Within the Github for Mac app, we clone the branch to our Desktop. Any location on the computer will do, though the app told us that Dropbox can corrupt things (probably due to latency).

## 3. Install Jekyll locally

We then installed Jekyll locally. We want a local install so that we can develop locally, see bugs, before committing and pushing live.

{% highlight ruby %}
sudo gem install jekyll
{% endhighlight %}

## 4. Make the Jekyll file structure

We then ask jekyll to create a new site in the same folder we cloned the 'gh-pages' branch to. You may see an error because your original clone added files (like a readme, license, or gitignore file). If you temporarily move these, then creat the site, and move them back, you should be fine. 

This will create a bunch of files in the folder (not including _site, which is where the static html pages go).

## 5. Create the Jekyll site

Next, we ask Jekyll to build the site locally, and automatically rebuild with any changes I make to the files in the desktop folder. This creates the _site folder that houses the actual HTML pages.

{% highlight ruby %}
jekyll serve --watch
{% endhighlight %}

## 6. Fix _config.yml
To properly link all the site files together (CSS, incudes, HTML, etc.), we need to edit _config.yml. The big thing is to change the root directory to your project name (/project-name)

## 7. Push to Github (and go live)

Finally, we can and commit and sync the local 'gh-pages' branch to Github.

After a few minutes, I should be able to visit jeffrlaw.github.io/project-name.
