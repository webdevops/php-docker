# Prebuild PHP Docker Boilerplate images

![License MIT](https://img.shields.io/badge/license-MIT-blue.svg?style=flat)

This Dockerfiles are used for prebuild images for:

- [PHP Docker Boilerplate](https://github.com/mblaschke/php-docker-boilerplate)
- [TYPO Docker Boilerplate](https://github.com/mblaschke/TYPO3-docker-boilerplate)

Supported distributions:

- Ubuntu 12.04 - PHP 5.3, LTS (precise)
- Ubuntu 14.04 - PHP 5.5, LTS (trusty)
- Ubuntu 15.04 - PHP 5.6 (vivid)
- Ubuntu 15.10 - PHP 5.6 (wily)
- CentOS 7 - PHP 5.4

Following packages are included:

- common tools
- ansible (for easy provisioning)
- mysql client
- dnsmasq
- ssmtp
- supervisord
- php cli and fpm