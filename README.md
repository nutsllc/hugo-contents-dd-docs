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

