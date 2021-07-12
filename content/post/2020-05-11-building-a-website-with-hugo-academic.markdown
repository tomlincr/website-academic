---
title: Building a Website with Hugo/Academic
author: admin
date: '2020-05-11'
categories:
  - web
tags:
  - web
  - blogdown
  - Markdown
  - RStudio
  - Hugo
  - Academic
slug: building-a-website-with-hugo-academic
lastmod: '2020-05-11T15:15:24+01:00'
featured: no
image:
  caption: ''
  focal_point: ''
  preview_only: no
---
I decided to write this post as I felt that the [documentation from Academic](https://sourcethemes.com/academic/docs/deployment/), whilst excellent, was very much angled towards using [netlify](https://www.netlify.com/). Although netlify looks like a slick deployment system, I wanted to learn the process of building a classic [GitHub Pages](https://pages.github.com/) website from 'getting my hands dirty'!

Thus here I will document my approach to installing Hugo/Academic with an **RStudio-centric approach**. This should be suited to anyone who is familar with RStudio and wishes to use it as the text editor/IDE for their website. This particular installation was performed on macOS 10.14 Mojave, but I work cross-platform.

## Installation

1. GitHub
    * Fork [academic-kickstart](https://github.com/sourcethemes/academic-kickstart). 
      * This repository will house the code that *creates* your website + the 'raw' content (e.g. Markdown)
    * Create repo: username.github.io 
      * This will form the *GitHub Pages* repository that hosts your *compiled website* (i.e. HTML, CSS etc.) accessible at http://username.github.io  
2. Create a New Project in RStudio that will be the Content Project
    * New Project > Create Project: Version Control > Git
    * Repository URL = your fork of academic-kickstart: https://github.com/username/academic-kickstart
    * Subdirectory of: `/My Docs/Website/`  
3. Install Blogdown & Hugo dependencies  
			`install.packages("blogdown")`  
			`blogdown::install_hugo(version = "0.69.2", force = TRUE)`  
4. Workaround a Blogdown bug by moving `.config/_default/config.toml` to `config.toml` at your project root (replacing the default (blank) config.toml file)
    *	Open config.toml
	  * Amend baseurl to `baseurl = "https://<USERNAME>.github.io/"`  
5. Open Terminal in R (Computer: academic-kickstart user$)  
		  `git submodule update --init --recursiv`  
6. We will now add the username.github.io repo into a submodule in the folder named public  
		  `git submodule add -f -b master https://github.com/username/username.github.io.git public`  
    * This is similar to making a 'symbolic link'. Any content you publish into the public subfolder of your academic-kickstart fork will automatically appear in the root of your username.github.io (i.e. GitHub Pages) repo  
    * Note this has to be committed/pushed separately (see step 9)  
7. Publish initial commit  
		  `git add .`  
		  `git commit -m "Initial Commit"`  
		  `git push -u origin master`  
8. RStudio Console:  
		  `library(blogdown)`  
		  `hugo_build()`  
    * This will 'build' our website from the raw markdown files (currently the demo defaults) into HTML and place it in the public folder
9. Publish the public folder (i.e. the HTML our GitHub Pages will display)  
		`cd public `  
		`git add .`  
		`git commit -m "Build website"`  
		`git push origin master`  
		`cd ..`  
		
If all has gone to plan you should see the Academic kickstart demo appear at https://username.github.io !

## Configuring Academic

I couldn't put this any more simply than Academic have in their documentation. So first go to https://sourcethemes.com/academic/docs/get-started/ to set a theme, select widgets, specify core parameters and write a brief biography.  
  
Then move on to https://sourcethemes.com/academic/docs/page-builder/ which will guide you through the process of adding content to each widget (i.e. about, blog posts, etc.).

## Previewing changes with serve_site()

Once you've edited, and *saved*, the relevant `.toml` configuration files or `.md` widgets you will likely want to preview your changes before publishing them. Make sure you've loaded `library(blogdown)` then type `serve_site()` into the RStudio Console.

In the right-hand 'Viewer' window you will see a rendered preview of your website. The built-in RStudio browser is not the greatest, so you may also wish to test it in your default browser. Simply copy and paste the address from the Console output:  
`Serving the directory .Website/website-academic at http://127.0.0.1:4321` 
into your browser.

For any further changes once you press save the relevant file in RStudio you should find that Hugo will automatically re-render your site (you may need to refresh your browser)!

## Publishing changes to GitHub Pages

Once you're happy with your initial personalisation you will be ready to publish your site to GitHub Pages for the world to see!

Type `build_site()` into the Console in RStudio. Note how quick Hugo is, 884 ms to build 53 pages on my 9 year old computer!

You now need to commit your changes to GitHub. This takes two stages:  
  
  1. First update the 'academic-kickstart' repository that you forked during installation, this can be thought of as the 'backend' of your website.  
    In the RStudio **terminal** type:   
    `git add .`  
    `git commit -m "Initial Personalisation`  
    `git push origin master`  
2. Then commit the `/Public/` folder which contains the rendered HTML and has been made a Git submodule so the files you commit here will end up in the root of your `username.github.io` repo.
    `cd public`  
    `git add .`  
    `git commit -m "Initial Personalisation`  
    `git push origin master`
