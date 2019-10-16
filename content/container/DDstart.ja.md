---
title: "DDstart"
date: 2019-10-14T09:06:17Z
weight: 2
draft: false
---

## 概要
``DDstart`` コマンドは 停止中の Docker コンテナを起動します。

## 説明
``DDstart`` コマンドを実行すると peco が起動し停止中のコンテナ一覧が表示されるので、その中から起動したいコンテナを選択します。

## 使い方
``DDstart`` コマンドを実行します。

```bash
$ DDstart
```

peco が起動し、停止中のコンテナ一覧が表示されるので、その中から起動したいコンテナを選択します。

```bash
QUERY>                                                                  IgnoreCase [1 (1/1)]
57357eb6a1c2        docker-compose_sample-php-5.6    "/entrypoint-php.sh …"   10 minutes ago
```

選択したコンテナが起動します。

```bash
$ DDstart
docker start
57357eb6a1c2
```
