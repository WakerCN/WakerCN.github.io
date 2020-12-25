---
title: hexo-next主题配置
tags:
  - hexo
  - next
abbrlink: 20357
date: 2020-12-25 15:57:54
---

## 插件

### hexo-generator-searchdb

#### 简介

​		为 Hexo 博客添加本地搜索功能，该插件用于生成搜索索引文件，其中包含文章的所有必要数据，可用于为博客编写本地搜索引擎。

#### 安装

```bash
npm install hexo-generator-searchdb
```

####  Hexo 配置`_config.yml`

```yaml
# 本地搜索
# https://github.com/theme-next/hexo-generator-searchdb
search:
  path: search.xml
  field: post
  content: true
  format: html
```

#### Next 配置`_config.yml`

```yaml
# Local Search
# Dependencies: https://github.com/next-theme/hexo-generator-searchdb
local_search:
  enable: true
  # If auto, trigger search by changing input.
  # If manual, trigger search by pressing enter key or search button.
  trigger: auto
  # Show top n results per article, show all results by setting to -1
  top_n_per_article: 1
  # Unescape html strings to the readable one.
  unescape: false
  # Preload the search data when the page loads.
  preload: true
```

## 样式

单行代码颜色

找到 `themes\next\source\css\_variables\base.styl`修改以下代码

```stylus
// 文章``代码块的自定义样式
$code-foreground                = #dd0055  // 用``围出的单行代码字体颜色
$code-background                = #eee  // 用``围出的单行代码背景颜色
```

