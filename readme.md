# Vagrant Local Ansible

## Purpose
This environment allows you to develop ansible code for new roles

## Starting it up

* Make sure you are on a connection without a proxy (by example a guest wifi)
* Install Vagrant & virtualbox
** http://wwww.vagrantup.com
** http://www.virtualbox.org
* Add Vagrant binary to your Path


```
vagrant up
```

## Tips
Username & Password : vagrant/vagrant

ssh access: vagrant ssh

reprovision without destroy: vagrant destroy

startover: vagrant destroy -f && vagrant up

