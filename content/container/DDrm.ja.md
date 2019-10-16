---
title: "DDrm"
date: 2019-10-14T09:06:55Z
weight: 5
draft: false
---

## 概要
``DDrm`` コマンドは停止中の Docker コンテナを破棄します。

## 説明
``DDrm`` コマンドを実行すると peco が起動し停止中のコンテナ一覧が表示されるので、その中から破棄したいコンテナを選択します。

## 使い方
``DDrm`` コマンドを実行します。

```bash
$ DDrm
```

peco が起動し、停止中のコンテナ一覧が表示されるので、その中から停止したいコンテナを選択します。

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

選択したコンテナが破棄されます。

```bash
 DDrm
docker rm
57357eb6a1c2
```
 
