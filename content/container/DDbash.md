---
title: "DDbash"
date: 2019-10-14T09:06:26Z
weight: 31
draft: false
---

## 目的

``DDbash`` コマンドは 稼働中の Docker コンテナの中に入ります。

## 概要

コンテナ内ではシェル(``bash``)を用います。

``DDbash`` コマンドを実行すると peco が起動し稼働中のコンテナ一覧が表示されるので、その中から、中に入りたいコンテナを選択します。

``DDbash`` コマンドは ``docker exec -it <コンテナID> /bin/bash`` と同等です。

``exit`` コマンドでコンテナから抜けることが出来ます。

## Demo

```bash
$ DDbash
``` 

## Hints & Tips

Alpine Linux をベースにしたコンテナには bash がインストールされていないため ``DDbash`` でコンテナの中に入ることは出来ません。

``DDbash`` コマンドの代わりに ``DDsh`` でコンテナの中に入れます。



