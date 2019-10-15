---
title: "DDbash"
date: 2019-10-14T09:06:26Z
weight: 31
draft: false
---

``DDbash`` コマンドは 稼働中の Docker コンテナの中に入ります。

コンテナ内ではシェル(``bash``)を用います。

``DDbash`` コマンドを実行すると peco が起動し稼働中のコンテナ一覧が表示されるので、その中から、中に入りたいコンテナを選択します。

``DDbash`` コマンドは ``docker exec -it <コンテナID> /bin/bash`` と同等です。

``exit`` コマンドでコンテナから抜けることが出来ます。

```bash
$ DDbash
``` 

