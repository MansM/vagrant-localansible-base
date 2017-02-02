# How to create a new ansible role

## creating the ansible role skeleton
```
vagrant ssh
-bash: warning: setlocale: LC_CTYPE: cannot change locale (UTF-8): No such file or directory
[vagrant@ansible-centos ~]$ cd /vagrant
[vagrant@ansible-centos vagrant]$ cd roles/
[vagrant@ansible-centos roles]$ ansible-galaxy init newrole
- newrole was created successfully
[vagrant@ansible-centos roles]$ ls -l
total 0
drwxr-xr-x. 1 vagrant vagrant 408 Feb  2 10:01 newrole
```

## Adding it to the set of roles to run:
edit playbook.yml:
```
- hosts: all
  become: yes
  roles:
    - newrole
  tasks:
    - name: echo hello world
      shell: echo "hello world"
```