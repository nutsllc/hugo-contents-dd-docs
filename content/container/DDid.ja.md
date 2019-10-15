---
title: "DDid"
date: 2019-10-14T09:06:26Z
weight: 51
draft: false
---

## 概要
``DDid`` コマンドは 稼働中の Docker コンテナのコンテナ ID を出力します。

## 説明
``DDid`` コマンドを実行すると peco が起動し稼働中のコンテナ一覧が表示されるので、その中からコンテナ ID を出力したいコンテナを選択します。

## Example
``DDid`` コマンドを実行します。

```bash
$ DDid
```

peco が起動し、稼働中のコンテナ一覧が表示されます。

```bash
QUERY>                                                                 IgnoreCase [10 (1/1)]
0333057af059        nutsllc/toybox-nginx:1.15.7-alpine       "/entrypoint-ex.sh"      13 min
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

任意のコンテナを選択すると、選択したコンテナのコンテナ ID が出力されます。

```bash
$ DDid
0622d9c615ad
```
