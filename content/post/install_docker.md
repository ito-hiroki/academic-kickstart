---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "DockerをUbuntuにインストール"
subtitle: ""
summary: ""
authors: []
tags: ["memo", "docker"]
categories: ["docker"]
date: 2020-03-22T17:05:23+09:00
lastmod: 2020-03-22T17:05:23+09:00
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

研究室の色々なPCにdockerをインストールするときに、  
毎回調べるのは面倒なのでメモっておく。  

参考サイト
1. https://qiita.com/ksasaki/items/b20a785e1a0f610efa08
1. https://docs.docker.com/install/linux/docker-ce/ubuntu/#install-docker-engine---community
1. https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-on-ubuntu-18-04
1. https://github.com/NVIDIA/nvidia-docker/tree/master#quickstart

### リポジトリのセットアップ
参考サイト2に書いてあることと同じ。  
```
sudo apt-get update

sudo apt-get install \
    apt-transport-https \
    ca-certificates \
    curl \
    gnupg-agent \
    software-properties-common

curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -

sudo apt-key fingerprint 0EBFCD88

sudo add-apt-repository \
   "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
   $(lsb_release -cs) \
   stable"
```

### docker engineのインストール
参考サイト2に書いてあることと同じ。  
```
sudo apt-get update

sudo apt-get install docker-ce docker-ce-cli containerd.io  ##最新のversionでよければ

sudo docker run hello-world
```


### sudoなしでdockerコマンドが使えるように
dockerグループに自分を追加する。
```
sudo usermod -aG docker [ユーザ名]
```

この後は再ログインしないと反映されないっぽいので注意！  
sshで入ってるなら、一旦抜けて再接続すればok。   


### nvidia-container-toolkitのインストール
参考サイト4に書いてあることと同じ。  
sudoが行えるようにして以下を実行。   
```
# Add the package repositories
distribution=$(. /etc/os-release;echo $ID$VERSION_ID)
curl -s -L https://nvidia.github.io/nvidia-docker/gpgkey | sudo apt-key add -
curl -s -L https://nvidia.github.io/nvidia-docker/$distribution/nvidia-docker.list | sudo tee /etc/apt/sources.list.d/nvidia-docker.list

sudo apt-get update && sudo apt-get install -y nvidia-container-toolkit
sudo systemctl restart docker
```




