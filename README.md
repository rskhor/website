# Website

## Live Version

The live version is available at [rushan.pelagicworld.com](https://rushan.pelagicworld.com).

## Hosting Guide

The static files for the live version are all stored on [Amazon S3](https://aws.amazon.com/s3).
I'm caching these files close to end-users by using [Cloudflare](https://www.cloudflare.com) as a CDN.

This speeds up load times dramatically since the Amazon S3 bucket is in the AWS Region **Asia Pacific (Tokyo)**
but most readers of this website are based far away in either Singapore or New York City.

### Create an allowlist so your CDN can read from your origin server

Access to your object store should be limited to your CDN, and for read operations only.

AWS has a guide for this in their
[S3 documentation](https://docs.aws.amazon.com/AmazonS3/latest/userguide/example-bucket-policies.html#example-bucket-policies-IP).
This will involve adding the full list of [Cloudflare IP addresses](https://www.cloudflare.com/ips) to the S3 Bucket Policy section.

### Configure your CDN eviction policy using HTTP headers

Make sure your origin server sends an informative `Cache-Control` header over to your CDN in HTTP responses.

```
Cache-Control: public, max-age=31536000, immutable
```

If you plan to evict the CDN cache manually, you can get away with setting a long `max-age`.

### Configure client browser HTML rendering using HTTP headers

Make sure that your origin server returns the correct `Content-Type` headers, especially for HTML files.
If the header is absent, client browsers might not render the HTML file,
and instead treat it as a file download if it lacks a `.html` file extension.

```
Content-Type: text/html
```

## Setup Guide

Clone the repository and navigate into the project directory.
Next, [install Jekyll](https://jekyllrb.com/docs/installation/macos).

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

1. Open `_data/links.yml`.
1. Add a new `title` line.
1. Add a new `url` line.

### Add a new Project post

1. Create a `_projects` folder if it does not already exist.
1. Create a folder within it with the same name as the year of your new post.
    - For instance, `2021`.
1. Add a new Markdown file for your Project post.
    - Markdown files have `.md` as their file extension.
    - This file should be named with `kebab-case`.
    - The filename will also be the URL endpoint of the post, sans the `.md` file extension.
1. Use the following template and add your content in Markdown below the header block.

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

1. Create a `_blog` folder if it does not already exist.
1. Create a folder within it with the same name as the year of your new post.
    - For instance, `2021`.
1. Add a new Markdown file for your Blog post.
    - Markdown files have `.md` as their file extension.
    - This file should be named with `kebab-case`.
    - The filename will also be the URL endpoint of the post, sans the `.md` file extension.
1. Use the following template and add your content in Markdown below the header block.

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
