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

## Example

```bash
$ DDmysql
```
