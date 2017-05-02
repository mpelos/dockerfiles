FROM mpelos/ruby-node:2.4.1

MAINTAINER Marcelo Pélos

WORKDIR /app

RUN curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | apt-key add - && \
    echo "deb https://dl.yarnpkg.com/debian/ stable main" | tee /etc/apt/sources.list.d/yarn.list && \
    apt-get update && apt-get install -y apt-utils yarn && \
    gem install rails -v 5.1.0
