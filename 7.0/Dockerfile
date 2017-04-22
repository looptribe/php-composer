FROM ubuntu:16.04

MAINTAINER Diego Ferri <diego.ferri@looptribe.com>

RUN apt-get update && DEBIAN_FRONTEND=noninteractive \
	apt-get -o Dpkg::Options::="--force-confnew" install -y \
	php7.0 \
	php-cli \
	php-curl \
	php-dev \
	php-gd \
	php-intl \
	php-mbstring \
	php-mcrypt \
	php-mysql \
	php-sqlite3 \
	php-xdebug \
	zip \
	unzip \
	git

RUN phpenmod mcrypt

COPY web.ini /etc/php/7.0/cli/conf.d/90-web.ini

RUN curl -sS https://getcomposer.org/installer | \
	php -- --install-dir=/usr/local/bin
