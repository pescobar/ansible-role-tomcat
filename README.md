[![pipeline status](https://bc2-gl.bc2.unibas.ch/ansible/ansible-roles/scicore-tomcat/badges/master/pipeline.svg)](https://bc2-gl.bc2.unibas.ch/ansible/ansible-roles/scicore-tomcat/commits/master)


scicore-tomcat
=========

Install the tomcat tarball and systemd init script


Role Variables
--------------
```
tomcat_version: "8.5.27"

tomcat_major_version: "{{ tomcat_version.split('.')[0] }}"

tomcat_url: "http://apache.rediris.es/tomcat/tomcat-{{ tomcat_major_version }}/v{{ tomcat_version }}/bin/apache-tomcat-{{ tomcat_version }}.tar.gz"

tomcat_install_folder: "/opt"

java_home: "/opt/java"

tomcat_user: "tomcat"

tomcat_group: "tomcat"
```

Dependencies
------------

Role [scicore-java-oracle](https://bc2-gl.bc2.unibas.ch/ansible/ansible-roles/scicore-java-oracle)


Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: scicore-tomcat }

License
-------

GPLv3

Author Information
------------------

Pablo
