FROM php:zts-alpine3.10

RUN apk add git bash

RUN mkdir -p /opt/phabricator && \
    cd /opt/phabricator && \
    git clone https://github.com/phacility/arcanist.git && \
    git clone https://github.com/phacility/libphutil.git

ENTRYPOINT ["/opt/phabricator/arcanist/bin/arc"]
