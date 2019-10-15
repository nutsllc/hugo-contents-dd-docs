---
title: "DDstats"
date: 2019-10-14T09:06:26Z
weight: 50
draft: false
---

## 概要

``DDstats`` コマンドは 稼働中の Docker コンテナの CPU やメモリ使用状況などの stats を出力します。

## 説明

``DDstats`` コマンドを実行すると peco が起動し稼働中のコンテナ一覧が表示されるので、その中から環境変数の一覧を取得したいコンテナを選択します。

stats はリアルタイムで表示され、``Ctl`` + ``c`` で ``DDstats`` が終了します。

## Example

``DDstats`` コマンドを実行します。

```bash
$ DDstats
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

選択したコンテナの stats がリアルタイムで表示されます。

```bash
CONTAINER ID  NAME                            CPU % MEM USAGE / LIMIT     MEM %  NET I/O         BLOCK I/O       PIDS
3963109fdda3  bin_starton.jp-wordpress-db_1   0.12% 111.5MiB / 1.795GiB   6.06%  103MB / 4.36GB  146MB / 1.61GB  28
CONTAINER ID  NAME                            CPU % MEM USAGE / LIMIT     MEM %  NET I/O         BLOCK I/O       PIDS
3963109fdda3  bin_starton.jp-wordpress-db_1   0.09% 111.5MiB / 1.795GiB   6.06%  103MB / 4.36GB  146MB / 1.61GB  28
```

