FROM debian:stretch

# Make sure we don't get notifications we can't answer during building.
env DEBIAN_FRONTEND noninteractive

LABEL maintainer "Jonathan Goldfarb <jgoldfar@my.fit.edu>"

RUN set -eux; \
  apt-get update; \
  apt-get install -y --no-install-recommends \
    ca-certificates \
# ERROR: no download agent available; install curl, wget, or fetch
    curl \
  ; \
  rm -rf /var/lib/apt/lists/*

ENV JULIA_PATH /usr/local/julia
ENV PATH $JULIA_PATH/bin:$PATH

# https://julialang.org/juliareleases.asc
# Julia (Binary signing key) <buildbot@julialang.org>
ENV JULIA_GPG 3673DF529D9049477F76B37566E3C7DC03D6E495
