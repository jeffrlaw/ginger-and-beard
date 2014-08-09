---
layout: post
title:  "How we installed Jekyll"
date:   2014-08-09 01:01:27
categories: jekyll update
---

# Is this confusing or what?

First we created a repo.

We then created a new branch of the repo 'gh-pages'. This automatically treats the HTML files as Github pages (which runs on Jekyll). Free hosting!

Within the Github for Mac app, we clone the branch/repo to our Desktop (apparently Dropbox can corrupt things)

We then installed Jekyll locally. We want a local install so that we can develop locally, see bugs, before committing and pushing live.

sudo gem install jekyll

We then ask jekyll to create a new site to the same Desktop folder.

This will create a bunch of files in the folder.

We ask jekyll to serve locally and automatically rebuild with any changes I make to the files in the desktop folder.

jekyll serve --watch

This will take the files and create a new _site folder with the actual website in it.

I can now commit and push to Github.

Within _config.yml, change the root directory to /project-name

After a few minutes, I should be able to visit jeffrlaw.github.io/project-name.