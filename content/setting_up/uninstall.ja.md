---
title: "アンインストール"
date: 2019-10-14T09:06:07Z
weight: 2
draft: false
---

## アンインストール

クローンしたデイレクトリを削除し、``.bash_profile`` または ``.bashrc`` に追記したコマンドを削除するだけでアンインストール完了です。

###  STEP 1.

クローンしたデイレクトリを削除する。

```bash
$ rm -rf docker-dd
```

### STEP 2.

``.bash_profile`` または ``.bashrc`` から以下を削除します。

```bash
source /path/to/docker-dd/docker-dd-common.fnc
source /path/to/docker-dd/docker-dd-network.fnc
source /path/to/docker-dd/docker-dd-volume.fnc
```

お疲れさまでした :-)