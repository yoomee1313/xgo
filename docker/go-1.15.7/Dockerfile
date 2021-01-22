# Go cross compiler (xgo): Go 1.15.7
# Copyright (c) 2021 The klaytn Authors. All rights reserved.
#
# Released under the MIT license.

FROM karalabe/xgo-base

MAINTAINER Choah Jade Jung <jade.jung@groundx.xyz>

# Configure the root Go distribution and bootstrap based on it
ENV GO_VERSION 11507

RUN \
  export ROOT_DIST=https://storage.googleapis.com/golang/go1.15.7.linux-amd64.tar.gz && \
  export ROOT_DIST_SHA=0d142143794721bb63ce6c8a6180c4062bcf8ef4715e7d6d6609f3a8282629b3 && \
  \
  sed -i '/darwin\/386/d' $BOOTSTRAP_PURE && \
  sed -i '/darwin GOARCH=386/d' $BOOTSTRAP_PURE && \
  sed -i 's/karalabe\/xgo/klaytn\/xgo/' $BOOTSTRAP_PURE && \
  \
  sed -i '483,488d' $BUILD && \
  \
  $BOOTSTRAP_PURE
