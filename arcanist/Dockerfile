FROM php:zts-alpine3.10

RUN apk add bash git openssh

RUN mkdir -p /opt/phabricator && \
    cd /opt/phabricator && \
    git clone https://github.com/phacility/arcanist.git

ENTRYPOINT ["/opt/phabricator/arcanist/bin/arc"]
