# TurtleCoin Blog

> Official TurtleCoin blog powered by Jekyll. All Articles reside on the \_post folder.

## Adding a new Article

Make sure that the filename adheres to the following naming schema `{YYYY}-{MM}{DD}-{slug}`. All blog posts are written in markdown and should start with a Jekyll header. Here is an example snippet:

```
---
layout: "post"
title: "One Trillion Turtles: Coin Supply and Unit Economics"
description: "Out of everything we get asked the most, and probably the biggest criticism, we, as a project, receive, is.."
image: "{{ site.baseurl }}/images/0XVJ-ujosmHGFdv1F"
published: "2018-01-09T16:20:24.977Z"
---

<--- MARKDOWNS STARTS HERE --->


```

Markdown should not start with a `# ` title. This is inserted by Jekyll using the title property in the header snippet.
