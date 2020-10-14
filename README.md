# blog

## 如何發表文章
see https://themes.gohugo.io/hugo-theme-jane/
```bash
cd $HOME

git clone https://github.com/iii-cutting-edge-tech-lab/old-buddies-website.git

cd old-buddies-website
## add example.md to content/post/ like 
vim content/post/example.md [link](./content/post/example.md)
==================================================================
---
title: "Hello Wolrd Page"
date: 2020-10-13T00:00:00+08:00
lastmod: 2020-10-13T00:00:00+08:00
draft: false
tags: ["hellowolrd", "example"]
categories: ["docs", "shortcodes", "index"]

menu:
  main:
    parent: "docs"
    weight: 3
---

# Hello Wolrd
==================================================================
---
```

### 地端測試網頁 
```bash
hugo server -D
```

### 發布文章
```bash
cd $HOME/old-buddies-website
hugo -D

# output will in public dir.

# new file need to track
git add . && git ci -a -m "🚀 Build and deploy"
```