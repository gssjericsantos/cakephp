FROM php:alpine
LABEL maintainer=<"ronjericsantos.gss@gmail.com">
RUN apk update && apk add bash \
    npm \
    curl \
    apache2 \
    mysql \
    mysql-client \
    #libapache2-mod-php \
    #php-mysql \
    php-mbstring \
    php-intl \
    php-xml \
    && curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer \
    && chmod +x /usr/local/bin/composer \
    && composer self-update \
    && rm /var/cache/apk/*
WORKDIR /src/composer
VOLUME /src/composer
ENTRYPOINT ["composer"]
