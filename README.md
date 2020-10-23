## 如何發表文章
see https://themes.gohugo.io/hugo-theme-jane/
```bash
git clone https://github.com/iii-cutting-edge-tech-lab/old-buddies-website.git

cd old-buddies-website
## add example.md to content/post/ like 
vim content/post/example.md
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
cd old-buddies-website

# new file need to track
git add . && git ci -a -m "what-you-do?!"

git push
```

### 修改/增加 Social 
以 `section3.md` 做範例 ，先增加 instagram 欄位。
```md
---
title: "Contact"
weight: 4
---

## Contact Old budddies Day
### Special thanks to
![](/img/lbh.png)![](/img/lg.png)
{{< socialhandles >}}
    {{< facebook >}}
    {{< github >}}
    {{< instagram > }}
{{< /socialhandles >}}
```

再修改 `config.toml` ，新增 instagram 欄位。
```toml
.
.
.
[Social]
    facebook = "groups/349727092633390"
    github ="iii-cutting-edge-tech-lab"
    instagram ="instagram"
```