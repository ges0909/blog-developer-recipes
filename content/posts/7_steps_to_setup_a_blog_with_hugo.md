---
title: 7 Steps to Setup a Blog with Hugo
date: 2021-03-28T08:00:00+01:00
draft: true
---

The instructions are written for [Windows](https://www.microsoft.com/de-de/windows/) and [Chocolatey](https://chocolatey.org/).

## Step 1: Install Git

As _admin_ user:

```bash
choco install git -y
git version # check installation
```

## Step 2: Install Hugo

As _admin_ user:

```bash
choco install hugo-extended -y
hugo version # check installation
```

## Step 3: Create a new Blog site

```bash
hugo new site hugo_blog && cd hugo_blog
```

## Step 4: Init a Git repo

```bash
git init
git remote add origin git@github.com:ges0909/hugo_blog.git
```

## Step 5: Add a Hugo theme

```bash
git submodule add git@github.com:dillonzq/LoveIt.git themes/LoveIt
echo theme = "LoveIt" >> config.toml
```

Edit `config.toml` as required by theme author.

## Step 6: Create a first Blog post

```bash
hugo new posts/7_steps_to_setup_a_blog_with_hugo.md
```

## Step 7: Run the Blog

```bash
hugo serve -D # development mode
# or
hugo server -D --disableFastRender
```

In an other console:

```bash
start http://localhost:1313/
```
