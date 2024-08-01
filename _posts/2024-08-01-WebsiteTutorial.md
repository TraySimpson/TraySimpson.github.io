---
title: How To Make Your Own Website for Free
date: 2024-08-01 16:53:00 +0600
categories: [Web Dev, Hosting]
tags: [jekyll, github, ruby, webdev, html, domain, website]     # TAG names should always be lowercase
---

### Prerequesites
Before we get started, this tutorial is aimed at people who:

- Want more control over their website than no-code options offer (ex. Squarespace, WordPress, Wix)
- Have experience with GitHub (or just git)
- Have a basic understanding of how static websites work (not required)

This tutorial will guide you on how to create your own website for 100% free using GitHub pages to host a static site. 

Let's get started!

### The Basics
#### Create a GitHub Account
> If you don't want to use a custom domain, be aware that your URL will contain you GitHub username
{: .prompt-warning }

To get started, you'll need to [create a GitHub account](https://github.com/join) if you don't have one already. 

#### Choose a Jekyll Theme
[Jekyll]() is a static website framework written in Ruby that GitHub pages will use for serving your website. With Jekyll, you have the option of making it completely from scratching (writing your own HTML, CSS, and JS) or starting with a [template](https://jekyllrb.com/docs/themes). 

I would highly recommend choosing a template first, as this allows you to focus on the content of your site. You can always make changes to the template if needed.

Personally, I went with [Chirpy](https://chirpy.cotes.page) because it supported a responsive layout for mobile devices, easy support for creating posts, and lots of quality of life features (like dark mode toggles, post searching, and a timeline).


#### Create Your Repository
Depending on which theme you choose, this next step may vary slightly. For me, I cloned a copy of Chirpy's starter template into my GitHub account. 

[The GitHub Pages docs](https://pages.github.com) will guide you through most of the setup, so I'll only cover a few issues/scenarios you may run into, as these steps are better explained by the documentation.

### Running Your Site Locally
If you only follow the steps above, you'll need to make edits in the GitHub file editor, apply them, and then wait for the pipeline to finish before you can preview your site each time. Instead, [this guide](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/testing-your-github-pages-site-locally-with-jekyll) describes how to run your site locally for quick development.

> Getting Ruby to install the correct version can be a pain, so I'd highly recommend [Ruby Version Manager](https://rvm.io). This allows easy installing and switching between Ruby versions, which can be especially helpful if you want to try different templates
{: .prompt-warning }

### Adding Site Content
#### Modifying Your Site
Before you get too far ahead of yourself, I'd recommend reading [the basics of Jekyll](https://jekyllrb.com/docs/step-by-step/01-setup) to have some understanding of what you can do. This will vary based on the theme you selected, but the basics are always the same.

Start by updating any template variables in `_config.yml`. This is usually things like contact info, the site name, or even Google Analytics config. As always, this will depend on your theme.

#### VS Code Markdown Preview
If you don't want to bother setting up your site to run locally, you can also write your post files in markdown and use VS Code's Markdown Preview extension. Do note this may not be exactly what is displayed (based on what your theme modifies) but it can be close enough in most cases.

#### Verify Your `index.html`
Regardless of your theme, you will always need an `index.html` file in your projects root. This serves as the entry point to your website, AKA the default landing page. Without this, you may get a strange file directory view when you try to visit your site.

#### Create Your First Post
By default, posts are created in the `_posts` directory in the root of your project, and are named in the format `YYYY-MM-DD-Title.md`. You may also use the `.html` extension, but `.md` will be a lot easier to work with.

Additional details are described in [the Jekyll documentation](https://jekyllrb.com/docs/step-by-step/01-setup)

#### How To Update Your Site
Once you have your site looking how you want, simply push your changes up to GitHub. After a few minutes, the GitHub Pages pipeline should run and deploy your site at `<your-username>.github.io`

That's it! Now you have a public website that you can share with other people
