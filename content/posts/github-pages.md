---
title: "Github Pages"
isCJKLanguage: true
date: 2019-06-18T21:54:03+08:00
summary: "GitHub Pages 是目前最便宜（免費）且便利的靜態網站部署點。"
draft: false
---

GitHub Pages 最初提供給開發者的靜態網站佈署方式，是替專案建立一個獨立分支 `gh-pages`，意即與專案目錄擺放完全不同的內容，例如專案目錄下若是一個 SSG（靜態網站生成器），那麼 `gh-pages` 分支就是擺放「轉製後的靜態網站檔案」。

但現在 GitHub Pages 提供了更方便的方式：整個網站當靜態網站的根目錄，或是指定 `docs/` 目錄為靜態網站根目錄。

後者對 SSG 來說完全就是天生匹配，雖然說這設計的原意、與 `gh-pages` 最初的初衷一致：替一個開發專案，建置對外呈現的解釋、說明、或宣傳內容。

在 Hugo 的 `config.toml` 中添加：

```
publishDir = "docs"
```

並記得不要擺進 `.gitignore` 檔案中（一般會將 `public/` 目錄加入）。