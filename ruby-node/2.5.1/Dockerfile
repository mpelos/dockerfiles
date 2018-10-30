FROM ruby:2.5.1

MAINTAINER Marcelo Pélos

RUN curl -sL https://deb.nodesource.com/setup_10.x | bash - && \
    apt-get update -qq && apt-get install -y build-essential nodejs && \
    apt-get clean
