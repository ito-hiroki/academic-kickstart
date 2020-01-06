---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "新しい記事の追加の仕方"
subtitle: ""
summary: "サイトに新しい記事を追加するときの手順メモ"
authors: []
tags: ["memo", "Hugo"]
categories: ["memo"]
date: 2020-01-07T00:32:35+09:00
lastmod: 2020-01-07T00:32:35+09:00
featured: false
draft: false

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: ""
  focal_point: ""
  preview_only: false

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects: []
---

# 記事を新規作成する手順

基本的には`hugo new`を使って，記事を新規作成する．

1. `hugo new .\content\post\post_name.md`で新しい記事のmarkdownファイルが作成される．
1. `---`で囲まれたyamlフロントマターのtitle等を入力する．
1. 本文をmarkdownで書く
1. `hugo serve`でlocalhostで確認して，GitHubにpushしておしまい
