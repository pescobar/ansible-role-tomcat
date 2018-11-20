[![Build Status](https://travis-ci.org/pescobar/ansible-role-tomcat.svg?branch=master)](https://travis-ci.org/pescobar/ansible-role-tomcat)

ansible-role-tomcat
=========

Install the tomcat tarball and systemd init script


Role Variables
--------------
```
tomcat_version: "8.5.35"

tomcat_major_version: "{{ tomcat_version.split('.')[0] }}"

tomcat_url: "http://apache.rediris.es/tomcat/tomcat-{{ tomcat_major_version }}/v{{ tomcat_version }}/bin/apache-tomcat-{{ tomcat_version }}.tar.gz"

tomcat_install_folder: "/opt"

java_home: "/opt/java"

tomcat_user: "tomcat"

tomcat_group: "tomcat"
```

Dependencies
------------

Role [pescobar.java_oracle](https://galaxy.ansible.com/pescobar/java_oracle)


Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: pescobar.tomcat }

License
-------

GPLv3

Author Information
------------------

Pablo Escobar
