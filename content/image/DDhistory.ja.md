---
title: "DDhistory"
date: 2019-10-14T09:06:26Z
weight: 50
draft: false
---

## 概要
``DDhistory`` コマンドは Docker コンテナイメージの履歴を出力します。

## 説明
``DDhistory`` コマンドを実行すると peco が起動しコンテナイメージの一覧が表示されるので、その中から履歴を確認したいイメージを選択します。

## Example
``DDenv`` コマンドを実行します。

```bash
$ DDhistory
```

peco が起動し、イメージ一覧が表示されるので、その中からイメージを選択します。

```bash
QUERY>                                                                 IgnoreCase [16 (1/1)]
hugo                                     latest              155a39a63fa9        3 days ago
nginx                                    latest              f949e7d76d63        2 weeks ago
nutsllc/toybox-hugo                      latest              a8620a836027        4 weeks ago
test/fpm-alpine                          7                   d8d7bffb94b7        6 weeks ago
alpine                                   3.10                961769676411        7 weeks ago
nutsllc/toybox-php                       7.0-fpm             da5ef3d61de0        8 weeks ago
nutsllc/toybox-nginx                     1.15.7-alpine       b265b479f4e3        2 months ag
alpine                                   3.4                 b7c5ffe56db7        8 months ag
nginx                                    1.15.7-alpine       6884a281e9a4        9 months ag
nutsllc/toybox-mariadb                   10.1.14             d98e4c2a6bb0        10 months a
```

選択したイメージの履歴が表示されます。

```bash
$ DDhistory
IMAGE               CREATED             CREATED BY                                      SIZE                COMMENT
f949e7d76d63        2 weeks ago         /bin/sh -c #(nop)  CMD ["nginx" "-g" "daemon…   0B
<missing>           2 weeks ago         /bin/sh -c #(nop)  STOPSIGNAL SIGTERM           0B
<missing>           2 weeks ago         /bin/sh -c #(nop)  EXPOSE 80                    0B
<missing>           2 weeks ago         /bin/sh -c ln -sf /dev/stdout /var/log/nginx…   22B
<missing>           2 weeks ago         /bin/sh -c set -x     && addgroup --system -…   56.8MB
<missing>           2 weeks ago         /bin/sh -c #(nop)  ENV PKG_RELEASE=1~buster     0B
<missing>           2 weeks ago         /bin/sh -c #(nop)  ENV NJS_VERSION=0.3.5        0B
<missing>           2 weeks ago         /bin/sh -c #(nop)  ENV NGINX_VERSION=1.17.4     0B
<missing>           4 weeks ago         /bin/sh -c #(nop)  LABEL maintainer=NGINX Do…   0B
<missing>           4 weeks ago         /bin/sh -c #(nop)  CMD ["bash"]                 0B
<missing>           4 weeks ago         /bin/sh -c #(nop) ADD file:1901172d265456090…   69.2MB
```

