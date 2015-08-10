#++++++++++++++++++++++++++++++++++++++
# CentOS 7 PHP Docker container
#++++++++++++++++++++++++++++++++++++++

FROM centos:7
MAINTAINER mblaschke82@gmail.com

ENV PATH /opt/ansible/bin:/bin:/usr/bin:/sbin:/usr/sbin
ENV PYTHONPATH /opt/ansible/lib
ENV ANSIBLE_LIBRARY /opt/ansible/library

# Install python
RUN yum clean all
RUN yum -y install \
        epel-release \
        PyYAML \
        python-jinja2 \
        python-httplib2 \
        python-keyczar \
        python-paramiko \
        python-setuptools \
        git \
        python-pip \
    && yum clean all

RUN git clone --recursive http://github.com/ansible/ansible.git /opt/ansible

# Install tools
RUN yum -y install \
        sudo \
        zip \
        unzip \
        bzip2 \
        ImageMagick \
        wget \
        curl \
        net-tools \
        moreutils \
        dnsutils \
        bind-utils \
        mysql \
        rsync \
        git \
        pygpgme \
    && yum clean all
    
# Install services
RUN yum -y install \
        ssmtp \
        dnsmasq \
        supervisor \
    && yum clean all
    
# Install php (cli/fpm)
RUN yum -y install \
        php-cli \
        php-fpm \
        php-json \
        php-intl \
        php-curl \
        php-mysqlnd \
        php-xdebug \
        php-memcached \
        php-mcrypt \
        php-gd \
        sqlite \
        php-xmlrpc \
        php-xsl \
        geoip \
        php-ldap \
        php-memcache \
        ImageMagick \
        ImageMagick-devel \
        ImageMagick-perl \
        php-pear \
        php-devel \
        gcc \
    && pecl install imagick \
    && yum clean all

# Update
RUN yum upgrade -y && yum clean all