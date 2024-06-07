---
title: How this blog was created
date: 2024-05-26T17:54:56.586Z
tags: ['Technology', 'Meta']
authors: ['Outman']
---

![targets](banner.jpg)
*An image of Parisian railtracks to make this post more aesthetic, because why not.*

## Introduction

This is intended to be a guide on how to host your own [HUGO](https://gohugo.io/) blog on Netlify for free.

First, you need to set up HUGO for local development. I'll be providing Windows-specific steps but you can find alternatives for macOS and Linux under the source for each step/command.

You can simply follow the steps provided here:
https://gohugo.io/installation/

But if you're on Windows 11 with WinGet and Chocolatey already installed, you can simply follow the steps below.

## Prerequisites

*Note: make sure to run PowerShell as administrator*

1. [Git](https://git-scm.com/):

	`winget install --id Git.Git -e --source winget`

2. [Go](https://go.dev/):

	Installer: [Download page](https://go.dev/doc/install)

    Go is also available on WinGet through the following command:

    `winget install -e --id GoLang.Go.1.20` (Latest version as of the writing of this article)
3. [Dart Sass](https://gohugo.io/hugo-pipes/transpile-sass-to-css/#dart-sass)

    `choco install sass`

## Exploring HUGO

### Themes

I built my HUGO theme on [Hugo Starter with Netlify CMS](https://github.com/ericmurphyxyz/hugo-starter-netlify-cms) and adapted the tagging system and RSS Feed integration from [LUGO](https://github.com/lukesmithxyz/lugo)

I made sure to update the CMS dashboard package from using an old version of Netlify CMS (https://unpkg.com/netlify-cms@^2.0.0/dist/netlify-cms.js) to the latest version of Decap CMS (https://unpkg.com/decap-cms@^3.1.2/dist/decap-cms.js)

I will provide a template on my GitHub soon and update this post with a link. I need to implement a tag page and search first.

### Development

1. Clone a HUGO theme:

    `git clone https://github.com/ericmurphyxyz/hugo-starter-netlify-cms.git`

    *(Will soon replace this with my theme)*

2. Open in your favorite text editor, like VSCode
3. Run the following command:

    `hugo server`

    This will deploy your website to localhost blazingly fast. You can navigate it by following the link with the exact port that should appear on the terminal.


HUGO is as simple as it gets, I'm still learning to script the different pages with Go and interested in exploring shortcodes in the future but for now all you need to know is some Markdown and writing your first post under the `/content` directory. I'll leave a sample blog post as a starting example.

### Deployment

First you need to create a free Netlify account and a GitHub account if you don't have one already. Then follow these steps:

1. Push your blog to a GitHub repository of your choosing.
2. Click the following link: https://app.netlify.com/start/deploy?repository=https://github.com/ericmurphyxyz/hugo-starter-netlify-cms&stack=cms *(Will soon replace this with my theme)*
3. Choose the branch you want to deploy


# Notes

 I will thouroughly expand on this post soon.