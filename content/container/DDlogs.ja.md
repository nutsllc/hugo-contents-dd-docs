---
title: "DDlogs"
date: 2019-10-14T09:06:26Z
weight: 50
draft: false
---

## 概要
``DDlogs`` コマンドは 稼働中の Docker コンテナのログを出力します。

## 説明
``DDlogs`` コマンドを実行すると peco が起動し稼働中のコンテナ一覧が表示されるので、その中からログを取得したいコンテナを選択します。

## Example

``DDlogs`` コマンドを実行します。

```bash
$ DDlogs
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

選択したコンテナのログが出力されます。

```bash
$ DDlogs
172.17.0.10 -  15/Oct/2019:20:43:40 +0900 "GET /wp-login.php" 200
172.17.0.10 -  15/Oct/2019:20:43:41 +0900 "POST /wp-login.php" 200
172.17.0.10 -  15/Oct/2019:20:43:42 +0900 "POST /xmlrpc.php" 200
172.17.0.10 -  15/Oct/2019:20:55:50 +0900 "GET /index.php" 404
172.17.0.10 -  15/Oct/2019:21:14:19 +0900 "GET /index.php" 404
172.17.0.10 -  15/Oct/2019:21:28:29 +0900 "POST /xmlrpc.php" 200
172.17.0.10 -  15/Oct/2019:21:33:18 +0900 "GET /index.php" 404
172.17.0.10 -  15/Oct/2019:21:52:22 +0900 "POST /wp-cron.php" 200
```

## Tips

```DDlogs``` に ``-f`` オプションをつけて実行すると、リアルタイムでログが更新されます。

```bash
$ DDlogs -f
```


