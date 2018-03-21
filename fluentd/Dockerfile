FROM fluent/fluentd:latest

RUN apk add --update --virtual .build-deps \
        sudo build-base ruby-dev \
                                 mariadb-dev mariadb-client-libs \
                                 tzdata \
 && sudo gem install \
        fluent-plugin-mysql \
 && sudo gem sources --clear-all \
# && apk del .build-deps \
 && rm -rf /var/cache/apk/* \
           /home/fluent/.gem/ruby/2.3.0/cache/*.gem \
