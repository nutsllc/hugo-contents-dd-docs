---
title: "DDbash"
date: 2019-10-14T09:06:26Z
weight: 31
draft: false
---

## 概要
``DDbash`` コマンドは 稼働中の Docker コンテナの中に入ります。

## 説明
コンテナ内ではシェル(``bash``)を用います。

``DDbash`` コマンドを実行すると peco が起動し稼働中のコンテナ一覧が表示されるので、その中から、中に入りたいコンテナを選択します。

``DDbash`` コマンドは ``docker exec -it <コンテナID> /bin/bash`` と同等です。

``exit`` コマンドでコンテナから抜けることが出来ます。

## Example
``DDbash`` コマンドを実行します。

```bash
$ DDbash
```

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
$ DDbash
root@0622d9c615ad:/#

# コンテナの中でコマンドを実行します
root@0622d9c615ad:/# cd /var/www
root@0622d9c615ad:/var/www# ls -la
total 0
drwxr-xr-x. 1 root root 18 Jul 14  2016 .
drwxr-xr-x. 1 root root 17 Jul 14  2016 ..
drwxr-xr-x. 1 root root  6 Aug 18 13:32 html
root@0622d9c615ad:/var/www#
```

``exit`` コマンドでコンテナから抜けます。

```bash
root@0622d9c615ad:/var/www# exit
exit
$
```

## Hints & Tips

Alpine Linux をベースにしたコンテナには bash がインストールされていないため ``DDbash`` でコンテナの中に入ることは出来ません。

``DDbash`` コマンドの代わりに ``DDsh`` でコンテナの中に入れます。



