FROM ruby:2.3.1

MAINTAINER Marcelo Pélos

RUN curl -sL https://deb.nodesource.com/setup_7.x | bash - && \
    apt-get update -qq && apt-get install -y build-essential nodejs && \
    apt-get clean
