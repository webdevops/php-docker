#++++++++++++++++++++++++++++++++++++++
# Ubuntu 12.04 PHP Docker container
#++++++++++++++++++++++++++++++++++++++

FROM ubuntu:12.04
MAINTAINER mblaschke82@gmail.com

# Ensure UTF-8
RUN locale-gen en_US.UTF-8
ENV LANG       en_US.UTF-8
ENV LC_ALL     en_US.UTF-8

# Install apt-add-repository
RUN apt-get update -q
RUN apt-get install -y python-software-properties
    
# Install ansible
RUN apt-add-repository ppa:ansible/ansible
RUN apt-get update -q
RUN apt-get install -y ansible python-apt aptitude

# Install tools
RUN apt-get install -y \
    sudo \
    zip \
    unzip \
    bzip2 \
    graphicsmagick \
    wget \
    curl \
    net-tools \
    moreutils \
    dnsutils \
    mysql-client
    
# Install services
RUN apt-get install -y \
    ssmtp \
    dnsmasq \
    supervisor
    
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
    php5-imagick

# Cleanup
RUN apt-get clean -y
RUN apt-get autoclean -y
