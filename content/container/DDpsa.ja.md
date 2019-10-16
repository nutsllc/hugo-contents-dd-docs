---
title: "DDpsa"
date: 2019-10-14T09:06:07Z
weight: 1
draft: false
---

## 概要
``DDpsa`` は Docker ホスト上に存在する全てのコンテナを出力します。

## 説明
``DDpsa`` コマンドは ``docker ps -a`` のエイリアスです。そのため、``DDpsa`` の出力結果は、``docker ps -a`` と同じです。

特別の場合を除いて、通常は [DD](dd/) コマンドの方が使い易いと思います。

## 使い方

``DDpsa`` コマンドを実行します。

Docker ホスト上に存在する全てのコンテナが一覧で表示されます。

```bash
$ DDpsa
<docker ps -a>
0333057af059        nutsllc/toybox-nginx:1.15.7-alpine       "/entrypoint-ex.sh"      54 seconds ago      Up 53 seconds       0.0.0.0:32927->80/tcp                      docker_hugo-memo-dev_1
a93835fa896d        nutsllc/toybox-nginx:1.15.7-alpine       "/entrypoint-ex.sh"      7 weeks ago         Up 7 weeks          0.0.0.0:32844->80/tcp                      bin_starton.jp-wordpress_1
0622d9c615ad        nutsllc/toybox-php:7.0-fpm               "/entrypoint-ex.sh p…"   7 weeks ago         Up 7 weeks          9000/tcp                                   bin_starton.jp-php-fpm_1
3963109fdda3        nutsllc/toybox-mariadb:10.1.14           "/entrypoint-ex.sh"      7 weeks ago         Up 7 weeks          3306/tcp                                   bin_starton.jp-wordpress-db_1
b67977b1e21e        nutsllc/toybox-nginx:1.15.7-alpine       "/entrypoint-ex.sh"      7 weeks ago         Up 7 weeks          0.0.0.0:32843->80/tcp                      bin_dev.ontheroad.jp-wordpress_1
e9c9e997f0af        nutsllc/toybox-php:7.0-fpm               "/entrypoint-ex.sh p…"   7 weeks ago         Up 7 weeks          9000/tcp                                   bin_php-fpm_1
bd6f6c506eed        nutsllc/toybox-mariadb:10.1.14           "/entrypoint-ex.sh"      7 weeks ago         Up 7 weeks          3306/tcp                                   bin_wordpress-db_1
c0678a620996        jwilder/docker-gen                       "/usr/local/bin/dock…"   7 weeks ago         Up 7 weeks                                                     toybox-proxy-nginx-gen
ae953f2b2d71        jrcs/letsencrypt-nginx-proxy-companion   "/bin/bash /app/entr…"   7 weeks ago         Up 7 weeks                                                     toybox-proxy-letsencrypt
56f96ed795fc        nutsllc/toybox-nginx:1.15.7-alpine       "/entrypoint-ex.sh"      7 weeks ago         Up 7 weeks          0.0.0.0:80->80/tcp, 0.0.0.0:443->443/tcp   toybox-proxy-nginx
```


この例では、ホスト上には 10 個のコンテナが存在していることがわかります。