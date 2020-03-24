---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "bot運用でのcron設定のメモ"
subtitle: ""
summary: ""
authors: []
tags: ["memo", "cron"]
categories: ["cron"]
date: 2020-03-24T14:49:56+09:00
lastmod: 2020-03-24T14:49:56+09:00
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

研究室関係のbotをcronで定期実行したときの、cronの書き方のメモ。
参考サイト: https://intellectual-curiosity.tokyo/2018/10/12/ubuntu%E3%81%A7%E3%81%AEcron%E3%81%AE%E4%BD%BF%E3%81%84%E6%96%B9/

1. フォーマットのコピー
```
sudo cp /etc/crontab /etc/cron.d/cron_test
```

1. 設定の書き込み
```
sudo vi /etc/cron.d/cron_test
```
記述例: 左から分・時・日・月・曜日・ユーザ・シェル・コマンド
* 分は0-59
* 時は0-23
* 日は1-31
* 月は1-12
* 曜日は0,7:日曜日、1-6:月-土曜日
```
# 10分ごとに実行する
*/10 * * * *   userA /bin/bash /home/userA/test/test.sh
# 毎日23:58に実行する
58 23  * * *   userA /bin/bash /home/userA/test/test.sh
```
