[![Build Status](https://travis-ci.org/wtanaka/ansible-role-certbot.svg?branch=master)](https://travis-ci.org/wtanaka/ansible-role-certbot)
[![CircleCI](https://circleci.com/gh/wtanaka/ansible-role-certbot.svg?style=svg)](https://circleci.com/gh/wtanaka/ansible-role-certbot)

wtanaka.certbot
===============

Installs certbot command line tools for the letsencrypt certificate
authority

Example Playbook
----------------

    - hosts: servers
      roles:
         - role: wtanaka.certbot
           # Read the TOS then uncomment this
           # letsencrypt_agree_tos: --agree-tos
           letsencrypt_email: example@example.com
           letsencrypt_webroot: /var/www/html
           letsencrypt_domains:
           - wtanaka.com
           - www.wtanaka.com


Or you can include just the role, and configure it in

    PLAYBOOK
    - hosts: servers
      roles:
         - wtanaka.certbot

    HOST_VARS file:

    # Read the TOS then uncomment this
    # letsencrypt_agree_tos: --agree-tos
    letsencrypt_email: example@example.com
    letsencrypt_webroot: /var/www/html
    letsencrypt_domains:
    - wtanaka.com
    - www.wtanaka.com

License
-------

GPLv2

Author Information
------------------

http://wtanaka.com/
