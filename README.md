# Hugo theme : Mainso

Mainso is a simple blog theme. Aim is to provide a simple way to publish blog articles or guides. 

## Features

Mainso is very light, there is some interesting features and maybe more are coming ! 

* Responsive
* Reading time estimation on articles
* Tags (and allow to filter by tag) 

Next features :
* Accessibility RGAA compliant
* Multi language support

## Getting started with Mainso

In this section we will see how to load Mainso theme and the basics configuration. 

### Use Mainso theme

From the Hugo's root project, add Mainso theme using git submodule

```bash
    git submodule add https://github.com/quentinchampenois/mainso.git themes/mainso
``` 

Once the theme is cloned, you can define `Mainso` as theme for your project

In your file `config.toml`, update the name of the theme as following :

```
theme = 'mainso'
```

At this moment, your project should have the mainso theme.

### Create your first content

When I create a new article, I simply use the hugo command for generating content.

Imagine we want to create our getting-started article.

1. Create new content using Hugo at the root project
```
hugo new blog/getting-started.md
```

This command should generate a new file under `content/blog/getting-started.md`

2. Configure the content header

By default, files is generated with 3 keys :
* title : Title is used as title in the articles list, and as tab title.
* Date
* Draft : By default draft is true, it means you won't be able to see it in the blog articles. However, you can configure hugo to serve draft content too

New keys to add : 

You can add keys `metadescription` and `tags` directly in the `content/blog/getting-started.md` as following :

```text

---
title: "Getting Started"
date: 2021-07-09T12:21:41+02:00
draft: false
metadescription: "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam"
tags: ["getting-started", "mainso", "hugo", "blog"]
---
```

Thanks to `metadescription`, your blog post has a metadescription in HTML structure. 
`tags` allows to filter article by tag, you can create new tag just by adding it in the tags array. If the search fails for a newly created tag, you can try to restart the hugo server.

### Theme configuration

Mainso is very light but a work was done to make it configurable.

In `config.toml` file, you can overrides some behaviour: 

```
copyright = "© 2015 Jane Doe.  <a href=\"https://creativecommons.org/licenses/by/4.0/\">Some rights reserved</a>."
enableEmoji = true

[params]
    # Define the date format for the blog posts
    dateFormat = "Jan 2, 2006"
    ###- Resume block -###
    # Title above the resume in homepage
    title = "Nunc odio odio, hendrerit ut rutrum et."
    # Resume present in the homepage
    resume = "Duis ex lorem, dapibus sed dolor a, fermentum venenatis arcu. Nunc odio odio, hendrerit ut rutrum et, luctus id justo. Interdum et malesuada fames ac ante ipsum primis in faucibus. Aenean cursus magna mi. Aliquam fringilla rhoncus massa ut iaculis. Donec non urna eros. Mauris in magna ut leo mattis maximus ac a ligula. Nullam blandit leo ac sodales malesuada. Nunc eleifend tortor ac elementum facilisis. Aliquam quis lectus sed elit consectetur molestie ac consectetur quam. Pellentesque posuere tortor in auctor consequat. Duis rutrum odio eget risus aliquet, vitae condimentum turpis gravida. Quisque tincidunt, ante eget volutpat pulvinar,"
    ######################
    # Homepage metadescription
    Meta = "Mainso metadescription"

    # Title on the sidebar
    sideTitle = "Posts"

    # Colors layout configuration
    links_color = "#5c00a2"
    background_color = "#fffef4"
    titles_color = "#000"
    paragraphs_color = "#000"
```

