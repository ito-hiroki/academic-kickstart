---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "ブログの編集環境を新しく作る場合"
subtitle: ""
summary: ""
authors: ["memo", "Hugo"]
tags: []
categories: ["memo"]
date: 2020-03-22T16:08:01+09:00
lastmod: 2020-03-22T16:08:01+09:00
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

回りくどいやり方をしようとしてハマったのでメモ。  
参考にするAcademicのインストールサイト: https://sourcethemes.com/academic/docs/install/#install-with-git  
マジでsourceからインストールとか、snapを使ってインストールするな。  


1. Gitはインストールされている前提。
1. Hugoのインストール。   
[Hugoのreleases](https://github.com/gohugoio/hugo/releases)から.debをインスコ用のファイルをDL。   
条件は、**Extended** かつ **v0.63.1** 以上の必要がある。　　
1. 自分のブログのリポジトリをpull。
1. **git submodule update --init --recursive** をpullしたリポジトリ内で実行。ここ重要。 

snapを使ってイントールしようとしたり、sourceからインストールしようとしたけど、   
権限の関係や、versionの関係でクソダルいので.deb使ってインストールが一番簡単(だと思う)。  
インストールしようとして以下のようなエラーが出たら、  
多分最後の `git submodule` のコマンドを実行してない。  
```
Error: Error building site: "/home/hiroking/my_blog/academic-kickstart/content/home/publications.md:69:1": failed to extract shortcode: template for shortcode "alert" not found
```

