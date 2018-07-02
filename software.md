---
layout: page
title: Software Installation
sidebar_link: true
permalink: /software-installation/
---



## Bare Metal - Dev Machine

### System Requirements

* Ubuntu / MacOS


### Install Ruby

#### Ruby Version Manager
We are going to install ruby through a Ruby Version Manager. It is highly recommended
that we use a version manager, as Ruby release new versions ever year on December 25th
and a security patch is released as soon as a vulnerability is made known.

The tool I personally recommend is RVM (Ruby version manager).

[https://rvm.io](https://rvm.io)

```sh
gpg --keyserver hkp://keys.gnupg.net --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3 7D2BAF1CF37B13E2069D6956105BD0E739499BDB

curl -sSL https://get.rvm.io | bash -s stable
```

If you see an error that says curl doesn't exist do:

```sh
sudo apt-get install curl
```

*Note:* Do not install RVM or ruby as a root user. We recommend this as we don't want
the applications we are building to have root permission. Giving root permission to an application could lead to serious securitiy issues in the future.

#### Install latest Ruby

It is always recommended to work in the latest version of any tool before you build your
application. As the chances are that you wont be able to upgrade once you start
writing business critical code.

```
rvm install 2.5.1
```

### Install Rails



### Install Database (If your workshop coveres databases as well)



*All the software recommended in this workshop are free and open source*
