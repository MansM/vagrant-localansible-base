# Vagrant Local Ansible

## Purpose
This environment allows you to develop ansible code for new roles

## Starting it up

* Make sure you are on a connection without a proxy (by example a guest wifi)
* Install Vagrant & virtualbox
  * http://www.vagrantup.com
  * http://www.virtualbox.org
* Add Vagrant binary to your Path


```
vagrant up
```

## Create ansible roles

[see creating role](creatingrole.md)

## Tips
Username & Password : vagrant/vagrant (rootpw = vagrant)

ssh access: vagrant ssh

reprovision without destroy: vagrant provision

startover: vagrant destroy -f && vagrant up

in the VM you find your files in /vagrant

in the Vagrantfile you can change the amount of output:
```
ansible.verbose = "v"
up to 
ansible.verbose = "vvvv"
````
