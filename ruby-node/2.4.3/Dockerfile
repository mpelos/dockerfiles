FROM ruby:2.4.3

MAINTAINER Marcelo Pélos

RUN curl -sL https://deb.nodesource.com/setup_9.x | bash - && \
    apt-get update -qq && apt-get install -y build-essential nodejs && \
    apt-get clean
