# Personal Website

## Setup Guide

Clone the repository and navigate into the project directory.
Next, [install Jekyll](https://jekyllrb.com/docs/installation/macos/).

```
brew install ruby
```

```
gem install --user-install bundler jekyll
```

```
gem install --user-install webrick
```

## Development Guide

### Run the development server

Jekyll comes with a local development server that supports auto reloading.

```
jekyll serve
```

View the website at [`localhost:4000`](http://localhost:4000/) in your browser.

### Add a new Link entry

1. Open `_date/links.yml`.
1. Add a new `title` line.
1. Add a new `url` line.

### Add a new Project post

1. Go to, or create, the `_projects` folder.
1. Find a folder within that named after the year of your post.
    - If it doesn't yet exist, create it.
1. Add a new Markdown file for your Project post
    - Markdown files have `.md` as their file extension.
    - This file should be named with `kebab-case`.
    - The filename will also be the URL endpoint of the post, sans the `.md`.
1. Use the following template and add your content in Markdown below the header
block.

```markdown
---
layout: skeleton
title: Digital spaces
subtitle: 09 August 2020
thumbnail: "/assets/images/rectangular-tiles.png"
---

# Contents of your post

Write the contents of your post in Markdown.

![This is an image](/assets/images/filename.png "Your image caption")
```

### Add a new Blog post

1. Go to, or create, the `_blog` folder.
1. Find a folder within that named after the year of your post.
    - If it doesn't yet exist, create it.
1. Add a new Markdown file for your Blog post
    - Markdown files have `.md` as their file extension.
    - This file should be named with `kebab-case`.
    - The filename will also be the URL endpoint of the post, sans the `.md`.
1. Use the following template and add your content in Markdown below the header
block.

```markdown
---
layout: skeleton
title: Digital spaces
subtitle: 09 August 2020
---

# Contents of your post

Write the contents of your post in Markdown.

![This is an image](/assets/images/filename.png "Your image caption")
```

## Live Version

The live version is available at [rushan.pelagicapps.com](https://rushan.pelagicapps.com).
