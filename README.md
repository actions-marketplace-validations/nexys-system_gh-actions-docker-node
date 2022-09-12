# Gh actions docker

This GitHub Action will build your node app and turn it into a docker container

Tested with koa

see [gh-actions-spa-test](https://github.com/nexys-system/gh-actions-spa-test) if you only need build + test

## Usage

```
name: Docker

on:
  push:
    tags:
      - v*

jobs:
  test:
    runs-on: ubuntu-latest
    steps:
      - uses: nexys-system/gh-actions-docker-node@v0.0.1
```

## Parameters

* `container-name`: docker name. Default: name of the repo
* `build-command`: build command. Default is `VITE_VERSION=${GITHUB_REF##*/} VITE_GIT_SHA=$GITHUB_SHA yarn build`
* `yarn` is used, to install and test (`yarn test`)


## License
The scripts and documentation in this project are released under the [GNU GPLv3 License](https://github.com/nexys-system/gh-actions-docker-spa/blob/main/LICENSE).
