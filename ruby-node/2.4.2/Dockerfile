FROM ruby:2.4.2

MAINTAINER Marcelo Pélos

RUN curl -sL https://deb.nodesource.com/setup_8.x | bash - && \
    apt-get update -qq && apt-get install -y build-essential nodejs && \
    apt-get clean
