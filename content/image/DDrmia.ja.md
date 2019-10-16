---
title: "DDrmia"
date: 2019-10-14T09:06:07Z
weight: 12
draft: false
---

## 概要
``DDrmia`` コマンドは Docker ホストに存在する全ての Docker コンテナイメージを削除します。

## 説明
コンテナ化されているイメージは削除されません。イメージを削除する場合は、先にコンテナを停止/破棄してください。

コンテナの停止/破棄は [DDdown](../dddown) コマンドで実行出来ます。

## 使い方

``DDrmia`` コマンドを実行します。

```bash
$ DDrmia
```

Docker ホスト上に存在する全てのイメージがイメージが削除されます。

```bash
$ DDrmia
f949e7d76d63
4862iny5hjck2
52qsjnx415hl1
```
