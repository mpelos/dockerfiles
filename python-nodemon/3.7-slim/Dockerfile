# Use an official Python runtime as a parent image
FROM python:3.7-slim

WORKDIR /root

RUN rm -rf /var/lib/apt/lists/* && \
    apt-get update && apt-get install -y curl && \
    curl -sL https://deb.nodesource.com/setup_12.x | bash - && \
    DEBIAN_FRONTEND=noninteractive apt-get install -y apt-utils nodejs yarn groff

RUN npm install -g nodemon

RUN pip3 install --upgrade pip && \
    pip3 install jupyter
