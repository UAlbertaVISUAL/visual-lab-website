---
title: Sample Blog Post Template
image: images/blog/sample-post/sample-image.png
tags:
  - sample
  - template
  - blog
excerpt: A sample post showing the filename format, front matter, excerpt, and image setup used for blog entries on this site.
---

<!-- excerpt start -->
Use this sample post as a starting point when adding new updates to the lab blog. Create a Markdown file in `_posts` named `YYYY-MM-DD-your-post-title.md`, update the front matter, and replace the sample text and image with your own content.
<!-- excerpt end -->

## Overview

This template demonstrates the minimum setup needed for a blog post to appear on the blog page:

- place the file in `/_posts`
- use the `YYYY-MM-DD-your-post-title.md` filename format
- set `title`, `image`, and any `tags` in the front matter
- replace the sample body content with the real post text
- save the file and Jekyll will include it automatically on the Blog page

{% include figure.html
  image=page.image
  caption="Sample blog image"
  width="100%"
%}

## Reusing this template

1. Copy this file.
2. Rename it using the publication date and post title slug.
3. Update the front matter and body content.
4. Delete the file from `_posts` when you want to remove the post from the site.
