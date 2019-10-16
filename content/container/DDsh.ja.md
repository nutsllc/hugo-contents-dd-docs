---
title: "DDsh"
date: 2019-10-14T09:06:26Z
weight: 30
draft: false
---

## 概要

``DDsh`` コマンドは 稼働中の Docker コンテナの中に入ります。
コンテナ内ではシェル(``sh``)を用います。

## 説明

``DDsh`` コマンドを実行すると peco が起動し稼働中のコンテナ一覧が表示されるので、その中から、中に入りたいコンテナを選択します。

``DDsh`` コマンドは ``docker exec -it <コンテナID> /bin/sh`` と同等です。

``exit`` コマンドでコンテナから抜けることが出来ます。

## Example

``DDsh`` コマンドを実行します。

peco が起動して稼働中のコンテナ一覧が表示されるので、内部のシェルに接続したいコンテナーを選択します。

```bash
QUERY>                                                                 IgnoreCase [10 (1/1)]
0333057af059        nutsllc/toybox-nginx:1.15.7-alpine       "/entrypoint-ex.sh"      44 min
a93835fa896d        nutsllc/toybox-nginx:1.15.7-alpine       "/entrypoint-ex.sh"      7 week
0622d9c615ad        nutsllc/toybox-php:7.0-fpm               "/entrypoint-ex.sh p…"   7 week
3963109fdda3        nutsllc/toybox-mariadb:10.1.14           "/entrypoint-ex.sh"      7 week
b67977b1e21e        nutsllc/toybox-nginx:1.15.7-alpine       "/entrypoint-ex.sh"      7 week
e9c9e997f0af        nutsllc/toybox-php:7.0-fpm               "/entrypoint-ex.sh p…"   7 week
bd6f6c506eed        nutsllc/toybox-mariadb:10.1.14           "/entrypoint-ex.sh"      7 week
c0678a620996        jwilder/docker-gen                       "/usr/local/bin/dock…"   7 week
ae953f2b2d71        jrcs/letsencrypt-nginx-proxy-companion   "/bin/bash /app/entr…"   7 week
56f96ed795fc        nutsllc/toybox-nginx:1.15.7-alpine       "/entrypoint-ex.sh"      7 week
```

選択したコンテナ内部のシェルに接続します。

```bash
$ DDsh
/ #

# コンテナの中でコマンドを実行します
/ # cd /usr/share/nginx
/usr/share/nginx # ls -la
total 8
drwxr-xr-x    3 nginx    nginx           39 Aug 18 10:38 .
drwxr-xr-x    1 root     root            48 Dec 21  2018 ..
drwxr-xr-x    5 nginx    nginx         4096 Oct 15 16:41 html
-r--------    1 nginx    nginx         2882 Aug 18 10:38 wp-config.php
/usr/share/nginx #
```

``exit`` コマンドでコンテナから抜けます。

```bash
/usr/share/nginx # exit
$
```
