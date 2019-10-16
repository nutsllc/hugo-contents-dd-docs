---
title: "DDenv"
date: 2019-10-14T09:06:26Z
weight: 50
draft: false
---

## 概要
``DDenv`` コマンドは 稼働中の Docker コンテナに設定されている環境変数の一覧を出力します。

## 説明
``DDenv`` コマンドを実行すると peco が起動し稼働中のコンテナ一覧が表示されるので、その中から環境変数の一覧を取得したいコンテナを選択します。

## 使い方
``DDenv`` コマンドを実行します。

```bash
$ DDenv
```

peco が起動し、コンテナ一覧が表示されるので、その中からコンテナを選択します。

```bash
QUERY>                                                                 IgnoreCase [10 (1/1)]
0333057af059        nutsllc/toybox-nginx:1.15.7-alpine       "/entrypoint-ex.sh"      36 min
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

選択したコンテナの環境変数一覧が表示されます。

```bash
$ DDenv
PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
HOSTNAME=396310woi3d9fdda3
TERM=xterm
TOYBOX_UID=1234
TOYBOX_GID=1234
MYSQL_ROOT_PASSWORD=xxxx
MYSQL_DATABASE=starton_jp
MYSQL_USER=hanako
MYSQL_PASSWORD=miho
GOSU_VERSION=1.7
MARIADB_MAJOR=10.1
MARIADB_VERSION=10.1.14+maria-1~jessie
HOME=/root
```
