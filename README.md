# Hugo Memo for Development

## Setup

1. clone this repository
2. fetch theme

	```bash
	$ git submodule update --init --recursive
	```

3. start server

	```bash
	$ cd docker
	$ dockerr-compose up -d
	```

4. access to ``http://localhost:1313`` on your browser.

5. enjyo :-)


## Create New document

### Create chapter

```bash
$ sh bin/chapter <chapter name>
```

### Create content

```bash
$ sh bin/post <chapter name>/<post name>.md
```

## Regenerate from WorkingCopy that is App for iOS.

create .git/hooks/post-recieve

### STEP1: clone this repository.

```bash
$ git clone https://github.com/nutsllc/hugo-contents-dd-docs
```

### STEP2: clone this repository as bare repository on the same directory as non-bare repository.

```bash
$ git clone --bare https://github.com/nutsllc/hugo-contents-dd-docs hugo-contents-dd-docs.git
```

### STEP3: create hook file into bare repository.


```bash
vi hugo-contents-dd-docs.git/hooks/post-receive


#!/bin/sh

cd ~/path/to/real/repository

# fetch repository
git --git-dir=.git pull origin master

# generate HTML
sh bin/hugo

# restart docker container
docker-compose -f docker/docker-compose.yml down
docker-compose -f docker/docker-compose.yml up -d

exit 0
```

