#++++++++++++++++++++++++++++++++++++++
# Ubuntu 15.10 PHP Docker container
#++++++++++++++++++++++++++++++++++++++

FROM ubuntu:15.10
MAINTAINER mblaschke82@gmail.com

# Ensure UTF-8
RUN locale-gen en_US.UTF-8
ENV LANG       en_US.UTF-8
ENV LC_ALL     en_US.UTF-8

# Install apt-add-repository
RUN apt-get update -q
RUN apt-get install -y \
    software-properties-common \
    && apt-get clean -y

# Install ansible
RUN apt-add-repository ppa:ansible/ansible
RUN apt-get update -q
RUN apt-get install -y \
    ansible \
    python-apt \
    aptitude \
    && apt-get clean -y

# Install tools
RUN apt-get install -y \
    lsb-release \
    sudo \
    zip \
    unzip \
    bzip2 \
    imagemagick \
    graphicsmagick \
    wget \
    curl \
    net-tools \
    moreutils \
    dnsutils \
    mysql-client \
    && apt-get clean -y

# Install services
RUN apt-get install -y \
    ssmtp \
    dnsmasq \
    supervisor \
    && apt-get clean -y

# Install php (cli/fpm)
RUN apt-get install -y \
    php5-cli \
    php5-fpm \
    php5-json \
    php5-intl \
    php5-curl \
    php5-mysqlnd \
    php5-xdebug \
    php5-memcached \
    php5-mcrypt \
    php5-gd \
    php5-sqlite \
    php5-xmlrpc \
    php5-xsl \
    php5-geoip \
    php5-ldap \
    php5-memcache \
    php5-memcached \
    php5-imagick \
    && apt-get clean -y

# Cleanup
RUN apt-get clean -y
RUN apt-get autoclean -y