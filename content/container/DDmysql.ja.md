---
title: "DDmysql"
date: 2019-10-14T09:06:26Z
weight: 32
draft: false
---

## 概要
``DDmysql`` コマンドは MySQL が稼働しているコンテナに接続し ``mysql`` コマンドを実行します。

## 説明
MySQL への接続は、

ユーザー名: root
パスワード: root

です。

``DDmysql`` コマンドを実行すると peco が起動し稼働中のコンテナ一覧が表示されるので、その中から、接続したい MySQL が稼動しているコンテナを選択します。

``DDmysql`` コマンドはコンテナの中に入り、 ``mysql -u root -proot`` を実行することと同等です。

``DDmysql`` コマンドで MySQL に接続した後は ``use <データベース名>`` でデータベースに接続出来ます。

``exit`` コマンドでコンテナから抜けることが出来ます。

## 使い方
``DDmysql`` コマンドを実行します。

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

選択したコンテナの内部に入り ``mysql`` コマンドが実行されます。

```bash
$ DDmysql
Welcome to the MariaDB monitor.  Commands end with ; or \g.
Your MariaDB connection id is 2
Server version: 10.1.14-MariaDB-1~jessie mariadb.org binary distribution

Copyright (c) 2000, 2016, Oracle, MariaDB Corporation Ab and others.

Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.

MariaDB [(none)]>
```
