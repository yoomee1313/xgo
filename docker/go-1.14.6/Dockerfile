# Go cross compiler (xgo): Go 1.14.6
# Copyright (c) 2020 Péter Szilágyi. All rights reserved.
#
# Released under the MIT license.

FROM karalabe/xgo-base

MAINTAINER Choah Jade Jung <jade.jung@groundx.xyz>

# Configure the root Go distribution and bootstrap based on it
ENV GO_VERSION 11406

RUN \
  export ROOT_DIST=https://storage.googleapis.com/golang/go1.14.6.linux-amd64.tar.gz && \
  export ROOT_DIST_SHA=5c566ddc2e0bcfc25c26a5dc44a440fcc0177f7350c1f01952b34d5989a0d287 && \
  \
  $BOOTSTRAP_PURE
