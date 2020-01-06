---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Hugoのインストール"
subtitle: ""
summary: "Hugoをwindows10にインストールした時のメモ"
authors: ["admin"]
tags: ["memo", "Hugo"]
categories: ["memo"]
date: 2020-01-07T00:23:28+09:00
lastmod: 2020-01-07T00:23:28+09:00
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

基本的には[ココ](https://gohugo.io/getting-started/installing/#windows)を参考に進めば良い．

1. `Hugo/bin`と`Hugo/Sites`フォルダを作成
1. [Hugo Releases](https://github.com/gohugoio/hugo/releases)からextend ver.のzipをインストールして，binの中に展開．
1. `hugo.exe`へのPathを環境変数に追加．
1. 一応，`hugo help`でPathが正常に通っているか確認．