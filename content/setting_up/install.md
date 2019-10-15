—
title: “インストール”
date: 2019-10-14T09:06:07Z
weight: 1
draft: false
—

## システム要件

- docker
- peco


## Toybox DD インストール

レポジトリからクローンします。

```bash
$ git clone https://github.com/nutsllc/docker-dd
```

``.bash_profile`` から Toybox DD を読み込みます。

```bash
$ vim .bash_profile

source /path/to/docker-dd/docker-dd-common.fnc
source /path/to/docker-dd/docker-dd-network.fnc
source /path/to/docker-dd/docker-dd-volume.fnc 
```

``.bash_profile`` の設定を反映させます。

### 確認

```bash
$ DDversion
```