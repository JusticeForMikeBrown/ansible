
Reset Root User Password
=======================

This role will reset root user on servers either using random password or one set at command line

The chosen password, and server hostname, will be written to localhost log file

Message that password was reset will be sent to Slack

Requirements
------------

You must have Ansible 2.0 installed.

You need a Slack server

Examples
--------

If setting password

ansible-playbook $ANSIBLE_HOME/utilities/reset_password.yml -e hosts=node113 --sudo -K "-e new_password=test12345"


If random password

ansible-playbook $ANSIBLE_HOME/utilities/reset_password.yml -e hosts=node113 --sudo -K "-e random=[]"

TODO
--------------

Use ansible-vault for crypted password

Integrate with LastPass
