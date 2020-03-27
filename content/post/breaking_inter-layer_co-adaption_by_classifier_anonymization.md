---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Breaking Inter-Layer Co-Adaptation by Classifier Anonymization"
subtitle: ""
summary: ""
authors: []
tags: ["paper", "privacy-preserving"]
categories: ["paper"]
date: 2020-03-25T11:53:16+09:00
lastmod: 2020-03-25T11:53:16+09:00
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

# どんな論文？
ニューラルネットワークにおける特徴抽出器と分類器の共適応の問題．  
ナイーブに共同最適化をすると、特定の分類機に適応した複雑すぎる特徴分布がテスト性能を低下させることがある．  
特別な条件のもとでは，FOCA (Feature-extractor Optimization through Classifier Anonymization) 特徴が，同一クラス内でクラス分離可能な点状分布を形成することを数学的に示した．   
FOCAは最適化の際にランダムに生成された多数の弱い分類機を用いることで，露骨な共適応を避けるようにする．

# 先行研究と比べてすごいところ
FOCAはネットワークランダム化の研究に近いけれど，特徴抽出器と分類器の共同最適化を採用しない点で他とは異なる．
経験的に最適な特徴層を探索するのではなく，根本的に共適応を回避する方法を模索する．

# 技術や手法のキモはどこ


# どうやって有効だと検証した？


# 議論はある？


# 次に読むべき論文は？


