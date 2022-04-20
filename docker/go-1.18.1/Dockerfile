# Go cross compiler (xgo): Go 1.18.1
# Copyright (c) 2022 The klaytn Authors. All rights reserved.
#
# Released under the MIT license.

FROM karalabe/xgo-base

MAINTAINER Aidan Kwon <aidan.kwon@krustuniverse.com>

# Configure the root Go distribution and bootstrap based on it
ENV GO_VERSION 11801

RUN \
  export ROOT_DIST=https://go.dev/dl/go1.18.1.linux-amd64.tar.gz && \
  export ROOT_DIST_SHA=b3b815f47ababac13810fc6021eb73d65478e0b2db4b09d348eefad9581a2334 && \
  \
  sed -i '/darwin\/386/d' $BOOTSTRAP_PURE && \
  sed -i '/darwin GOARCH=386/d' $BOOTSTRAP_PURE && \
  sed -i 's/karalabe\/xgo/klaytn\/xgo/' $BOOTSTRAP_PURE && \
  \
  sed -i '483,488d' $BUILD && \
  \
  $BOOTSTRAP_PURE
