alpine-golang-buildimage
========================

This repository contains the sources for the following [docker](https://docker.io) base images:
- [`sharops/alpine-golang-buildimage`]

## Usage

This Image is intedend to be used in multi stage docker builds and is not for final or production use you can find more info
about multistage build in this [blog post](https://www.critiqus.com/post/multi-stage-docker-builds/)

```
FROM iopsthecloud/alpine-golang-buildimage

ADD . /go/src/github.com/lacion/test
WORKDIR /go/src/github.com/lacion/test

RUN go build *.go

```
## Developing and testing

```bash
# Pull image
git clone ssh://git@github.com/sharops/alpine-golang-buildimage.git
cd alpine-golang-buildimage

# hack hack hack

# Build
make build

# Test
