---
title: "インストール"
date: 2019-10-14T09:06:07Z
weight: 1
draft: false
---

## システム要件

- [Docker](https://www.docker.com/)
- [peco](https://github.com/peco/peco)

## インストール

[toybox-dd](https://github.com/nutsllc/docker-dd) は単なるシェル関数の集まりなので、リポジトリをクローンして、ファイルを読み込むだけでインストールは完了です。

###  STEP 1.

GitHub から [toybox-dd](https://github.com/nutsllc/docker-dd) を任意の場所へクローンします。

```bash
$ git clone https://github.com/nutsllc/docker-dd.git
```

### STEP 2.

``.bash_profile`` または ``.bashrc`` に以下を追記します。

```bash
source /path/to/docker-dd/docker-dd-common.fnc
source /path/to/docker-dd/docker-dd-network.fnc
source /path/to/docker-dd/docker-dd-volume.fnc
```

### STEP 3.

``.bash_profile`` または ``.bashrc`` を再読み込みします。

```bash
$ sourse ~/.bash_profile

または

$ source ~/.bashrc
```

### インストールの確認

```bash
$ DDh
```

お疲れさまでした :-)