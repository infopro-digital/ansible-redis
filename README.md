Redis Ansible
=============

[![Ansible Galaxy](http://img.shields.io/badge/ansible--galaxy-infopro-digital.redis-blue.svg)](https://galaxy.ansible.com/list#/roles/3989) [![Build Status](https://travis-ci.org/infopro-digital/ansible-redis.svg)](https://travis-ci.org/infopro-digital/ansible-redis)

Install and configure [Redis](http://redis.io/).

Requirements
------------

- Only Debian Wheezy or Jessie.

Role Variables
--------------

  - Default config file is defined in [default vars](defaults/main.yml). All config vars are prefixed with "redisconf\_".
  - redis\_use\_apt\_backports: set true to install Redis from backports (default: false).
  - redis\_enable: set true to enable Redis service (default: true)
  - redis\_service\_manage: set true to let role manage Redis server start/enable/restart on config change.

Dependencies
------------

None.

Example Playbook
----------------

### Simple

    - hosts: servers
      roles:
         - { role: infopro-digital.redis }

### Redis from Backports

    - hosts: servers
      roles:
         - { role: infopro-digital.redis, redis_use_apt_backports: true }

License
-------

GPLv2

Author Information
------------------

  - All issues, pull-request are welcome :)
