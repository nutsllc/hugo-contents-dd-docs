---
title: "DD"
date: 2019-10-14T09:06:07Z
weight: 1
draft: false
---

``DD`` コマンドで Docker ホストに存在する全ての Docker コンテナの状態を一覧で確認することが出来ます。

それぞれのコンテナは、稼働（``Up``）, 停止（``Stopped``）, エラー（``Error``） などのコンテナの状況毎に区分けして表示されます。

以下の例では、ホスト上には 10 個のコンテナが存在しており全てのコンテナが正常稼動中です。


```bash
$ DD
--------------------------------
<Running: Up>
1 : 547f1f4fffc9      nutsllc/toybox-nginx:1.1 docker_hugo-memo-dev_1
2 : a93835fa896d      nutsllc/toybox-nginx:1.1 bin_starton.jp-wordpress_1
3 : 0622d9c615ad      nutsllc/toybox-php:7.0-f bin_starton.jp-php-fpm_1
4 : 3963109fdda3      nutsllc/toybox-mariadb:1 bin_starton.jp-wordpress-db_1
5 : b67977b1e21e      nutsllc/toybox-nginx:1.1 bin_dev.ontheroad.jp-wordpress_1
6 : e9c9e997f0af      nutsllc/toybox-php:7.0-f bin_php-fpm_1
7 : bd6f6c506eed      nutsllc/toybox-mariadb:1 bin_wordpress-db_1
8 : c0678a620996      jwilder/docker-gen       toybox-proxy-nginx-gen
9 : ae953f2b2d71      jrcs/letsencrypt-nginx-p toybox-proxy-letsencrypt
10: 56f96ed795fc      nutsllc/toybox-nginx:1.1 toybox-proxy-nginx
--------------------------------
<Stopped>
--------------------------------
<Stopped: Created>
--------------------------------
<Error:Dead>
--------------------------------
<Error: Restarting>
```