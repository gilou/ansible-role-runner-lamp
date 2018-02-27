runner-lamp
=========
This role is aimed at deploying a LAMP setup for symfony using PHP from Ondřej Surý's repository
At this point, it's published so it can be used as a proof of concept for a galaxy deployment scenario.

Requirements
------------

We assume some gitlab-runner or vagrant configuration. By default it will try to use the vagrant user.

Role Variables
--------------

|```runner_webroot```|Root for our files|/srv/www|
|```runner_apache_group```|Group for apache|www-data|
|```runner_mysql_password```|mysql root password|~|
|```runner_mysql_userdb```|Users and password, and their db to create|{test: test}|
|```runner_domain```|Domain (suffix) used for this runner|test.dawan.biz|
|```runner_extra_packages```|Packages to add to those in vars|~|
|```runner_install_composer```|Should we install composer|True|
|```runner_php_version```|PHP Version to install (from Sury's repos)|7.2|

Dependencies
------------

none for now

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: gilou.runner-lamp }

License
-------

WTFPL

