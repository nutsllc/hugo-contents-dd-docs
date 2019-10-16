---
title: "DDrmi"
date: 2019-10-14T09:06:07Z
weight: 11
draft: false
---

## 概要
``DDrmi`` コマンドは Docker ホストに存在するDocker コンテナイメージを削除します。

## 説明
``DDrmi`` コマンドを実行すると peco が起動し Docker イメージの一覧が表示されるので、その中から削除したいイメージを選択します。

コンテナ化されているイメージは削除されません。イメージを削除する場合は、先にコンテナを停止/破棄してください。

コンテナの停止/破棄は [DDdown](../dddown) コマンドで実行出来ます。

## 使い方
``DDrmi`` コマンドを実行します。

```bash
$ DDrmi
```

peco が起動し、イメージ一覧が表示されるので、その中からイメージを選択します。

```bash
QUERY>                                                                 IgnoreCase [16 (1/1)]
hugo                                     latest              155a39a63fa9        3 days ago
nginx                                    latest              f949e7d76d63        2 weeks ago
nutsllc/toybox-hugo                      latest              a8620a836027        4 weeks ago
test/fpm-alpine                          7                   d8d7bffb94b7        6 weeks ago
alpine                                   3.10                961769676411        7 weeks ago
nutsllc/toybox-php                       7.0-fpm             da5ef3d61de0        8 weeks ago
nutsllc/toybox-nginx                     1.15.7-alpine       b265b479f4e3        2 months ag
alpine                                   3.4                 b7c5ffe56db7        8 months ag
nginx                                    1.15.7-alpine       6884a281e9a4        9 months ag
nutsllc/toybox-mariadb                   10.1.14             d98e4c2a6bb0        10 months a
```

選択したイメージが削除されます。

```bash
$ DDrmi
f949e7d76d63
```


