# Hugo Prototype

Static Site with Hugo.

部署在 GitHub Pages，勾選使用「主分支的 `docs` 目錄」，不需要設置 `gh-pages` 分支，但必須是開放倉儲（或升級成付費帳號）。

才知道原來 GitHub Pages 目前已經有三種模式：

- 原有的 `gh-pages branch` 分支模式。
- 整個主分支當成靜態網站根目錄。
- 將主分支的 `/docs` 當成網站根目錄。此模式特別適用於靜態網站生成器（SSG - Static Site Generator），Hugo 預設使用 `/public` 目錄，但可以在 `config.toml` 中修改 `publishDir = "docs"` 即可。

因此當模板開發時應使用「開發分支」，開發完成合併至 master branch 時等於自動發布正式版。