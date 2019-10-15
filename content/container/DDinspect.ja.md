---
title: "DDenv"
date: 2019-10-14T09:06:26Z
weight: 50
draft: false
---

## 概要
``DDinspect`` コマンドは 稼働中の Docker コンテナの多くの情報が含まれているインスペクトを出力します。

## 説明
``DDinspect`` コマンドを実行すると peco が起動し稼働中のコンテナ一覧が表示されるので、その中から環境変数の一覧を取得したいコンテナを選択します。

## Example
``DDinspect`` コマンドを実行します。

```bash
$ DDinspect
```

peco が起動し、稼働中のコンテナ一覧が表示されるので、その中からコンテナを選択します。

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

選択したコンテナのインスペクトが出力されます。

```bash
[
    {
        "Id": "3963109fdda37b9b2f95e1d61b526ae9f96bcefd12564b866493b88611d7627f",
        "Created": "2019-08-26T09:26:36.378347389Z",
        "Path": "/entrypoint-ex.sh",
        "Args": [],
        "State": {
            "Status": "running",
            "Running": true,
            "Paused": false,
            "Restarting": false,
            "OOMKilled": false,
            "Dead": false,
            "Pid": 9104,
            "ExitCode": 0,
            "Error": "",
            "StartedAt": "2019-08-26T09:26:36.931345701Z",
            "FinishedAt": "0001-01-01T00:00:00Z"
        },
        "Image": "sha256:d98e4c2a6bb033105587fbd28f48012ecd359294fbbc59fcbe281fa8b0650224",
        -- 以下省略 --
```

``q`` で ``DDinspect`` を終了します。

