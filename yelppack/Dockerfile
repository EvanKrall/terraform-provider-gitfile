FROM docker-dev.yelpcorp.com/lucid_yelp
MAINTAINER Evan Krall <krall@yelp.com>

RUN apt-get update && DEBIAN_FRONTEND=noninteractive apt-get install -yq \
    go \
    git \
    build-essential \
    ruby1.8 rubygems \
    libopenssl-ruby \
    ruby-dev \
    --no-install-recommends

ENV GOPATH /go

RUN gem install fpm
RUN ln -s /var/lib/gems/1.8/bin/fpm /usr/local/bin/fpm

#WORKDIR /go/src/github.com/Yelp/terraform-provider-gitfile
