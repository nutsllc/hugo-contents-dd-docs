---
title: "DDidi"
date: 2019-10-14T09:06:26Z
weight: 51
draft: false
---

## 概要
``DDidi`` コマンドは Docker ホスト上に存在するコンテナイメージのイメージ ID を出力します。

## 説明
``DDidi`` コマンドを実行すると peco が起動しコンテナイメージ一覧が表示されるので、その中からイメージ ID を出力したいコンテナを選択します。

## 使い方
``DDidi`` コマンドを実行します。

```bash
$ DDidi
```

peco が起動し、コンテナイメージ一覧が表示されます。

```bash
UERY>                                                                                                                                                              IgnoreCase [18 (1/1)]
hugo                                     latest              155a39a63fa9        3 days ago          57.5MB                                                                              nginx                                    latest              f949e7d76d63        2 weeks ago         126MB
nutsllc/toybox-hugo                      latest              a8620a836027        4 weeks ago         57.5MB
test/fpm-alpine                          7                   d8d7bffb94b7        6 weeks ago         47.7MB
<none>                                   <none>              6485ad97e0d1        6 weeks ago         400MB
jekyll/jekyll                            3.8                 ce4b587f0134        7 weeks ago         457MB
alpine                                   3.10                961769676411        7 weeks ago         5.58MB
nutsllc/toybox-php                       7.0-fpm             da5ef3d61de0        8 weeks ago         526MB
lw                                       latest              4b5af5b4d226        2 months ago        49.2MB
<none>                                   <none>              d72ac4f4b1f8        2 months ago        49.2MB
nutsllc/toybox-nginx                     1.15.7-alpine       b265b479f4e3        2 months ago        18.3MB
jrcs/letsencrypt-nginx-proxy-companion   latest              cf1282c6f745        3 months ago        94.1MB
alpine                                   3.4                 b7c5ffe56db7        8 months ago        4.82MB
nginx                                    1.15.7-alpine       6884a281e9a4        9 months ago        17.8MB
nutsllc/toybox-mariadb                   10.1.14             d98e4c2a6bb0        10 months ago       388MB
jwilder/docker-gen                       latest              8159de90f0e8        11 months ago       20.2MB
nutsllc/toybox-mailcatcher               latest              805e5f026a19        2 years ago         162MB
php                                      5.6.23-apache       f520057d2e04        3 years ago         400MB
```

任意のコンテナイメージを選択すると、選択したコンテナイメージのイメージ ID が出力されます。

```bash
 DDidi
ce4b587f0134
```

