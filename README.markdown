# Vagrant (precise32) + Node

## Installs

- [n](https://github.com/visionmedia/n)
    - latest stable node
        - express
        - grunt-cli
        - bower
        - supervisor
        - jshint
        - jslint
        - yuidocjs
- mongodb
- puppet 3
- zsh

## Depencies

- Git
- [Vagrant 1.2.x](http://www.vagrantup.com/)

## Usage

```
git clone https://github.com/hstkk/vagrant-node.git
cd vagrant-node
git submodule init
git submodule update
vagrant up
vagrant ssh
```

## Protips

- Static IP address is 10.10.10.10
- `/home/vagrant/workspace` is shared folder
- Speed up startup

```
vagrant up --no-provision
```

- Use suprevisor

```
supervisor app.js
```
